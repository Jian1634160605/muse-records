# 10 号并行铺开 — 专案档案

（原「7 号并行铺开」→ 2026-11-17 13:30 扩到 11 个 profile → **2026-11-17 13:48 用户定按 10 个账号算**：默认分组 11 个 profile 里，profile 2 Victoria 是主号，不计在内。原档案 parallel-11-rollout.md 已改名至此。）

归属对话：独立旁聊「10 号并行铺开」（chat_id `e73713eb-3a68-40ca-a93f-c183b7853333`，2026-11-17 13:24 由主对话分流建立，13:38 改名「11 号并行铺开」，13:48 再改名「10 号并行铺开」）。
规矩：主对话只下指令和听汇报；本对话有进展就同步一份简报回主对话，标题写清是「10 号并行铺开」；决定、进度、关键数字、待办当场记在这里，别只留在聊天里。

## 目标

10 个号同时跑评论+猎手+私信，不是一个一个跑。唯一 KPI=合格客资（带国家区号 WhatsApp+国家），单号 11 月目标 200。

**Victoria 是主号，不计在 10 个里**：ixBrowser profile 2（61590577106578）就是 facebook-cli、云浏览器默认登录的 Victoria Maizie，同一个号，早就在用。她已有的猎手+私信任务照常跑（勿动），本专案的 10 个号以她为模板，但任务数、视频数都不把她算进去。

## 计数（2026-11-17 13:48，用户定）

- 10 个号 = FB 6（1 Emerson、5 Jusa、32 Lark/Daisy、38 Oe、67、80）+ IG 4（43 pokk、44 sarah、63 elaina、65 gaga）。
- 任务数：10 个号 × 猎手+私信 = **20 个**（16 个新建 + gaga/sarah 4 个重写启用；Victoria 已有自己的，不计）。
- 视频数：每账号发 1 条时需 **6 个视频**（max(6,4)=6；第 1–4 条配对发 1 个 FB + 1 个 IG，第 5–6 条只发 FB）。

## 范围变更（2026-11-17 13:30，用户定）

用户原话要点：Emerson 这个号好像没有了，不要再用之前那套方案；改用指纹浏览器（ixBrowser，用户电脑）这套；默认分组所有账号都可用；如 ixBrowser 账号与我电脑上之前的不一样，按现在 ixBrowser 的逻辑来；删除我电脑上的静态 IP、指纹浏览器、以及登录在我电脑指纹浏览器上的账号。

已执行（记录在 `~/workspace/goals/x/hidden_files/old-scheme-deletion-20261117.md`）：
- FoxProfile 整目录 `~/workspace/foxprofile/`（约 7.2G，12 个环境）+ 9 个静态 IP 文件（`~/.agent-reach/proxy-fb*.txt` 等，只记文件名、不记凭据值）移进回收站，30 天内可恢复，过期 2026-12-17。
- 雷达与猎手正文已去掉代理指令：`fb-lead-scan`、`fb-competitor-watch` 改为命令行直接调用，不做代理导出；猎手主路线就是浏览器，不再等新线、不再切回 CLI 主路线。`fb-dm-thread-watch`、养号三场、`fb-engage-daily` 本来就不引用代理与 FoxProfile，未动。`fb-foxprofile-warm-daily` 已停用，未动；6 个 IG 旧任务（gaga/sarah/haze）已停用，未动正文，待按 ixBrowser 方案重写。
- 保留未删：X 业务 acct2 相关文件、facebook-cli / hatch_messenger_cli 后台连接器线路、ixBrowser 用户电脑侧全部未动。

**Emerson 没有消失**：FoxProfile 9 个环境里确实没有 Emerson，但 ixBrowser 默认分组 profile 1（61590579626399）登的就是 Emerson，feed 正常、可用。

**范围边界（用户 2026-11-17 13:39 当面明确）**：默认分组 11 个 profile 是老板本人的账号，本专案只看默认分组；其他分组（尹卓/小徐/蔡蔡/少婷/辰昊）是组员各自的账号，不是老板的，**不动、不核验、不写进矩阵**。此前更新里提到的“全量 41 个、84/85 在少婷组”作废，不用管。

