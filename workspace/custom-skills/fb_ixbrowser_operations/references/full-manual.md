# FB 运营（指纹浏览器方案）移植手册

版本：2026-11-17。适用：把现在这套 FB 获客运营完整搬到另一台 Windows 电脑上跑。
包里没有任何密码、令牌、cookie、代理凭据——那些不能跟着包走，新电脑上现配（见第 10 节）。

## 1. 包里有什么

```
portable-fb-ops/
├── 00-移植手册.md              # 本文件
├── agent-v6/                   # 常驻小程序（全权限版，给自己人用的电脑）
│   ├── ixbrowser_agent.py      # 服务主程序（端口 8765）
│   ├── ixbrowser_driver.py     # ixBrowser API 驱动
│   ├── config.example.json     # 令牌模板（照着填新令牌，别直接用）
│   ├── requirements.txt
│   ├── install.bat             # 装一次：桌面快捷方式 + 开机自启 + 启动
│   ├── start.bat / stop.bat
│   └── README_AGENT.md
├── agent-v7-restricted-src/    # 受限版源码（给组员/外人用的电脑，见第 11 节）
├── concat/                     # 剪辑桥
│   ├── concat_bridge.py        # 跑在新电脑上，端口 8766，转给 Concat 的 MCP
│   ├── concat_client.py        # Muse 侧客户端
│   ├── concat_bridge_startup.bat
│   └── STATUS.md
├── driver/                     # Muse 侧驱动与核验脚本
│   ├── ixbrowser_driver.py
│   ├── list_tags.py            # 列 profile 的 tag/group
│   ├── flows/ixb_client.py     # IxAgent 客户端（令牌存在 Muse 侧，不在包里）
│   ├── flows/check_default11.py / check_final.py / check_retry7.py
│   ├── flows/warm_default.py
│   └── profiles-20261117.md    # 账号矩阵快照（2026-11-17 核验结果）
├── playbooks/                  # 话术与规则（完整版，原样照搬）
│   ├── dm-playbook-combined.md     # 私信话术合并打法（主本）
│   ├── dm-sop-company.md           # 公司私信 SOP
│   ├── company-sops-digest.md      # 公司 SOP 摘要
│   ├── boss-chat-technique-jocelyn.md  # 老板亲示范例（Jocelyn Bee）
│   ├── dm-rate-measurement.md      # 私信频率实测
│   ├── ai-video-routine.md         # AI 面诊视频制作与发布 routine
│   ├── content-adjustment-2026-11-05.md  # 评论去模板化调整
│   └── competitor-watchlist.md     # 同行监控名单
└── crons-inventory.md          # 定时任务清单（任务跑在 Muse 侧，见第 9 节）
```

不含客户数据：leads、dm-threads、group-prospects 这些台账不打包（里面是客户隐私），新电脑上从零开始记。

## 2. 整体架构

```
Muse（总管，跑在云端 VM）
  │  Tailscale 内网
  ├─ 100.78.166.12:8765 ──► ixBrowser Agent（常驻小程序，跑在用户电脑上）
  │                           ├─ ixBrowser Local API 127.0.0.1:53200（只听本机）
  │                           ├─ 浏览器 CDP 调试端口（只听本机）
  │                           └─ 10 个 profile（每号一个浏览器环境）
  ├─ 100.78.166.12:8766 ──► Concat 桥（剪辑，跑在用户电脑上）
  │                           └─ Concat MCP（concat.exe --mcp，46 个工具）
  ├─ facebook-cli（后台发 FB Reel、发评论、读帖子）
  └─ instagram-cli（后台发 IG Reel；须先连账号）
```

关键点：ixBrowser 的接口和浏览器调试端口只听本机（127.0.0.1），Muse 从外面够不着，所以必须在装 ixBrowser 的那台电脑上跑常驻小程序，浏览器操作全在本机完成。Muse 只发高层指令（开哪个号、去哪个网址、点什么、说什么）。

## 3. 新电脑要装什么

- Windows 10/11（64 位）。
- Python 3.12+（原机是 3.15.2），装完勾上“Add to PATH”。
- ixBrowser 客户端（指纹浏览器），在设置里打开 Local API 开关（付费功能）。账号用新电脑使用人的员工号登录，只看自己被授权的分组。
- Tailscale，登录进同一个 tailnet（原机 Tailscale IP：100.78.166.12；Muse 侧 100.74.60.50）。
- Concat v0.2.11（GitHub jub0t/Concat），装到 `D:\Concat\concat.exe`（路径固定，桥里写死了这个位置，换地方要改桥）。
- ffmpeg（WinGet 装，已在 PATH，用于剪辑前后的核验；装 Concat 也行，但 ffprobe 核验音频軌数要用到）。

