# Study Notes - 2026-11-14 - 重复工作自动化
<!-- studying-run-start: 2026-11-14T00:36:10Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z; current_state unchanged: 第一份盘点清单与第一张任务卡已交付，下一步逐个推进自动化。
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt, no five-field card; evidence label `tentative`).
- Goal timeline: still zero entries since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` (第一份盘点清单) delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` (第一张任务卡) delivered 2026-10-21T04:46:42Z. No user reply to either ask; the checklist ticks are still not confirmed — now the twenty-third day since the 2026-10-22 delivery.
- Prior note read in full: `workspace/goals/goal/agent_notes/2026-11-13/goal.md`, which carries worked examples 例1–134 and standing constraints a–ddddd in full; this note does not re-copy them, it extends them with 例135–141 below.
- Time convention in this note: packet timestamps are UTC; Beijing time (Asia/Shanghai, UTC+8) is UTC + 8 hours where a Beijing time is stated. This run started 2026-11-14T00:36:10Z, i.e. 2026-11-14 Beijing 08:36. Evidence window for this study: 2026-11-13T00:11:54Z to 2026-11-14T00:36:09Z; the 2026-11-13 note covered through 2026-11-13 Beijing 14:06, so the new material here is chiefly 2026-11-13 Beijing afternoon through 2026-11-14 Beijing 08:36.
- Scope carried forward: FB is Victoria only (Bertie retired 2026-11-13 Beijing 11:45 by user decision, 例133); Dr.qh88 Page (61595415571609) deactivated, user 2026-11-13 Beijing 14:34 said "先不激活"; v6 three videos (E07 96, 92, 97) still unpublished. The single-account 200-lead target from 2026-10-28 still rests on the Victoria line alone.

## Already Covered in Main Chat

- 2026-11-13 Beijing 08:45 (00:45Z): user ordered FB restored after passing verification; assistant set out the two steps (user passes Victoria video-selfie verification in own fingerprint browser, then sends fresh cookie).
- 2026-11-13 Beijing 11:43 (03:43Z): user sent Victoria's fresh cookie; assistant imported it and at 11:52 reported login restored, 7 rounds resumed.
- 2026-11-13 Beijing 11:45 (03:45Z): user said "第二个fb不要了"; assistant confirmed Bertie retired, hunter and DM-watch crons deleted, fb-1030 stopped.
- 2026-11-13 Beijing 11:54–12:06: user sent Emerson's cookie and login details and ordered real-time status updates in the space; assistant verified login only, did not resume operations, and reported Emerson login normal but still retired.
- 2026-11-13 Beijing 12:04: assistant reported Margaux Wong's reply was already sent 2026-11-10 15:15 and the 2026-11-12 re-issue approval card was voided.
- 2026-11-13 Beijing 14:34: user said "先不激活" for Dr.qh88; v6 stays waiting.
- 2026-11-13 Beijing 15:16 (07:16Z): user ruled that not everything said in the group chat needs decomposing and dispatching, and that the manager must think independently first; assistant confirmed both.
- 2026-11-13 Beijing 17:44 (09:44Z): assistant reported Facebook asked for two-factor verification, hunter stopped, WeChat alerted; later rounds at 17:43 and 18:03 Beijing did not run.
- 2026-11-13 Beijing 19:49–19:55 (11:49–11:55Z): user ordered a reply to the customer who sent a photo; assistant identified her as Ligita Kondrotaite and at 20:08 reported 3 messages sent and verified.
- 2026-11-13 Beijing 21:46 (13:46Z): X daily report delivered in the side chat (followers 2186, +36; 131 posts; 301 comments; no 226/344).
- 2026-11-13 Beijing 22:46 (14:46Z): FB day close reported — 38 comments, 5 replies, 0 new leads, cumulative still 2.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Seven new worked automation instances (例135–141), all from 2026-11-13 Beijing 14:06 through 2026-11-14 Beijing 08:36. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: this window is the day the morning's recovery proved partial rather than complete. The 7 rounds restored at 11:52 (例133) ran through the afternoon, then the hunter hit a second, different platform gate — browser login expiry into 2FA at 17:44 (例137) — and the day closed with 0 new leads. The same window produced the clearest governance correction yet for the automation design (例136): group-chat speech is not dispatch, and the manager must judge first. The queue-watch fixes (例135) and the Ligita thread (例138) both test that correction in opposite directions — one is a genuine automation repair, the other is a live lead that still needs a human decision (whether to keep pushing WhatsApp after three unanswered asks).