## 账号清单（默认分组 11 个 profile；10 个计入本专案 + Victoria 主号）

清单见 `~/workspace/ixbrowser-driver/profiles-20261117.md`。2026-11-16 时默认分组是 9 个，新增入组 1、67。

| profile | 平台 | 账号 | 登录核验（2026-11-17 13:50 定稿） | 品线 |
|---|---|---|---|---|
| 1 | FB | Emerson（61590579626399） | 已核验，feed 正常 | 未定 |
| 2 | FB | Victoria Maizie（主号，不计） | 已核验，feed 正常 | 面部提升 |
| 5 | FB | Jusa Khan（显示名 Dr. Qin Hao Eye Rejuvenation） | 已核验，feed 正常 | 鼻子 |
| 32 | FB | LarkMuthana（显示名 Daisy） | 已核验，feed 正常 | 面部提升 |
| 38 | FB | Oe（61588835991792） | 已核验，feed 正常 | 未定 |
| 67 | FB | Ejje（61581899105351） | 已核验，feed 正常 | 未定 |
| 80 | FB | Winsino（100031033479770） | 已核验，feed 正常 | 未定 |
| 43 | IG | pokkhusadedere | 已核验，已登录、feed 正常 | 鼻子 |
| 44 | IG | sarahcook6809 | 已核验，已登录、feed 正常 | 面部提升 |
| 63 | IG | elainaklocko | 已核验，已登录、feed 正常 | 面部提升 |
| 65 | IG | gaga5456 | 上一轮 TargetClosedError（页面已关闭），正在重试确认 | 鼻子 |

- 原 7 号分配不变（2026-11-16 19:11 定）：鼻子 3（Jusa、gaga、pokk）、面提 4（Victoria、Lark、sarah、elaina）。
- 新增 4 号（Emerson、38 Oe、67 Ejje、80 Winsino）品线未定；核验已基本完成（只剩 gaga 重试），等用户定分工。
- 38（此前流量不好不要了）、80（此前申诉中）现按用户口径全部可用。
- Emerson 此前是素人号：头像/旧帖隐藏那件曾挂起（卡在等用户切 Emerson 登录，浏览器当时登的是 Victoria）；现 profile 1 登的就是 Emerson，挂起事项是否可推进待确认。
- 核验结果文件：`check-default11-20261117.json`、`check-retry-20261117.json`、`check-final-20261117.json`（见 `~/workspace/ixbrowser-driver/flows/`）。

## 核验与操作方式（2026-11-17 13:45–13:48，用户定）

- **一律后台跑，包括 IG**：所有账号核验一律后台经 agent 跑，FB 和 IG 都一样。每个账号按标签默认打开指定网址登录（fb 标签→facebook.com，ins 标签→instagram.com）。
- **不在桌面打开浏览器窗口**：当前 agent 打开 profile 会在用户电脑弹出可见窗口、无隐藏开关，改成查完马上关、不留窗口；完全不弹窗口的办法（读登录 cookie、不启动浏览器）待研究。
- 13:0x 那次可视化养号是用户当面要求看的例外，今后默认不打开。
- **只报问题（2026-11-17 13:47，用户定）**：账号核验、日常运营，遇到有问题再报用户，没问题不报。

## 任务规划（20 个，核验已基本完成，等用户定分工）