## 4. 安装步骤（新电脑上）

### 4.1 常驻小程序 agent-v6

1. 把 `agent-v6/` 解压到固定文件夹（比如 `D:\ixbrowser-agent`，以后别挪地方）。
2. 生成一个新令牌，写进 `config.json`：复制 `config.example.json` 改名为 `config.json`，把里面的 `REPLACE_WITH_NEW_TOKEN` 换成一个新生成的随机长字符串（不要复用旧电脑的令牌，每台电脑一个独立令牌）。
3. 双击 `install.bat`：建桌面快捷方式“ixBrowser Agent”、加开机自启、立即后台启动（无黑窗口）。
4. 验活：在浏览器打开 `http://<新电脑 Tailscale IP>:8765/health`，应返回 `{"ok": true, "agent": "ixbrowser-agent", "version": 6}`。
5. 把新电脑的 Tailscale IP + 新令牌告诉 Muse，Muse 登记后才能像操作原机一样操作这台电脑。

### 4.2 Concat 剪辑桥

1. 把 `concat/concat_bridge.py` 拷到 `D:\ixbrowser-agent\concat_bridge.py`（和 agent 同目录，共用 `config.json` 里的令牌）。
2. 把 `concat/concat_bridge_startup.bat` 放进 Startup 文件夹（开机自启），双击一次立即启动。
3. 验活：`http://<新电脑 Tailscale IP>:8766/health` 应返回 ok 且 mcp_running 为 True。

### 4.3 ixBrowser 账号

1. 在新电脑的 ixBrowser 里新建 profile（每号一个），或从原机导出导入（只导环境配置，不导登录态）。
2. 每个号在自己的 profile 里登录一次 Facebook / Instagram（输账号密码、过 2FA——真人验证要号主在自己手机上点批准）。
3. 打标签：tag='fb' 是 Facebook、tag='ins' 是 Instagram；放进默认分组（group_id=1）。
4. 登录态核验：用 `driver/flows/check_default11.py` 的思路逐个 open → check → goto 对应网址（fb→facebook.com，ins→instagram.com）→ 截图，看登录名对不对、feed 正常不正常。核验全程后台，不在桌面打开给人看；查完就关，不留窗口。

## 5. 账号矩阵（2026-11-17 核验，10 个号 + 1 个主号）

计数口径：按 10 个算。Victoria 是主号（早就在 facebook-cli 与云浏览器跑），不计在这 10 个里。

| profile | 账号 | 平台 | 方向 | 登录名（核验） |
|---|---|---|---|---|
| 1 | 61590579626399 | FB | 待定 | Emerson |
| 2 | 61590577106578 | FB | 面提（主号） | Victoria Maizie（不计入 10 个） |
| 5 | 61576748891565 | FB | 鼻子 | Jusa Khan（Dr. Qin Hao Eye Rejuvenation） |
| 32 | LarkMuthana | FB | 面提 | Daisy |
| 38 | 61588835991792 | FB | 待定 | Oe |
| 67 | 61581899105351 | FB | 待定 | Ejje |
| 80 | 100031033479770 | FB | 待定 | Winsino |
| 43 | pokkhusadedere | IG | 鼻子 | 已登录 |
| 44 | sarahcook6809 | IG | 面提 | 已登录 |
| 63 | elainaklocko | IG | 面提 | 已登录 |
| 65 | gaga5456 | IG | 鼻子 | 已登录（当日 IG 已用 9 小时 37 分，弹每日限额提示，会话有效） |

方向说明：2026-11-16 定的是鼻子 3（Jusa、gaga、pokk）+ 面提 4（Victoria、Lark、sarah、elaina）。新并进来的 4 个 FB 号（Emerson、38、67、80）方向未定，等老板定；建议 FB 6 个按 3 鼻子 / 3 面提分，保持平衡。IG 维持 2 鼻子 / 2 面提。

归属：默认分组 11 个 profile 是老板本人的账号；其他分组（尹卓/小徐/蔡蔡/少婷/辰昊）是组员各自的账号，不动、不核验、不写进矩阵。

## 6. 猎手逻辑（主动找客户）