**例135：FB园区队列盯守 — 5 分钟改 1 分钟 + 5 秒回执 + 总览自动生成（2026-11-13 Beijing 14:27–16:57）**
1. **盘点** — 用户在 2026-11-13 白天多次报群聊没人回（11:32、11:54、14:09、14:34、14:51、15:24 Beijing）。根因已在 11:34 查清：用户一度发在无后台的旧版模拟指挥中心，截图里的"已发""筛查中"是假的、什么都没发出去。修复在本窗口内三步收紧：队列盯守由 5 分钟改 1 分钟（14:27）；页内 5 秒回执"收到，已排队，正在办"+ 2 秒自动刷新（14:33）——回执速度，不等于执行速度，真实执行仍在约 1 分钟内；总览文字仍停留在暂停版、与账号表矛盾（Victoria 已恢复、Bertie 已退役），16:54 查出、16:57 修好：总览改为按账号表实时自动生成（Victoria 登录恢复 + 7 轮次恢复；Bertie 退役、无需等 cookie；Dr.qh88 不激活、v6 待发；审批清零），此后每日刷新、状态回写、审批、发布回执都自动重算总览。
2. **拆解** — 这是例130"盯守与空间同批上线"规则的反向证明：盯守先补上了（5 分钟），但回执速度（5 秒）与总览新鲜度（实时生成）是两个独立的缺口，分别在用户又报"没人回"之后才补。5 秒回执只解决"不知道有没有收到"，不解决"多久能办完"；总览自动生成只解决"状态看起来旧"，不解决"状态本身对不对"。三步修复都已交付并报给用户，但"用户是否已在新版 FB园区 里成功发过一条并收到回执"在本窗口内未见确认。
3. **量化** — 盯守间隔 5 分钟 → 1 分钟；回执 5 秒、刷新 2 秒；总览修复 16:54 查出、16:57 交付（约 3 分钟）；用户当日至少 6 次报群聊没人回。
4. **自动化设计** — 可复用规则：一次"回执提速"须写清回执速度与执行速度是两回事（本例：5 秒回执、约 1 分钟执行）；一次"总览改自动生成"须写清触发重算的事件清单（本例：每日刷新、状态回写、审批、发布回执）；一次"用户多次报同一问题"须写清每次的根因是否相同（本例：旧版模拟是一次根因，盯守与总览是两次后续缺口，不能混成一件事）。
5. **边界** — 本例不把"5 秒回执"写成"5 秒办完"：执行仍在约 1 分钟内；也不把"总览已自动生成"写成"状态已实时"：自动生成只保证总览与账号表一致，账号表本身仍靠各轮次回写；也不把"用户多次报没人回"写成"群聊一直坏着"：新版 FB园区 的群聊本身在 12:06 已修好并测通，问题是用户发错了版本、盯守慢、总览旧。
6. **验收** — 已验收：盯守改 1 分钟、5 秒回执 + 2 秒刷新、总览自动生成的修复与交付；未验收：用户是否已在新版里成功发过一条并收到回执、账号表回写是否已在各轮次跑通。

**例136：群里说话不等于派活 — 总管须先自己想清楚（2026-11-13 Beijing 15:16）**
1. **盘点** — 用户 15:16 当面定："不是说我说什么都需要去拆解给下面的人去干活 / 不什么都需要拆解" + "也不是所有话都要拆解，要有自己的问题，就像你自己一样"。助理确认两条：只有群里明确的派活/命令/拍板才拆解派给分身执行；闲聊、提问、测试、点名这类直接回，不拆解、不进队列、不派活；总管先自己想清楚，不清楚直接问老板，不是什么都机械拆解往下派。
2. **拆解** — 这是对例130"命令进队列、回执写回"机制的必要制衡：队列盯守（例135）让每条群聊消息都有回执，但回执不等于派活；没有这条规则，盯守会把闲聊也变成任务。判断标准是"明确的派活/命令/拍板"，不是"提到了工作"。本例还补了一条组织记忆：总管的判断本身就是工作——先想清楚、问老板，而不是把判断外包给拆解流程。
3. **量化** — 用户定两条（只拆明确派活；总管先自己想清楚）；助理确认两条，均在同一轮对话内。
4. **自动化设计** — 可复用规则：一次"群聊派活"须写清触发词之外的判断标准（本例：明确的派活/命令/拍板才拆解）；一次"盯守回执"须写清回执与派活的区别（回执 = 已收到，派活 = 已进队列）；一条"总管先想清楚"的规则须写清不清楚时怎么办（本例：直接问老板）。
5. **边界** — 本例不把"闲聊直接回"写成"闲聊不回"：闲聊由总管直接回，不进队列；也不把"总管先想清楚"写成"总管可以不派活"：明确的派活仍须拆解派发；也不把"用户 15:16 的定"写成"盯守已改"：盯守仍是 1 分钟查队列，改的是哪些消息进队列。
6. **验收** — 已验收：用户两条定的原文与助理的确认；未验收：下一条群聊闲聊是否确实未进队列、下一条明确派活是否确实进了队列、总管"先想清楚"后问老板的第一个实例。