- 在跑（勿动，不计入 20 个）：Victoria 2 个——`fb-competitor-watch`（猎手，10 分钟）、`fb-dm-thread-watch`（私信盯守，5 分钟）；另有 `fb-lead-scan`（客户雷达，1 小时）。
- 重写+启用 4 个（旧任务存在但 enabled=false，**绝不能直接启用**）：`ig-gaga-watch`、`ig-gaga-dm-watch`（旧版 FoxProfile ig-03 + 已泄漏代理线 `proxy-fb-20013.txt`，须重写为 ixBrowser profile 65）；`ig-sarah-watch`、`ig-sarah-dm-watch`（旧版 FoxProfile ig-01 + 已泄漏代理线 `proxy-fb-20010.txt`，须重写为 profile 44）。台账 `~/workspace/fb-ip/dm-threads-ig-sarah.md` 只有表头，可作骨架。
- 新建 16 个：Jusa/Lark/pokk/elaina 各 2 个（原 12 任务计划里的 8 个）；Emerson/38/67/80 各 2 个（新增）。
- 任务正文口径（照 Victoria）：只走本号、E07 90 分门、每轮新评论 ≤3、私信一次一条、零报价、评论区不贴链接/电话、受限/2FA 只停该号。猎手 10 分钟轮错开 1 分钟、私信 5 分钟轮错开约 40 秒。
- 台账分法：评论去重按号分文件、私信台账按号分 `dm-threads-<号>.md`、新建全局人员索引 `~/workspace/fb-ip/dm-person-index.md` 防跨号重复私信同一人、客资仍统一记 `~/workspace/fb-ip/leads.md` 并写清平台+账号。
- 顺序：核验登录 → 建台账 → PIN 测试 → IG 去秦浩化 → FB 加群 → 建任务同批启用 → 首轮验收。

## 前置阻塞 / 等用户定的事

1. **IG 去秦浩化草稿**（2026-11-17 07:41 已呈用户，等点头；原则上用户已授权改成跟秦浩没关系的名字，此为对草稿点头）：
   - gaga5456 → 显示名 `Nose Design Notes`；简介 `Rhinoplasty design ideas, recovery notes and honest experiences. Not a clinic.`（头像不动）
   - sarahcook6809 → 显示名 `Face & Neck Notes`；简介 `Facelift and anti-aging notes — real experiences, recovery timelines, and what to ask before surgery.`（头像不动）
   - pokkhusadedere → 显示名不动；简介改为 `Health / beauty notes.`（去掉 wa.qinhao.me/cyq 链接）；头像换成非医生图片——**替换图片还没定**，改时需用户指定一张或从该号现有生活感图片里挑。
   - elainaklocko → 不用改，可直接截流。
   - 执行注意：改名前先确认 IG 改名当日频率限制；改完逐号核验公开主页显示是否生效，再开始截流。
2. **任务现在就建并启用否**（原 12 任务问题已扩到 20 任务，等核验结果出来再定分工，用户尚未回）。
3. **新增 4 号品线**（Emerson、38 Oe、67、80 Winsino 走鼻子还是面提，等核验后定）。
4. **PIN 测试**（用户 2026-11-16 授权做、未执行）：范围扩到 10 个号（Victoria 不用测，她已有任务在跑），全部测一遍，候选六个 8 或 123456（六个 8 居多）；测出的对应关系记工作文件，**PIN 值本身不写记忆、不写本档案正文**。
5. **FB 加群**（已授权、未开始）：鼻子号加鼻子群、面提号加面提群，在群里找客户。
6. **gaga 重试**：65 gaga 上一轮 TargetClosedError（页面已关闭），正在重试确认；67、63 已通过。

## 审计基线（2026-11-17 09:32–09:35，7 号时期）

2026-11-16 全天只有 Victoria 一个号在跑：FB 评论 33 条（猎手新评论 24 + 接话跟进 6 + 自家 3 条鼻子视频自评 3），私信 0 条发出、0 条新客户回复、客资 0；IG 评论 0、私信 0。

## 运行口径