- 每 10 分钟一轮，全天滚动；每轮最多 3 条新评论；全天不设条数上限，量只受平台限制（出现受限/限额/摩擦提示立即停工并报）。
- 腿一（同行爆款评论区截流）：监控名单见 `playbooks/competitor-watchlist.md`（doctor.truesdale、nayakplasticsurgery、reface_scarless、drkassir、dra.camimartinez、toropclinic、dr.zhang.3u 等），看最近 2–3 天高播放帖子的评论区，找问价/问预约/问哪里做/要联系方式/问维持多久/问恢复期/说“我想做”的人，用医生身份回专业干货。
- 腿二（需求帖挖掘）：搜求推荐/求助帖（关键词如 recommend facelift surgeon、best rhinoplasty doctor、facelift before after advice、where to get facelift），重点看公开群组；已加入群组清单见猎手任务正文（Facelift Support Group、Blepharoplasty Support Group、Rhinoplasty and Revision Rhinoplasty、Facelift & Necklift Turkey、Plastic Surgery in Turkey、Facelift in Korea、Tijuana Plastic Surgery & Medical Tourism 等），每轮扫 1 个群的最新帖，群里发现的合格意向先记收集表再触达。
- 腿三（主动私信跟进）：对腿一/腿二里公开表达过明确意向的人发 Messenger 私信，话术见第 7 节。
- 回评跟进：每轮重读已评论帖的回复楼层（包括他人评论下面的回复楼层，CLI 只能读顶层，回复楼层走浏览器读），楼主回复了我方评论当天就接话；达到私信门槛（问价、要联系方式、明确想做）转私信流程。
- 评论风格（2026-10-26 定，2026-11-05 去模板化）：2–4 句，先一句勾住他的话再留一个让他想回的问题，不列长清单、不讲课；每条必须带楼主原帖独有的一个细节（年龄、部位、国家、面诊阶段、最担心的点、已提到的医生/诊所），钩子轮换（恢复时间线、避坑点、面诊必问清单、过程案例），结尾问题改二选一；发评论前除筛楼主外还要扫热门评论者，带推广嫌疑特征（化名格式、二手医生名单、同天多帖点评医生/诊所/恢复中心）的标注为邻近推广嫌疑，绝不回复、不 @、不接话；顶楼评论要点名楼主或复述楼主原问题。
- 评论区红线：不提“来找我做”、不留 WhatsApp/链接/电话、不贬低同行（链接和联系方式只在私信里发）。
- 去重：去重台账 `fb-reply-seen.md`，发之前重读、发完一条立即记一条，不攒到轮次结束；台账里出现过的父评论/帖子/人一律跳过。
- 审核：短评论先经 E07 短内容卡打分 90 分以上 + 总管确认才能发；长内容发布还需老板点头。
- 429 只是瞬时限流，不是每日额度：遇 429 短暂退避后重试，不停查、不等明天、不自己设限。
- 通道：猎手主路线是浏览器（2026-11-11 定，绕开 CLI 429）；旧静态 IP 方案已于 2026-11-17 删除，不再走任何代理、不再等新线。

## 7. 私信逻辑（盯守与跟进）

完整话术在 `playbooks/` 里（原样照搬，一个字没改）：

- `dm-playbook-combined.md`：私信话术合并打法（主本）。来源 A 是飞书《私信话术》公司 SOP，来源 B 是话术库。
- `dm-sop-company.md`：公司私信 SOP 原文。
- `company-sops-digest.md`：公司 SOP 摘要。
- `boss-chat-technique-jocelyn.md`：老板 2026-11-12 亲自示范 Jocelyn Bee 的打法（信号到了直接要号的范例）。
- `dm-rate-measurement.md`：私信频率实测。

口径总纲（细节以 playbooks 原文为准）：