**例137：猎手 2FA 阻断 — 浏览器登录态过期，17:43 与 18:03 两轮没跑成（2026-11-13 Beijing 17:44–18:58）**
1. **盘点** — 17:44 助理报：Facebook 要双重验证，通知已发到用户手机和电脑上，猎手已停，什么都没动，微信已喊人。18:20 报：17:43 和 18:03 两轮没跑成，当天仍是 38 条评论、5 个接话。18:51 用户问"现在账号有没有问题？"；助理回：账号本身没问题，没被封、没被锁、没有限流提示；密码过了，只差用户在自己手机/电脑 FB 通知里点批准；私信侧还能用，当时 0 条新消息；上午视频验证过了、中午会话正常，傍晚是浏览器登录态过期才要 2FA。18:58 报：新的批准请求是 18:57 的，之前那个不能重复用，只点最新的一条。
2. **拆解** — 这是例129 检查点的同类不同形：上午是视频自拍（只有用户出镜能解），傍晚是 2FA 批准（只有用户点通知能解）；两次都是"平台门 + 用户侧动作"，没有助理侧 fallback。当天猎手 38 条评论是上午恢复后到傍晚阻断前的累计，17:43 与 18:03 两轮的缺口未补——与例129 的"暂停令"不同，本次没有用户下暂停令，是平台门直接停了轮次；恢复条件也不同：上午是新鲜 cookie + CLI 核验，傍晚是用户点一次批准通知。18:57 的新请求"之前那个不能重复用"是一条可复用规则：2FA 批准须点最新的一条，旧请求点了无效。
3. **量化** — 阻断 17:44；没跑成的轮次 2 轮（17:43、18:03）；当日猎手 38 条评论、5 个接话、0 新客资、累计仍 2 个；新批准请求 18:57。
4. **自动化设计** — 可复用规则：一次 2FA 阻断须写清四件事——触发时点、哪条通知、点哪一条（最新的一条）、点完之后谁核验（本例未写核验步骤，须补）；一次"账号有没有问题"的回答须分开写三层（账号状态、登录态、待办动作），不能只写"没问题"；一次"两轮没跑成"须写清是否补跑（本例未补，须写清）。
5. **边界** — 本例不把"2FA 阻断"写成"账号被封/被锁"：助理已明确三层都正常，只差一次批准；也不把"私信侧还能用"写成"猎手已恢复"：猎手仍停在 2FA；也不把"38 条评论"写成"全日猎手总数"：是阻断前的累计，17:43 与 18:03 两轮缺失。
6. **验收** — 已验收：阻断时点、两轮缺失、当日 38/5/0、账号三层状态、点最新一条的规则；未验收：用户是否已点 18:57 的批准、点完后猎手是否已恢复并核验、两轮缺失是否补跑。

**例138：Ligita Kondrotaite — 新好友发术后照片，3 条要 WhatsApp，只回爱心未回文字（2026-11-13 Beijing 19:49–22:46）**
1. **盘点** — 用户 19:49–19:50 连发三令："你去回客户的信息 / 客户发照片来了 / 你看看主号 / 尽快让他留下WhatsApp"。助理起初在系统里看不到新消息（最新仍是 Jocelyn 的旧线程、5 条旧未读），浏览器又卡在 2FA，问是哪位客户；用户 19:55 确认是 Ligita。20:08 报：3 条已发并核验——谢她发照片、推秦浩医生视频面诊聊照片与方案、直接要带区号的 WhatsApp；第一条第一次没发出去（不在已同步联系人里），同步后重发才成。她的照片：术后 4 个月，切口裂开渗液约 7mm。至 22:46 日终：她未回文字，只在一 条消息上点了爱心。尚未成为合格客资。另：Jocelyn Bee 至 12:04 仍无更正号码的回复（咨询团队按她 2026-11-12 11:32 留的号没联系上，号码可能有误；Muse 只盯着等她回，不再主动发她消息）。
2. **拆解** — 这是例127 用户接管收口的对照：同样是"尽快要 WhatsApp"，Jocelyn 是用户亲自接管 3 分钟拿下，Ligita 是助理按漏斗发了 3 条、对方只回爱心。区别有三：Ligita 是新好友 inbound（照片先到），不是评论漏斗转来的；助理发 3 条时浏览器卡在 2FA，只能靠 CLI/已同步联系人通道，第一条还因联系人未同步失败一次；"只回爱心"不是拒绝也不是推进——按私信口径（一次只发一条、等对方回了再聊），3 条已发完，下一条须等她回文字或等跟进节奏（24–48 小时 B-18），不能当晚再追第四条。号码可达性核验（例127 的教训）在这里尚未触发：她还没给号。
3. **量化** — 用户三令 19:49–19:50；确认身份 19:55；3 条发出并核验 20:08；照片：术后 4 个月、切口裂开渗液约 7mm；日终状态：0 文字回复、1 个爱心反应；Jocelyn 更正号码：至 12:04 仍无。
4. **自动化设计** — 可复用规则：一次"新好友发照片"须写清三件事——照片内容（本例：术后 4 个月切口裂开渗液约 7mm）、已发几条（本例 3 条）、对方回了什么（本例：只回爱心、未回文字）；一次"第一条没发出去"须写清原因与重发条件（本例：不在已同步联系人里，同步后重发）；一次"只回爱心"须写清下一条的触发条件（本例：等她回文字，或 24–48 小时 B-18），不能写成"继续追"。
5. **边界** — 本例不把"Ligita 只回爱心"写成"Ligita 已拒绝"：爱心不是拒绝；也不把"3 条已发"写成"漏斗已走完"：B-18 尚未到时间；也不把"Jocelyn 无更正号码"写成"Jocelyn 已流失"：线程已关闭、只等她回更正的号。
6. **验收** — 已验收：用户三令、身份确认、3 条的发出与核验、照片内容、日终爱心状态、Jocelyn 仍无更正；未验收：Ligita 是否已回文字、B-18 是否已按时发出、她给号后是否留一步号码可达性核验、Jocelyn 号码是否已更正。