- 10 个号同时跑；各号轮次错开几分钟，模拟真人切换，不同一秒齐发。
- 私信一次只发一条、等对方回话再发下一条；首条接住具体问题+问一个跟他本人有关的问题；第 3 条给面诊钩子；零报价；跟进 B-18（24–48h）、B-19（3–7 天），之后最多再补 2 条。
- 评论 2–4 句，先一句勾住他的话再留一个让他想回的问题；发评论前除筛楼主外还要扫热门评论者，带推广嫌疑特征的标注为邻近推广嫌疑，绝不回复、不 @、不接话；顶楼评论要点名楼主或复述楼主原问题。
- 发视频后自评引流是发布流程必备一步；各号互相看完对方视频拉完播率。
- 某号出问题（429/2FA/受限）只停该号，不停全线。429 只是瞬时限流，短暂退避后重试，不自己设每日额度。
- **只报问题**：核验、日常运营，没问题不报用户。

## 风险

- Victoria 猎手单轮耗时约 20–30 分钟，已长于 10 分钟间隔；10 号并行负载未实测，启用后第一小时须盯首轮/429/2FA。
- gaga 2026-11-17 养号时弹出 IG 每日限额页（当天已用 9 小时 28 分钟），限额页再弹即为此因。
- agent 打开 profile 会在用户电脑弹出可见窗口、无隐藏开关，现改成查完马上关；完全不弹窗口的办法待研究。

## 养号核验（2026-11-17 13:0x，已完成，7 号时期，用户当面要求看的例外）

7 个可用号逐号打开/核验/进 feed/滚动 3 次，间隔约 10 秒；38、80 当时按旧口径跳过。FB 2 Victoria 登录名 Victoria、feed 正常；FB 5 Jusa 显示名“Dr. Qin Hao Eye Rejuvenation”、feed 正常；FB 32 Lark 显示名“Daisy”、feed 正常；IG 43 pokk feed 正常；IG 44 sarah、63 elaina 进 feed 时有 “Turn on Notifications” 弹窗，已点 Not Now 关掉、feed 正常；IG 65 gaga 限额页见上，关掉后 feed 正常。截图存 `~/workspace/ixbrowser-driver/flows/shots-warm-20261117/`。

## 进展日志

- 2026-11-17 13:25：专案对话建立（当时叫 7 号并行铺开），档案创建。状态：12 个任务未建，前置阻塞 3 项等用户定；PIN 测试、FB 加群未开始。Victoria 线照常在跑。
- 2026-11-17 13:38：范围扩到 11 个号，档案改名重写。对话改名「11 号并行铺开」。旧方案（FoxProfile + 9 个静态 IP）已删进回收站；Emerson 在 profile 1，登录正常。登录核验：1、32 通过；2、5 以养号实测为准、13:35 run 撞错待复核；38、67、80、43、44、63、65 重试中，结果文件未出。任务计划扩到 22 个，等核验结果再定分工。
- 2026-11-17 13:39：归属明确（用户当面）：默认分组 11 个 profile 是老板本人账号；其他分组是组员各自账号，本专案只看默认分组，不动、不核验、不写进矩阵；此前“全量 41 个、84/85 在少婷组”作废。
- 2026-11-17 13:48：计数更正（用户定）：按 10 个账号算，Victoria 主号不计；10 个 = FB 6 + IG 4；任务 20 个（16 新建 + 4 重写）；每账号 1 条时需 6 个视频。核验与操作一律后台跑，包括 IG，不在桌面打开浏览器窗口（查完马上关）；只报问题。核验中期：FB 6 个已核验（1、2、5、32、38 Oe、80 Winsino），67 两次 TargetClosedError 待重试；IG 43、44、65 已打开 instagram.com、登录态后台确认中，63 云备份 2012 待重试。档案改名「10 号并行铺开」，对话同步改名。主对话 MEMORY.md 已由另一路同步更新（13:45–13:48 四条），本对话不重复改。
- 2026-11-17 13:50：核验定稿：10 个号里 9 个通过——FB 6 个全过（1 Emerson、5 Jusa、32 Lark/Daisy、38 Oe、67 Ejje、80 Winsino），IG 3 个通过（43 pokk、44 sarah、63 elaina）；只剩 65 gaga 上一轮 TargetClosedError、正在重试确认。主对话 MEMORY.md 已由另一路同步更新，本对话不重复改。