- 唯一 KPI = 合格客资（带国家区号 WhatsApp + 国家）。准用户 = 海外 + 真实手术意向 + 需求对公司品相 + 真人个人号；同行/机构号、已术后求助、纯赞美吃瓜、明确拒绝出国、广告号完全不联系。
- 私信一次只发一条，等对方回话再发下一条（2026-11-06 硬规则）。
- 首条禁直接索号：只接住他原帖的具体问题给一句实在回答 + 问一个跟他本人有关的问题；每人说法不同。
- 漏斗：第 1–2 条接问题 + 问本人问题（不提号/WhatsApp/咨询团队），第 3 条给面诊钩子（秦浩医生线上远程视频面诊，每周 2 个免费名额、先到先得，具体时间 + 名额 + 下一步，不直接要号），第 4 条起给干货再推留号；已发 ≥3 条未给钩子的线程下一条即补钩子。
- 信号到了直接要号（Jocelyn Bee 范例）：客户主动问价/问地点/问怎么约 = 推进信号，只答离成交最近的一个问题、直接要带区号 WhatsApp，不给“先发链接”这类拖延选项；给号后 45 秒内回“咨询顾问很快联系你”，区号核对（区号 + 末四位、英国号首位 0 国际拨打去 0）写进移交备注。
- 价格零报价零区间：不直接说费用、不给任何数字区间；问价一律按公司 SOP 回应“费用看个人情况、需面诊确定、咨询团队会联系”。
- 地点只在他问“远不远/在哪做”时再说、只说相关的；集团只说重庆/上海/台湾，未核实城市只说“可以安排对接、具体由咨询团队确认”，巴黎没有服务点、绝不虚构地址。
- 不愿留号给咨询链接 https://drqh.jianjianmeili.com/vMPEX84o（私信可发，评论区不贴）。
- 跟进节奏：B-18（24–48h）、B-19（3–7 天），之后每隔 2–3 天可再补一条真人式再询问、最多再补 2 条；明确拒绝/拉黑立即停。
- 表情看状态宁少勿多：正面/轻松时可点 👍/❤️；担忧/纠结/问正事时不点；医疗场景不用 😆/😡。
- 送达判定：私信“已发送”必须经 Messenger CLI 查到线程存在且 snippet 为我方消息，才可汇报已发；只看浏览器气泡 = 未核验，不得汇报送达。
- 新好友立即联系：私信盯守每 5 分钟用 CLI 对好友列表做差分，筛查后仅收集表里的人/评论过的意向客户中的真人个人号才按私信口径立即发首条；待处理好友请求每轮经浏览器核查，疑似真实意向客户先通过再立即私信，身份拿不准先报老板再定。
- 盯守节奏：私信盯守 5 分钟一轮、客户雷达 1 小时一扫、猎手 10 分钟一轮、新私信 30 秒实时哨兵。
- 私信 PIN：各号聊天 PIN 基本是六个 8 或 123456，六个 8 居多；对应关系记工作文件、不写记忆正文、不进包。

## 8. 发布流程（视频）