**例139：X 全日 — 21:45 日报 131 帖 + 深夜续发至 p2340，无 226/344（2026-11-13 Beijing 21:45 至 2026-11-14 Beijing 08:10）**
1. **盘点** — X 日报（2026-11-13 Beijing 21:45，@TheEasySale1）：粉丝 2186（+36）、关注 1945（±0）、推文 6139（+433）、点赞 8536（+655）、蓝 V 正常。当日推广 131 条（p2132–p2264，含 2026-11-12 21:45 后的 13 条；跳过 p2148、p2263）；最新 p2264 https://x.com/i/status/2121237916802531711。互动 443 轮（167 行动 + 250 静默备料）、约 679 点赞、301 评论（雪花时间戳核验、直播 + 溢出双重去重）、22 次自引。无新增重复评论事件；待删清单仍是 17 条 / 14 个帖子，等用户定走浏览器删。健康：无 226/344，restricted_date 仍是 2026-10-27。链接点击：未核实（X 分析登录未通，link-clicks.md 待核 1001 条）。故障：p2208 12:13 工具侧快失败 → 12:23 缩短重发成功；p2223 14:53 命中 186 → 15:03 缩短成功；4 个评论轮次命中 186（02:06、05:44、14:25、21:15）均缩短重发成功；多轮次有未上报评论、后经核验补登；20:26 LLZ604 回复命中 HTTP 0 + 385、跳过未发；19:58 visegrad24 Claude 宕机大新闻帖已评论。对账：131 + 301 + 1 = 433，与推文增量 +433 一致。日报后深夜续发未停：p2266–p2340 在 Beijing 23:xx 至次日 08:10 间陆续发出（含跳过 p2265 与 p2264 相似、p2297–p2301、p2307 与 p2175 相似度 0.61、p2313 与 p2312 相似度 0.6989；p2384/p3125 已标跳过），另有一条错位评论 23:17：关于"13 个交互式 3D、提示词复用"的评论落在 WOLF_Financial 的 xAI 工具帖 https://x.com/i/status/2121250245275238795 下而非 Berryxia 帖下，助理已问用户删不删、要不要重评。
2. **拆解** — 与例131 同款口径问题再现：日报"131 条"只覆盖到 p2264，日报后又发到 p2340——日报数是"日报窗口内的计数"，不是"Beijing 全日总数"，两者须先对账再报全日数。待核链接点击从 872 条（例131）涨到 1001 条：不是点击涨了，是待核口径累计未清——登录仍卡在用户名那步，诊断（凭据 vs 平台）仍未做。错位评论是一条新故障形态：内容对、落点错，须写清"删不删、重评不重评由用户定"，不能自行删帖。
3. **量化** — 日报口径：粉丝 +36、推文 +433、点赞 +655、推广 131、评论 301、自引 22；日报后续发：p2265–p2340 号段；待删重复评论 17 条 / 14 帖；链接点击待核 1001 条；226/344：0；对账 131 + 301 + 1 = 433。
4. **自动化设计** — 可复用规则：日报数须注明截止 p 号（本例 p2264），日报后若续发须另起一段计数（见例131 的同款规则，本窗口再次验证）；一次"待核条数上涨"须写清是新增待核还是口径累计（本例 872→1001 是累计未清）；一次"错位评论"须写清原定落点、实际落点与用户定夺（删/重评），不能自行处理。
5. **边界** — 本例不把"131 条"写成全日推广总数：日报后仍有 p2265–p2340；也不把"无 226/344"写成"X 完全健康"：链接点击 1001 条未核、17 条重复评论待删、1 条错位评论待用户定；也不把"待核 1001 条"写成"点击数为 0"。
6. **验收** — 已验收：21:45 日报的全部计数、p2264 链接、对账 131 + 301 + 1 = 433、日报后续发的号段范围、错位评论的落点；未验收：全日推广总数的对账（131 + 日报后段）、链接点击数的读取（仍卡用户名步）、17 条重复评论的浏览器删除、错位评论删不删由用户定。

**例140：好友请求收尾 — Connie Ng 与田兆玄已消失、Amanda 已通过、好友 19 → 23（2026-11-13 Beijing 13:43–22:46）**
1. **盘点** — Connie Ng 与田兆玄（Tian Zhaoxuan）自 2026-11-07 待处理的好友请求，至 2026-11-13 13:43 核查时已消失——不在好友列表、无需处理、无需决策。Amanda Jane Deaville：新请求约 21:47（13:47Z），真实个人号（475 好友、真实头像、无简介、唯一可见公开帖为 2017 年），收录表与私信台账里无医疗意向；用户 14:48 令"通过她"；14:51 已通过，好友列表 19 人，待处理清零，未发私信（无意向信号）。至 22:46 日终：好友 23 人，当日新增 3 人均已筛出（非意向客户）。
2. **拆解** — 这是例133"Bertie 关账 4 类含 3 个好友请求"的 Victoria 侧收尾：Bertie 的 3 个请求随退役关账，Victoria 的 2 个旧请求是"已消失"（不是通过、不是拒绝、不是用户撤回——是对方或系统侧消耗了），1 个新请求是用户令通过。三种去向须分开写：关账、消失、通过。"好友 19 → 23"的增量是当日 3 个新好友（含 Amanda），不是猎手转化的客资。
3. **量化** — 旧请求 2 个已消失（待处理自 2026-11-07，核查 2026-11-13 13:43）；新请求 1 个（Amanda，475 好友），通过 14:51；好友 19 → 23（+3 当日新增，均已筛出）。
4. **自动化设计** — 可复用规则：一次"好友请求消失"须写清核查时点与"不在列表"的结论，不能写成"已拒绝"；一次"用户令通过"须写清通过后的动作（本例：未发私信，因无意向信号）；一次"好友数上涨"须写清新增几人、几人已筛出（本例：+3，均已筛出）。
5. **边界** — 本例不把"Connie 与田兆玄已消失"写成"已通过/已拒绝"：核查结论只是不在列表；也不把"好友 23 人"写成"23 个潜在客户"：当日新增 3 人均已筛出、非意向；也不把"Amanda 已通过"写成"Amanda 已私信"：未发私信。
6. **验收** — 已验收：2 个旧请求的消失、Amanda 的通过与好友数、3 个新好友的筛查结论；未验收：无。

