---
id: ig-matrix-prep-daily
title: 每日备料（选3条+差异版+FB文案）
enabled: true
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 09:45:00
timeout_secs: 3600
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
为 Facebook（个人号 Victoria Maizie）准备今天的 3 条起号视频。（2026-10-21 用户决定：IG 线已放弃——lillieflores24 不再运营；TikTok @faciallifting.qinhao 已交同事运营，本任务不得再碰 TikTok——不发布、不巡查、不读它的数据。下方 IG 源账号仅作选源读取，属内部复用。）

**选源优先级（2026-10-21 用户定）**：① **@internationalplasticsurgery916**（Dr. Lanlan，用户指定优先源，她的内容优先用）② @tan.iasampson（公司矩阵账号）。两个源共用同一本已用台账 used.txt，跨源不重复。

（队列目录沿用 ~/workspace/ig-ops/christycrawford85/queue/ 路径不改。）

**选片前置（2026-10-24 新增，必读）**：选片前先读 ~/workspace/ig-ops/christycrawford85/source-pool-2026-10-23.md 末尾的筛片结论与 ~/workspace/goals/x/hidden_files/showcase-fresh-slice-2026-10-24.md 的"今日候选/拉黑"记录，以及 src-2026-10-23 目录内的同人核验记录。**tan.iasampson "Dr.QinHao" 标题模板批（特征：大字 "IS SHE VERY DIFFERENT NOW?" / "SEE THE DIFFERENCE" / "POST-OP DAY 10"，含 ig-fastdl-14/15/17）= 疑似批量假对比，已拉黑，绝不选用**——此批 2026-10-24 已出过成品误发事件（备料成品被整批作废）。@reface_scarless 与 @yefacialdesign 只学结构、绝不下载使用。

**步骤 0：复盘昨天 FB 数据 + 受众核对（必做，先于一切，2026-10-21 用户新规）**
先查昨天 FB 已发视频的表现，再决定今天发什么：
- 数据来源：FB（Victoria Maizie）昨日各帖的播放量、点赞、评论（链接见各日 queue/posted.txt）。逐条记入台账 ~/workspace/ig-ops/christycrawford85/perf-log.md（日期/平台/链接/内容类型/播放/点赞/评论）。
- 内容类型按画面主题归类，如：恢复时间线（Day X 对比）、术前术后强对比、拆线/恢复日常、患者旅程叙事等。
- **受众核对（2026-10-21 用户总纲）**：看 FB 受众反应——哪个国家的受众互动多、哪种内容角度更吃香、评论区语言分布；记入 perf-log。目标排序：①客资 ②播放 ③涨粉。播放量持续差必须主动改（换型/换钩子/换时段），不要等用户催。
- 决策规则：(a) 昨天播放最高的类型，今天优先用同类型换新案例放大；(b) 昨天垫底的类型今天降权（以播放量为主指标）；(c) 某类型连续两天垫底 → 明确换型，并在报告中说明换型理由；(d) 数据读不到（页面异常等）就注明"未读到"，绝不编造数据。
- 复盘结论写进当天报告，并作为下面选片的依据。

**防覆盖检查（在复盘之后）**：若 ~/workspace/ig-ops/christycrawford85/queue/<今天日期>/ 已存在且里面有 v1.mp4、v2.mp4、v3.mp4 和 captions.md，说明今天的料已提前备好——不要覆盖、不要重复选片；报告里带上步骤 0 的复盘结论，并说明今日队列的类型与复盘结论是否一致，然后结束。

备料步骤（队列未就绪时）：
1. 按选源优先级读取两个源账号的 Reels 播放量与链接（打开源账号公开 /reels/ 页读取；IG 已无登录会话，若页面要求登录读不到，就用台账已知的高播放条目顺延选片，并在报告中注明源数据未读到）；读取台账 ~/workspace/ig-ops/christycrawford85/used.txt，挑播放量最高且未用过的 3 条（优先从 ① 号源里挑，不足再从 ② 补），选片类型服从步骤 0 的复盘结论。若未用过的不足 3 条，就用播放量最高的旧条目重新做差异版，并在报告中注明是复用。
   **选片质量硬标准（2026-10-21 用户验收教训，不合格播放量再高也不选）**：必须是单人单案例（同一患者贯穿全片）；画面与片内文案一致（文案问女性画面不能是男性）；横幅/标题文字完整不出框；禁止上下拼盘跳人、禁止多患者拼接。源片本身拼盘的直接淘汰。
   **916 源水印规则**：该源视频带其自有水印（"Dr. Lan"签名、诊所横幅、防盗字）。优先选水印位于画面边缘的条目；画面中央有大签名/大横幅遮挡主体的跳过；做差异版裁切时尽量把边缘水印裁出画面。