- 一个视频 = FB + IG 两个平台才算发完。FB = Victoria（后台 CLI），IG = gaga5456（鼻子号）；10 个号铺开后按配对发。
- **所有发布一律走后台，绝不走浏览器发帖框**（2026-11-16 硬规则）：FB Reel = 单个视频文件，`facebook-cli post create --message '文案' --file 视频.mp4`（不带封面图）；IG Reel = `instagram-cli post-feed --account-id <号> --file 视频.mp4 --cover 封面.jpg --caption '文案'`（IG 才要封面）。2026-11-16 浏览器发帖框误发过一次：封面 + 视频一起挂上去，FB 发成了图片帖、不是 Reel（帖 122154037917352570，删不删等老板确认，删除须走浏览器、不得擅自删）。
- 视频文件夹：桌面 `秦浩视频\未发视频\`，每个视频一个文件夹、里面带封面；发完移到 `秦浩视频\已发视频\`，并在该视频文件夹里写 `发布结果.txt`（成功/失败、失败原因、成功给链接）。同一账号不发重复视频。
- 视频数量公式：需要视频数 = max(FB 账号数, IG 账号数) × 每账号发几条。当前 6 个 FB / 4 个 IG，每账号发 1 条需 6 个视频；每账号发 3 条需 18 个。
- 发布时间：统一从下午 4 点（16:00，用户当地时间）开始，每个视频间隔 2 小时；同一轮次所有账号都发，但每账号之间错开几分钟（不要同一秒齐发），模拟真人手动切换账号。
- 视频文案由 Muse 自己写：对外英文，钩子 + 具体设计点 + 互动问题，AI 视频注明 AI-generated video for illustration。
- 发完立即做两件事（固定动作）：① 在本号评论区留一句自评引流评论，引导点主页 WhatsApp 联系链接，评论本身不贴链接、不贴电话；② 发了视频的账号互相看其他账号发的视频，把完播率拉起来。
- IG 后台连接：instagram-cli 至今未连上账号（accounts 为空），须老板点 IG 连接链接 https://agent.meta.ai/foa_ac_link/instagram 把 gaga5456 连上后台后才能发；没连上之前 IG Reel 一直待发、不走浏览器顶。
- 审核：AI 视频过 E07 90 分可直接发、事后报链接（真实患者视频仍先审后排）；内容先经 E07 90 分以上 + 总管确认，长内容发布还需老板点头；红线（假对比、伪造疗效、修患者影像、虚构服务点、他医冒充、他人水印或中央大水印）一票否决。
- AI 面诊视频标准（routine 全文见 `playbooks/ai-video-routine.md`）：10 秒版（2 秒封面 + 5 秒面诊 + 3 秒尾卡）；视频/封面/尾卡不许出现“AI 生成/AI-generated”“效果示意”字样；医生不露脸、不用 AI 脸（秦浩真照片为唯一面部参照）；面诊静音或背景音乐、无字幕；口播配音须医生本声、TTS 不接受；发布文案注明 AI 部分。
- 选片口径：过程型（术前划线→手术→恢复多阶段多场景），不要单人大脸成果特写；淡半透明签名可接受，大/中央水印弃用，疑似假对比禁用；非本案患者不露脸（只取切口/器械/手部近景），本案患者可露脸。
- 视频先审后排：所有确定好的视频必须先发老板看、确认后才能排期发布；例外：老板发来的成品视为已批准、直接发不再另等过目。
- 发视频必剥原音轨只留我方一条（ffprobe 核 = 1），选曲对标源爆款氛围/BPM、现代轻快；每天发布前先看前一天数据再定当天内容，读不到注明未读到、不编数据。

## 9. 定时任务清单（跑在 Muse 侧，不跟着电脑走）

这些任务是 Muse 的调度器在跑，不在新电脑上。新电脑只要 agent + Concat 桥装好，Muse 侧照单登记 IP/令牌就能接管。清单（2026-11-17 15:08 实测）：

| 任务 | 频率 | 状态 | 作用 |
|---|---|---|---|
| fb-command-queue-watch | 1 分钟 | 启用 | FB 园区命令队列盯守，群聊命令有人接 |
| fb-command-center-daily-refresh | 每天 09:45 | 启用 | FB 园区每日刷新 |
| fb-competitor-watch | 10 分钟 | 启用 | 同行监控猎手（Victoria 线） |
| fb-dm-thread-watch | 5 分钟 | 启用 | 私信线程盯回复（Anne/Judi 等） |
| fb-lead-scan | 1 小时 | 启用 | 客户雷达（新好友差分、好友请求核查） |
| fb-engage-daily | 24 小时 | 启用 | FB 每日互动养号 |
| fb-warm-am / noon / pm | 每天 10:45 / 14:45 / 18:45 | 启用 | 养号刷视频三场 |
| fb-content-daily | 24 小时 | 停用 | FB 每日内容（旧版，待按 ixBrowser 方案重写） |
| ai-video-publish-2h | 2 小时 | 停用 | AI 面诊视频轮流发布 |
| fb-foxprofile-warm-daily | 每天 15:45 | 停用 | 旧 FoxProfile 养号（方案已删） |
| fb-newpages-post-daily | 每天 18:45 | 停用 | 旧新主页发布（FoxProfile 方案已删） |
| fb-touche-queue-publish(-19/-21) | 每天 17:00/19:00/21:00 | 停用 | Touché 排期发布 |
| ig-gaga-watch / ig-gaga-dm-watch | 10 分钟 / 5 分钟 | 停用 | IG gaga 猎手/私信盯守（待重写启用） |
| ig-sarah-watch / ig-sarah-dm-watch | 10 分钟 / 5 分钟 | 停用 | IG sarah 猎手/私信盯守（待重写启用） |
| ig-haze-watch / ig-haze-dm-watch | 10 分钟 / 5 分钟 | 停用 | IG haze 猎手/私信盯守（号被锁，待恢复） |
| ig-competitor-engage | 3 小时 | 停用 | IG 同行评论区截流 |
| ig-warm-am / noon / pm | 每天 11:45/13:45/15:45 | 停用 | IG 养号三场 |
| ig-matrix-post-r1/r2/r3 | 每天 17:45/19:45/22:45 | 停用 | IG 矩阵发布轮次 |
| ig-matrix-prep-daily | 每天 09:45 | 停用 | IG 每日备料 |
| ig-lead-watch | 30 分钟 | 停用 | TikTok 评论私信巡查 |

10 个号铺开后，每号猎手 + 私信 2 个任务，共 20 个（Jusa/Lark/pokk/elaina + Emerson/38/67/80 共 8 号新建 16 个；gaga/sarah 重写启用 4 个；Victoria 已有自己的、不计）。是否现在建并启用，等老板拍板。

## 10. 不能跟着包走的东西（新电脑上现配）

- 令牌：每台电脑一个独立令牌，`config.json` 必须现生成，绝不复用旧电脑的令牌、绝不共用。
- 登录态：ixBrowser profile 的登录（cookie、账号密码、2FA）不能靠拷文件搬过去；新电脑上每个号要在自己的 profile 里重新登录一次，过 2FA 时号主在自己手机上点批准。
- 代理：旧静态 IP 方案已于 2026-11-17 全部删除（9 条线 + FoxProfile 整目录已进回收站），新电脑不装代理、不走代理。
- 客户数据：leads、dm-threads、group-prospects 等台账不打包；新电脑从零记。
- Muse 侧的东西：定时任务、facebook-cli / instagram-cli 后台发布、话术文件原件、GitHub 记录同步都在 Muse 的 VM 上，不用搬。
- PIN 码：各号聊天 PIN 的对应关系记在工作文件里，不写记忆、不进包；新电脑上按工作文件核对。

## 11. 员工版 v7（给组员/外人用的电脑时用这个）

`agent-v7-restricted-src/` 是受限版源码（已按老板“权限不要给那么多”砍过）：删了 /exec、/files/list、/files/read、/eval、/update；/goto 只限 facebook.com、instagram.com、messenger.com 及子域；/attach 只限包内 uploads/；/upload 只限视频图片。给自己人用的电脑装 v6 全权限版；给组员或外人用的电脑装 v7，并每人一个独立令牌。v7 源码在包里，令牌现生成、不要复用任何已发过的包。

## 12. 常见问题

- 429：只是瞬时限流，短暂退避后重试；不是每日额度，不停查、不等明天、不自己设限。
- profile 显示已开但本机找不到调试地址：先 close 再 open 即可恢复。
- TargetClosedError：多为页面已关，重开重试可过。
- code=2012：窗口云备份中，稍后再试。
- 浏览器崩溃丢登录态：先停浏览器，把 `camoufox_data/<env>/cookies.sqlite.bak` 拷回 `cookies.sqlite` 并删掉 `-wal`/`-shm`，再拉起即恢复（操作前先把当前 cookies.sqlite 备份到一边，勿在浏览器运行时拷）。ixBrowser 环境同理：先关 profile 再动数据文件。
- 每次重新登录都会产生新的 2FA 验证请求，须点最新那条。
- IG 每日限额提示（如 gaga 已用 9 小时 37 分）：会话本身有效，不用重登，等次日。
- 浏览器活由主 agent 直接派发，不派普通子代理（子代理没有实时浏览器控制权限）。
- Bertie 绝不走 browser.browse（默认浏览器 profile 是 Victoria，会把 Bertie 的活做到 Victoria 号上）。Bertie 已于 2026-11-13 退役，任何 Bertie 的发布/派活一律拦下。
- 凭据卫生：密码、cookie、2FA、代理值、令牌不写记忆、不在聊天复述；查环境状态只取 name + is_running，不打印接口原文。

## 13. 硬规则总表（贴墙上）

1. 发布一律走后台（FB 用 facebook-cli 单个视频文件发 Reel、IG 用 instagram-cli 带封面），绝不走浏览器发帖框。
2. 一个视频 = FB + IG 两个平台才算发完；同一账号不发重复视频。
3. 视频 16:00 起发，每条间隔 2 小时，同一轮次各账号错开几分钟。
4. 私信一次只发一条，等回再聊；首条禁直接索号；零报价。
5. 送达必须 Messenger CLI 查到线程且 snippet 为我方消息才算已发。
6. 内容先经 E07 90 分以上 + 总管确认；长内容发布还需老板点头；红线一票否决。
7. 视频先审后排（老板发来的成品视为已批准）。
8. 429 退避重试；226/344 即停该号、核实后不盲重试。
9. 对外文案一律英文；视频文字中英双译；跟老板沟通用中文。
10. 汇报只说重点和结果、不讲过程；只报问题，没问题不报。
11. 总管只派活不亲自干活（facebook-cli 发布与核验除外）；派活以总管 Muse 身份发、不借老板名义。
12. 浏览器操作默认后台跑，不打开给人看；只有老板说要看时才打开。
13. 令牌一机一个，绝不共用；登录态现登，不拷文件。

---
手册完。源码与话术原文在各子目录里，照单装就行；装好把新电脑 Tailscale IP + 新令牌发给 Muse 登记。