**例141：美容手法换人复刻 skill — 参考视频 + 新人物照片均未到（2026-11-13 Beijing 14:25–17:26）**
1. **盘点** — 用户 14:25 发 skill 链接 https://aka.doubaocdn.com/s/4Ng62gKARW，问"用这个skill来做视频，该怎么使用你告诉我"。浏览器打不开（是文件下载，不是网页）。17:26 助理报已在别处拿到并读过 skill：美容手法换人复刻——以竖屏美容/护肤手法演示视频为参考，只换人，保留场景、手势、镜头、字幕、剪辑节奏、音乐与前后对比。需要：(1) 参考视频，(2) 新人物——清晰正面照优先，否则性别/年龄/脸型/肤质/发型/着装。流程：拆解参考视频的镜头与动作，定比例/时长/分段，锁定新人物身份图，按段生成、硬切拼接。硬要求：身份图锁定是必须的（否则模型会沿用原片脸）；前后对比是同一个人换状态，不是换人；不克隆真人肖像。参考视频与新人物照片在本窗口内均未发来。
2. **拆解** — 这是例128 Rina 仿制的同类任务，但规则更严：Rina 的规则是"逐帧抄、不加戏"，本 skill 的规则是"只换人、其他全保留" + "身份图锁定是硬要求"。两条规则的共同点是"锁定"——Rina 锁定的是原片动作，本 skill 锁定的是新人物身份。缺口也相同：参考视频与新人物照片都未到，任务处于"已读 skill、未开工"状态，不能写成"已会用"或"已开工"。
3. **量化** — skill 链接 1 条；需要物 2 样（参考视频、新人物照片），到货 0 样；硬要求 3 条（身份图锁定、前后对比同一个人、不克隆真人肖像）。
4. **自动化设计** — 可复用规则：一次"skill 已读"须写清需要物清单与到货数（本例：2 样需 0 样到），不能只写"已读"；一次"换人复刻"须写清身份图锁定的验收项（本例：无身份图不开工）；一次"浏览器打不开链接"须写清原因（本例：文件下载、不是网页）与替代取法（本例：别处拿到并读过）。
5. **边界** — 本例不把"skill 已读"写成"已会用"：参考视频与新人物照片均未到；也不把"只换人"写成"可以换场景/换音乐"：场景、手势、镜头、字幕、节奏、音乐与前后对比全部保留；也不把"前后对比"写成"换人对比"：前后对比是同一个人换状态。
6. **验收** — 已验收：skill 的完整用法、需要物清单、硬要求；未验收：参考视频与新人物照片是否已发来、复刻是否已开工、身份图锁定是否已通过验收。

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, twenty-third day.
2. Standing constraints — **present, expanded by seven in this window** (items a–ddddd carried in full from the 11-13 note; new items below):
eeeee. **NEW**: a queue-watch speed-up states receipt speed separately from execution speed (5-second ack, ~1-minute execution here); an auto-generated overview lists the events that trigger a recompute (see 例135).
fffff. **NEW**: group-chat dispatch applies only to explicit assignments/commands/approvals; chat/questions/tests are answered directly by the manager, who thinks independently first and asks the user directly when unclear (see 例136).
ggggg. **NEW**: a 2FA block names four things — time, which notification, tap the newest one only, and who verifies after the tap; an "is the account OK?" answer separates account state, login state, and the pending action (see 例137).
hhhhh. **NEW**: a new-friend photo message names the photo content, how many messages were sent, and what the reply was (here: heart only, no text); a first-send failure names its cause and re-send condition (here: not in synced contacts, re-sent after sync); a heart-only reply names the next trigger (reply in text, or B-18 at 24–48h), not "keep chasing" (see 例138).
iiiii. **NEW**: a daily count states its cutoff p-number (here p2264) and counts post-report publishing separately; a rise in "pending verification" items states whether it is new backlog or accumulated scope (872→1001 here is accumulated, unread); a misplaced comment names its intended target, its actual target, and the user's decision (delete/re-comment), never self-deleted (see 例139).
jjjjj. **NEW**: a vanished friend request is recorded as vanished at a stated check time, not as approved or rejected; a user-approved friend states the post-approval action (here: no DM, no intent signal) (see 例140).
kkkkk. **NEW**: a "skill read" note lists the required inputs and how many have arrived (here: 2 required, 0 arrived); a person-swap remake does not start without an identity-image lock (see 例141).
3. Low-risk pilots demonstrated — **now one hundred and forty-one worked examples** (例1–141).
4. Scope correction carried into the next review: FB is Victoria-only (Bertie retired 2026-11-13 Beijing 11:45), with three IG accounts content-only; Dr.qh88 deactivated, user said do not reactivate yet; any transfer item or next-review question still written in Victoria + Bertie terms must be re-read as Victoria-only (FB) plus IG content-only before it is acted on. The 200-lead single-account target now rests on Victoria alone.

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–99 carried from the 11-08 note (see that note for the full text; the standing list is not re-copied here). 例100–108 are fully worked in the 11-10 note. 例109–118 are fully worked in the 11-11 note. 例119–126 are fully worked in the 11-12 note. 例127–134 are fully worked in the 11-13 note. 例135–141 are fully worked above.