2. 用 https://zh.savefrom.net/132Vh/download-from-instagram 贴链接下载这 3 条视频（失败则用浏览器下载兜底，再失败就报告并跳过该条、顺延下一条）。
3. 用 ffmpeg 给每条做画面差异版（参数在 3 条之间各不相同）：变速 0.96–1.04 倍、裁切放大 101%–105%、轻微调色（饱和/对比/亮度微调）、顶部居中加水印 drawtext 'Dr. Qin Hao · Shanghai Facelift'（DejaVuSans-Bold，白色 85% 不透明，带阴影，y=54，fontsize=30）、H.264 CRF18 重编码、去掉元数据。注意：咱们的水印不要压住源片画面内的标题文字（位置冲突时把水印改放 y=54 以下避开或微调）。这一步只处理画面，音频在下一步统一换轨。
4. **换音乐（2026-10-20 用户新规，必做）**：先用 ffmpeg 把 3 条源视频各自的音轨抽出来，存入音乐池 ~/workspace/ig-ops/christycrawford85/music_pool/（文件名带源 Reel 短码，如 DeQ2W0yCUAM.m4a；池子里已有的旧音轨也保留）。然后给 3 个差异版交叉换轨：v1 配第 2 条的音轨、v2 配第 3 条的、v3 配第 1 条的——每个成品的音乐与自身源视频不同、三条之间也互不相同。换轨时音轨做 atempo 对齐视频变速，长度不足循环、过长裁剪，与视频时长对齐，最终输出到 ~/workspace/ig-ops/christycrawford85/queue/<今天日期 YYYY-MM-DD>/v1.mp4、v2.mp4、v3.mp4，必须是画面+音乐都齐的最终成品文件。发布环节直接上传成品，不再进平台曲库找音乐。
5. 写同目录 captions.md：每条视频一节（## V1/V2/V3），只写 FB 版英文文案。FB 版角度 = 信任/专业（医生团队、上海诊所、面诊路径）。共同要求：只围绕拉皮（facelift），第一行强钩子，第二行提问引导评论，带国家词标签（Indonesia/Malaysia/Singapore/Brazil/USA/Philippines/Australia/UK 轮换，每条 8–10 个），咨询引导统一指向 WhatsApp 链接 https://drqh.jianjianmeili.com/vMPEX84o（可带链接文字）。每节另注明本条所配音乐的来源 Reel 短码和素材来源账号。
6. 把用掉的 3 条 Reel 链接追加进 used.txt（注明日期、播放量和来源账号）。
7. 向主聊天报告：昨天的复盘结论（哪类最好/最差、今天如何调整、FB 受众要点）、今天挑了哪 3 条（链接+播放量+来源账号）、各配了哪条的音乐、队列是否就绪。失败也要报告原因，不要静默。

**步骤 8：4 个新主页的每日备料（2026-10-22 用户指令新增，4 个新号正式纳入日常运营）**
矩阵已扩到 7 号 7 主页。除 Victoria 的 3 条外，每天再给下面 4 个新主页各备 1 条，存入 ~/workspace/ig-ops/christycrawford85/queue/<今天日期>/pages/ 子目录，文案写在同目录 pages-captions.md（每主页一节，注明类型 VIDEO 或 TEXT）：
- **fb-73057（Jioklm Dersx）主页「Dr. Qin Hao Facelift & Facial Rejuvenation」61595888184080 — 拉皮主线**：从未用过的源片里再选 1 条拉皮片做差异版（参数与 Victoria 当天 3 条都不同；音乐从池中另选未用过的音轨，先按 MD5 去重再选），成品 pages/p73057.mp4。
- **fb-91565（Jusa Khan）主页「Dr. Qin Hao Eye Rejuvenation」61595765429611 — 眼部年轻化**（双眼皮/提眉/眼袋/上睑）：源片里有眼周/上睑贴合内容的优先做差异版视频 pages/p91565.mp4；没有贴合的，就备 1 条英文科普文字帖（医生口吻、眼部专科角度、强钩子+提问引导评论+WhatsApp 链接 https://drqh.jianjianmeili.com/vMPEX84o），pages-captions.md 标 TEXT 并写好全文。不得拿不贴合的视频硬凑。
- **fb-75128（Simon Dyer）主页「Dr. Qin Hao Rhinoplasty & Nose Reshaping」61595900453604 — 鼻部专科**（隆鼻/鼻修复/鼻线雕/缩鼻翼）：同上规则，有鼻部贴合源片做视频 pages/p75128.mp4，没有就备英文科普文字帖（TEXT）。
- **fb-54124（Cora Gleichner）主页「Dr. Qin Hao Body Contouring」61595343737797 — 身体塑形**（吸脂/脂肪填充/隆胸/植发）：同上规则，有身体塑形贴合源片做视频 pages/p54124.mp4，没有就备英文科普文字帖（TEXT）。
- 4 个主页的文案角度互不重复，与 Victoria 当天文案也不要雷同；红线与主队列一致（不编造患者术后效果、不发标"不能发"的素材、禁用台湾人案例）。
- 复盘补充：次日起把 4 个主页昨日所发帖子的数据（播放/点赞/评论，链接见各日 queue/posted-pages.txt）也记入 perf-log.md（分主页记录）；某主页播放持续差就主动换型/换钩子，报告里说明。
- 报告补充一段：4 个主页今天各备了什么（视频/文字帖、主题、源片链接如有）。

红线：只处理公司自有/用户指定账号内容；不生成、不合成任何虚假的患者术后效果。