## Practice task (small, low-load; feedback after each step)

Steps 1–16 carried from the 11-11 note (checklist ticks; five-field card; patient info sheet; disputed-rule wording; owed follow-up count/retry/stop; automation-mode line; 2026-11-01 decision-slot line; Monday 17:45 line; open-disposition line; failure-mode line; scope/loop-closure line; measurement/bookkeeping line; batch/handover/metric line; recurrence-or-closure line; premise/pause/recurrence trace line; coordination-gap line). All still open.
Step 17 carried from the 11-12 note (one line per new loop gap). All still open.
Step 18 carried from the 11-13 note (one line per new loop gap from 例127–134). All still open.
Step 19 (NEW, from 例135–141): pick ONE of today's new loop gaps and write it as one line — 回执速度与执行速度分开写 / 群聊派活的判断标准与"总管先想清楚"的问老板路径 / 2FA 阻断的四件事 + 账号三层状态 / 新好友照片的 3 条 + 爱心-only 的下一条触发条件 / 日报截止 p 号 + 待核口径 + 错位评论的用户定夺 / 好友请求"已消失"的核查时点 / skill 需要物清单与到货数 — so a queue-watch fix, a 2FA block, and a live lead each leave a checkable trace instead of a bare "done".

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

Items 2, 4–8, 10 carried unchanged from the 11-11 note. Updated items:
1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28, page-plus-profile round completed 2026-10-29, rotation written and reverted same day 2026-10-30, reduced to Victoria + Emerson scope 2026-11-02, reduced again to Victoria-only scope 2026-11-04, expanded to Victoria + Bertie + IG content-only 2026-11-10/11, reduced again to Victoria-only scope 2026-11-13 (Bertie retired)**: 例135–136 是同一条线的下一环 — FB园区盯守改 1 分钟 + 5 秒回执 + 总览自动生成、群聊派活须先判断；例137 是同一条线的下一环 — 猎手傍晚撞 2FA、17:43 与 18:03 两轮没跑成；例138 是同一条线的下一环 — Ligita 新好友发术后照片、3 条要 WhatsApp、只回爱心；下一步是用户是否已点 18:57 的 2FA 批准、猎手是否已恢复、Ligita 是否已回文字、B-18 是否按时发出、用户是否已在新版 FB园区 里成功发过一条。
3. 私信首接的事件驱动升级 — done as 例8; 钩子提前到第 3 条后的漏斗执行与面诊名额台账仍在；例70 的双执行者锁、例77 的上线信号覆盖说明仍在；例86 的一次一条仍在；例91 的非目标联系人排除表仍在；例93 的"停催"独立跟进状态仍在；例97 的新好友筛查结论仍在；例106 新增一环：卡片作废后须有显式重弹路径，Margaux 等了约 18 小时；例114 新增一环：Bertie 首条私信已发（Yolande，怕术中醒着），lady_flower 私信通路卡在 Messenger 搜不到人；例117 新增一环：M Yuda 首条是用户自己发的、Connie 已删、田兆玄请求已消耗；例124 新增一环：Jocelyn Bee 是当前最接近客资的线（2 次翻修、嫌英国太贵、愿去欧洲、只差 WhatsApp），但 6.5 小时未回、草稿待用户定 Accept + 发，盯守在哪一段停住待查；例127 新增一环：Jocelyn Bee 已由用户亲自接管收口（11 月第 2 个客资），但双发 11 秒、号码疑似错误且未更正、线程已对 Muse 关闭；Bertie 线随 Bertie 退役全部关账（Yolande B-18、lady_flower 草稿、Neisha 核验、3 个好友请求不再做）；例138 新增一环：Ligita 是当前最接近客资的新线（术后 4 个月切口裂开渗液约 7mm，已发 3 条要带区号 WhatsApp，只回爱心、未回文字），B-18 在 24–48 小时内。
9. **失败上报的熔断与可用通道** — 例44 与例50 与例54 与例60 的 p634 转交死循环、例62 的误诊、例79 的加权超长、例88 的审批卡超时是同一类缺口；例94 再证：24 小时内第二起卡片超时，且 3 秒微信 escalation 两次未见触发；例105 再证：限额停工本身须带重置口径假设与复测时点，429 不是"明日再试"四个字就能闭环的；例104 再证：去重核查的方法失效本身就是上报口径的缺口，须先修方法再报数；例112 再证：平台写入故障五波，哨兵反复宕、队列与台账反复截断，兜底是 5 分钟盯守与手工记账，EPERM 根因仍未愈；例117 再证：一条"已登出"的单轮误报与一条"用户说好了"的所指不对齐，都是上报口径的缺口；例120 再证："未发送"须先拿证据再下结论，三聊同症指向系统侧，不是上下文上限；例123 再证：EPERM 第七波仍在，日报数与 p 号范围须先对账再报；例124 再证：审批卡瓶颈第四起，高意向私信 6.5 小时未回；例127 再证：审批卡瓶颈第五起以用户接管收口，同时暴露双发 11 秒的新故障形态；例129 再证：403 检查点是"只有用户能解"的停摆，不是可重试故障，暂停与恢复须各写清范围与核验顺序；例137 再证：2FA 阻断是"只有用户点通知能解"的停摆，17:43 与 18:03 两轮没跑成，点批准须点最新的一条。
11. **已过截止点的待定清单升级** — 例59 与例67 的 Monday 17:45 清单、例75–81 的"方向未定但队列在长"、例83–85 的"当日关闭项"三类分开记；例92 新增一类"同日 supersession"；例93 新增一类"当日关闭项"（Sarah Jane 停催）；例102 新增一类"当日关闭项"（发布暂停令，13 号已发、14/15 号顺延）；例106 新增一类"不回就按默认办"的四项 ask，默认行为尚未生效、用户本窗口未回；例111 新增一类"当日关闭项"（IG 只发内容，6 个任务停用）；例112 新增一类"平台故障待修项"（EPERM 根因、只发帖不存盘的根治方案待用户点头、p2803–p2808 草稿待补回）；例119 新增一类"用户已批待执行项"（AI 视频数据迭代闭环：复核时点与"爆了"标准待定）；例124 新增一类"当日关闭项待用户定"（Jocelyn Bee 的 Accept + 发，6.5 小时未回）；例126 新增一类"外部依赖待用户动手项"（4 条新线、2 份新鲜 cookie、6 条 Archive，均无再催时点）；例127 新增一类"已关闭但号码待核实项"（Jocelyn Bee 号码疑似错误、未更正、线程已关闭）；例129 新增一类"检查点待用户动手项"（视频自拍验证，已于 2026-11-13 11:51–12:05 闭环）；例133 新增一类"恢复未打勾项"（15 个停用任务中 8 个去向未写清、队列另两件事执行结果未写清、Dr.qh88 重新激活条件未写、Emerson 是否捡回待用户定）；例137 新增一类"2FA 待用户动手项"（18:57 的批准请求，用户是否已点未定、点完猎手是否已恢复未定）；例138 新增一类"等回复项"（Ligita 只回爱心、B-18 在 24–48 小时内）；例139 新增一类"用户定夺项"（错位评论删不删、17 条重复评论浏览器删）；例141 新增一类"等素材项"（美容手法换人复刻的参考视频与新人物照片均未到）；Bertie 退役后其关账 4 类不再列入待定清单。
12. **Peta 面诊时间的落定（from 例70）** — **CLOSED 2026-11-06**：Peta 已交后端咨询团队，Muse 停止跟进面诊时间；Sarah Jane 是此前最接近客资的线（英国已确认、下颌缘与下巴下方两处困扰已确认、WhatsApp 未给、11 月 12 日名额未确认），但自 2026-11-07 21:32 起主动跟进已停，下一轮只核对她是否回话，不再核对是否已催；Margaux 是另一条接近的线（Portland 眼睑、单侧更困扰已确认、WhatsApp 未给），旧回复已于 2026-11-10 Beijing 15:15 发出并核验送达，新回复先存着、等她回了再视情况用；Yolande 是 Bertie 线最接近的线（怕术中醒着已确认、首条私信已核验送达、未回、B-18 未到时间），但 Bertie 已退役、Yolande B-18 已关账不再做；lady_flower 是 Bertie 线最高意向（$9,200 全包价仍贵、接受去外地做，回评已发出、私信通路卡住），随 Bertie 退役关账；Jocelyn Bee 现为全线第 2 个已交后端的客资（见例127），号码待核实；Ligita Kondrotaite 现为全线最接近客资的新线（见例138）。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-11-15T00:36:10Z (24h, per study task plan). By then: 用户是否已点 18:57 的 2FA 批准、猎手是否已恢复并核验、17:43 与 18:03 两轮是否已补跑；Ligita 是否已回文字、B-18 是否已按时发出、她给号后是否留一步号码可达性核验；Jocelyn Bee 号码是否已更正并重新打通、后端是否已按新号码接上；用户是否已在新版 FB园区 里成功发过一条并收到回执、群聊闲聊是否确实未进队列；v6 三条是否已发出（须先重新激活 Dr.qh88）、第一批视频四项度量是否已复核、下一批调法与"爆了"标准是否已定；15 个停用任务中其余 8 个的去向、队列另两件事（猎手巡查、好友请求全通过）是否已执行；X 全日推广总数的对账、链接点击数是否已读到、17 条待删评论是否已走浏览器删、错位评论用户是否已定删不删；Emerson 是否捡回当第二个号用户是否已定；Victoria 恢复后的评论/回评/客资爬坡重算；美容手法换人复刻的参考视频与新人物照片是否已发来；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: seven new same-day worked examples (135–141) observed and preserved; the queue-watch receipt-vs-execution rule, the group-chat dispatch-judgement rule, the 2FA four-facts rule, the heart-only reply rule, the daily-count cutoff rule, the vanished-request rule, and the skill-inputs rule are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21, 例24, 例26, 例27, 例32, 例34, 例36, 例42, 例46, 例52, 例57, 例64, 例66, 例68, 例69, 例75, 例76, 例77, 例83, 例84, 例85, 例86, 例87, 例91, 例92, 例93, 例97, 例100 的榜单改写决定，例102 的停发与先拉互动决定，例103 的钩子方向决定，例108 的运营空间与 3D 分身决定，例109 的 24 小时与分身组织决定，例110 的多号定位决定，例111 的 IG 只发内容决定，例118 的团队群聊空间决定，例119 的 AI 生成直发与数据迭代决定，例121 的面诊 V1 定型决定，例125 的 3D 办公室组织决定，例127 的用户接管收口决定，例129 的 FB 暂停与恢复决定，例130 的 FB园区命名与盯守决定，例133 的 Bertie 退役决定，例136 的群聊不等于派活决定）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: 原推广队列是否已停未定；17 条待删评论仍在线、均等用户定"浏览器删"；FB 429 额度已恢复但每日额度仍在，浏览器模式切回条件未满足；13 号留还是删未定、"足够活跃"标准与天数未定；6 条钩子草稿未审；四项 ask 用户未回、默认行为未生效；X 链接点击数未拿到（卡在用户名步，待核 1001 条）；时间字段校验未见写进任务正文；两个运营空间用户是否已一次测完未定；Tatiana 的 B-18 是否已发出未定；3 秒微信 escalation 两次未见触发、原因未查；Sarah Jane 是否回话未定；Touché 14/15 号重排档位未定；IG 账号的新线与新鲜 cookie 未到；haze 锁未解；gaga 配音语言未确认；取关剩 7 个未补做；6 条 Archive 待用户在 App 里操作；猎手/盯守常驻还是错峰未定；Carmina 双份评论待修复；Yolande 回评 B 渲染状态待复核；EPERM 根因未愈；p2803–p2808 草稿全文已丢；dm-threads 拆分明晚待验；23 条加权超长草稿是否已修短未见；猎手 E07 插入段落未确认、正文未改；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知；Jocelyn Bee 号码是否已更正未定、双发锁未生效原因未查；Rina 第四轮与额度恢复未定、音乐版权未确认；v4/v5 五条中 v5 三条的逐条发出时点未写清；X 全日推广总数未对账；15 个停用任务中 8 个去向未写清；队列另两件事执行结果未写清；Dr.qh88 重新激活条件未写；Emerson 是否捡回未定；4 条新线是否已到并重绑未写清；用户是否已点 18:57 的 2FA 批准未定、猎手是否已恢复未定；Ligita 是否已回文字未定；用户是否已在新版 FB园区 里成功发过一条未定；美容手法换人复刻的参考视频与新人物照片未到。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "第二个fb不要了" (2026-11-13 Beijing 11:45, the Bertie retirement order)
- "先不激活" (2026-11-13 Beijing 14:34, the Dr.qh88 decision)
- "不是说我说什么都需要去拆解给下面的人去干活 / 不什么都需要拆解" (2026-11-13 Beijing 15:16, the group-chat dispatch correction)
- "也不是所有话都要拆解，要有自己的问题，就像你自己一样" (2026-11-13 Beijing 15:16, the manager-judgement correction)
- "账号正常了你也要在空间里面进行更新我要实时的状态！" (2026-11-13 Beijing 11:56, the real-time status order)
- "你去回客户的信息 / 客户发照片来了 / 你看看主号 / 尽快让他留下WhatsApp" (2026-11-13 Beijing 19:49–19:50, the Ligita orders)

## Research Trajectory

- *Prior trajectories reviewed*: `workspace/goals/goal/agent_notes/2026-11-13/goal.md` read in full (例1–134, constraints a–ddddd, next-review list); `workspace/goals/goal/agent_notes/2026-11-12/goal.md` carried via the 11-13 note; `user_goal.get` for goal_47ddf0ae009e (goal state, two briefings 2026-10-19/2026-10-20, zero timeline entries).
- *Repetition search*: grep-style shell search over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` for keyword variants — "自动化 / 盘点 / 任务卡 / 重复工作", "FB园区 / 群聊 / 2FA / 双重验证 / 链接点击 / 重复评论". All 24 prior notes (2026-10-20 through 2026-11-13) match the automation terms; the 2026-11-13 note already covers 例127–134 and the two October briefs already delivered the inventory checklist and first task card. No prior note or brief covers 例135–141 as a Letter topic, but every one of 例135–141 was narrated to the user live in main chat on 2026-11-13, so they are new to the written record, not new to the user.
- *User context and memory*: `muse.context_fetch` conversation category, window 2026-11-13T00:11:54Z → 2026-11-14T00:38:23Z (main-chat turns; X overnight rounds p2185–p2340, FB restore/Bertie retirement/2FA/Ligita/FB园区/skill exchanges); run handoff chunks 1–2 (evidence window 2026-11-13, FB/X/FB园区 findings); standing context in the run prompt (USER.md, MEMORY.md, people/groups indexes, alignment synthesis).
- *Connected user data*: none accessed in this study; no wearable, calendar, repo, or booking source bears on this goal today.
- *Image references checked*: none.
- *External sources viewed*: none — this study is grounded in the user's own record (goal state, prior notes, main-chat history); no web source was needed to establish today's findings.
- *Scaffolds and support tactics*: learning-goal plan carried (teach mode, novice band, retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check, next review 2026-11-15T00:36:10Z); no learning-style claim made.
- *Searches skipped or unavailable*: no web search run — the topic (the user's own 2026-11-13 automation instances) is fully evidenced by the user's own record; external research would not change the note or the ruling.
