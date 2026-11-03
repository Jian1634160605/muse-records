# Study Notes - 2026-10-31 - 重复工作自动化
<!-- studying-run-start: 2026-10-31T01:03:23Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now nine days since the 2026-10-22 delivery.
- Prior notes read in full: `2026-10-30/goal.md` and `2026-10-29/goal.md`; earlier notes carried via the 10-30 note's review (`2026-10-20` through `2026-10-28`).
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated.

## Already Covered in Main Chat

- 2026-10-30 Beijing 10:02–10:04: user asked four audit questions at once — whether all personal Pages and profiles had been changed to Qin Hao avatars and bios, whether all accounts had prepared comments and DMs today, how many videos were prepared for all Pages and profiles and how many finished items sat in the backend folder, and what state all static IPs were in.
- 2026-10-30 Beijing 10:06: user supplied the Q-Flow Facelift™ packaging wording and ordered it added to Page bios.
- 2026-10-30 Beijing 10:16: user complained that no consultation link was on any Page or profile, that customer replies to comments had not been answered or turned into DMs, that only one account was doing comments and DMs despite his order that all accounts do them, asked whether all accounts could run through the Muse browser, and ordered all processes to be updated after the thinking was organized.
- 2026-10-30 Beijing 10:33: user answered the three decisions put to him — he would paste links and bios himself, the two Victoria DMs to Cristiana Winter and Kim Kieu were his own and were not to be changed, and the four-point process update was approved ("ok，你弄吧").
- 2026-10-30 Beijing 10:35: assistant confirmed the hunter task text had been rewritten to five-account rotation (Victoria, Fowler, Emerson, Jioklm, Jusa, one account per round), full reply-floor re-reading each round, a five-account table after 21:30, DM watch expanded from Victoria single-line to five accounts, and Jioklm/Jusa cold-start limits lifted from today.
- 2026-10-30 Beijing daytime: the five-account rotation was then reverted the same day — hunter and DM watch back to Victoria only, the other four paused not deleted, the four-account warm-up disabled (not deleted) after it still ran a four-account round at 15:45 Beijing.
- 2026-10-30 Beijing daytime: the five-post sprint finished all five accounts (Victoria, Fowler, Emerson, Jioklm, Jusa), including Jioklm's d2新 after the identity-switch fix; the sprint was presented as a one-off catch-up, not a restoration of rotation, interception, or warm-up.
- 2026-10-30 Beijing 17:35: user ordered that when finished stock falls below the day's publish volume, content production starts immediately without waiting, with material requested from the user rather than hunted from the library.
- 2026-10-30 Beijing 17:38: user confirmed the 2345 numbering — Victoria, Fowler, Jioklm, Jusa may publish Qin Hao voiceovers, Emerson excluded — with voiceover cuts still review-before-schedule.
- 2026-10-31 Beijing 07:33: assistant asked the user to settle today's FB接档 before the evening window — finished stock is zero after yesterday's five posts, five Qin Hao voiceover originals are on hand, the proposal is to cut four (104058, 104331, 104506, 104927; 105202 held as backup) for his review, but only one if today stays Victoria single-line; no user answer appears in this window.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Four new worked automation instances (例42–45), all from 2026-10-30 lived operations and the 2026-10-31 early-morning question. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: 2026-10-30 is the day automation configuration itself became the unstable part. A five-account rotation was written into task text in the morning and unwritten the same afternoon; a five-post sprint proved every account could publish while proving nothing about the operating mode, because the mode had already reverted; and the X promo line kept retrying the same failing step every ten minutes all day while its failure reports piled up in a delivery channel that cannot deliver. The lesson is no longer "write the rule down" — it is that a rule only counts as automation once its revert path, its one-off exception, and its failure-report channel have all been tested too.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, ninth day.
2. Standing constraints — **present, expanded by four in this window** (items a–t carried from the 10-30 note):
   a. Approval/permission popups are system-level; the agent cannot bypass or auto-approve them (2026-10-22).
   b. Guardrails must be platform-verified signals only; self-invented numbers deleted (2026-10-23).
   c. Approval-card escalation trigger is exactly 3 seconds unclicked → WeChat immediately (2026-10-24 18:06 Beijing).
   d. Any problem, any platform, any account → report immediately in main chat + WeChat with platform, account, problem, and whether the user must act (2026-10-24 22:36 Beijing).
   e. Publish pipeline gates — video review-before-schedule and post-publish self-comment guiding to the homepage WhatsApp link (2026-10-24 17:56 and 18:17 Beijing).
   f. Publish tasks now require a "用户已批准" marker in the task section itself; queue-file existence alone no longer triggers a publish (2026-10-25 Beijing afternoon).
   g. External-tool adoption test — licence, CLI/library callability, local-machine feasibility, and the effect on the project's originality claim must all be checked before adoption (2026-10-26 00:26–00:46 Beijing).
   h. Approval attaches to material type, not to each post — user-sent finished content counts as approved and posts directly; user-sent raw material that Muse edits or writes copy for still needs review-before-schedule (2026-10-26 17:52–17:53 Beijing).
   i. A failed round gets an explicit recovery choice with a stop condition, and a carried-over item must be explicitly carried in — it is not silently merged with the next day's batch (2026-10-26 19:37 Beijing, path A).
   j. Provenance can override a visible watermark — a batch cut by Qin Hao IP editors counts as Qin Hao IP even where faint Chen Jie / Li Feng / Kaminsky watermarks remain visible (2026-10-26 19:52 Beijing).
   k. A repaired tool route becomes the default route by user decision, not by habit — no switching back and forth in the same window (2026-10-27 18:04 Beijing).
   l. The 3-second WeChat escalation is now explicitly attached to FB-content approval cards, not only to DM cards (2026-10-27 19:35 Beijing).
   m. A download is only what Muse itself confirmed it wants — no bulk extra downloads; chat transfer is impossible above 100 MB per file, so large material must be pulled from the library, not sent through chat (2026-10-27 18:21–18:22 Beijing).
   n. A retry loop gets a stop — after 13 consecutive identical tool failures, the round stops retrying and does read-only verification only (2026-10-28 02:13 Beijing).
   o. Report routing is by topic, not by channel default — X promo, interaction, and daily reports go to the side chat 「X 运营报告」; main chat is FB content only; urgent matters go side chat plus WeChat (2026-10-28 17:07 Beijing).
   p. Material intake is user-supplied by default — Muse no longer specifies what material is needed or hunts the library case by case; the only exception in this window is a separately ordered generic surgery reference download, split by doctor, never mixed, and never passing another doctor's face or voice off as Qin Hao's (2026-10-28 09:47 Beijing).
   q. A target change takes effect on the corrected date, not the planned date — the single-account 200 target runs from 2026-10-28 itself, after the user corrected the "preparation period until 2026-11-01" reading the same morning (2026-10-28 11:14 Beijing).
   r. All five FB accounts share the main account's line by user order (2026-10-29 Beijing 16:28), a troubleshooting instruction whose association risk was already known and accepted for the earlier Fowler/Emerson sharing and is now extended to all five.
   s. "No more approval cards, pass them all yourself" is not achievable — restated 2026-10-29 Beijing 16:32; the mitigations that do exist are scheduled tasks that do not pop cards, and the per-category "始终允许" choice (Messenger DM sending already set).
   t. Cookie-backup restore is a proven recovery for browser-crash login loss — stop the browser, copy the `cookies.sqlite.bak` back over `cookies.sqlite`, delete the `-wal`/`-shm` files, relaunch — applied successfully to Fowler, Jioklm, and Jusa 2026-10-29 Beijing evening.
   u. **NEW**: a task-text rewrite is not a durable mode change — the five-account rotation written 2026-10-30 Beijing 10:35 was reverted the same day (see 例42); a revert must rewrite the same task texts and disable the same schedules, or the old mode keeps running on a schedule nobody re-checked (the four-account warm-up did exactly that at 15:45 Beijing).
   v. **NEW**: a one-off sprint is not a mode restoration — five posts published 2026-10-30 does not mean rotation, interception, or warm-up resumed; the sprint was user-demanded catch-up under the still-paused mode (see 例43).
   w. **NEW**: a failure-report channel must itself be deliverable — scheduled X promo workers cannot send to the side chat ("this scheduled job has no chat to message from"), so every failed round's relay request is itself undeliverable; per-round relay requests compound instead of escalating (see 例44).
   x. **NEW**: "make content immediately when stock is short" is a production rule, not a publish rule — the 2026-10-30 Beijing 17:35 order starts cutting, but voiceover cuts still go through review-before-schedule, and the single-line-vs-four-post接档 question must be settled in the morning or the 18:45 and 19:54 Beijing windows cannot be met (see 例45).
3. Low-risk pilots demonstrated — **now forty-five worked examples** (例1–45 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–41 carried from the 10-30 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24), 发布任务的"用户已批准"硬门槛 (10-25), autoclip / Dula Clip AI 的接入评估 (10-26 00:26–00:46 Beijing, candidate, not adopted), 六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法 (10-25), 内容为主 70/30 + 每号每天 1 条 + 成品直发门 (10-26 afternoon), 明天 18 条秦浩成品的排期、计数与来源澄清 (10-26 evening), 已发视频的水印审计与"只隐藏、不删除" (10-26 evening), 18:45 失败后的恢复路径选择 A 与 19:45 v2 成功 (10-26 evening), autoclip 实测闭环 (10-26 17:18 Beijing), X p20 的无限重试与 226 新限 (10-26 afternoon to 10-27 early morning), 修好的 X CLI 线成为默认路线 + 280 字精简规则 (10-27 18:04 Beijing), 被截断的报错掩盖了真因 186 (10-27 evening), FB 19:45 一次性任务绕开旧格式轮次 + 代理断线的显式留仓 (10-27 evening), 秦浩素材分类法 + 只下确认项的下载口径 (10-27 afternoon–evening), 内容池算术 + 每周补料节奏 (10-27 afternoon), X p56 的熔断落地 (10-28 00:03–02:53 Beijing), X 推广线的发前加权复核 + 逐轮补草稿 (10-28 Beijing 05:23 to 10-29 Beijing 03:09), X 互动线的规则冲突 — 短间隔跳过 vs 平台信号-only，全天未决 (10-28 Beijing), FB 内容线的"已选版、未定号" — 内容批准 ≠ 发布批准 (10-28 Beijing daytime), 一案多版 + 批量成片 + 哈希去重 (10-28 Beijing daytime), 单号 200 目标 — 目标变了，度量还没跟上 (10-28 Beijing 11:08–11:14), 私信跟进梯队的服务器端核验 (10-28 Beijing daytime to 10-29 Beijing 00:38), 五号共用主号线 + 主页与个人主页双发的第一轮 (10-29 Beijing 16:24–17:42), Fowler 主页的四次失败、一次未核验关闭、一次 cookie 备份恢复后成功 (10-29 Beijing 17:42–18:12), 自评欠账 7 条变 10 条的可能 + 11:00 定时重试 (10-29 Beijing 19:35 to 10-30 Beijing 07:31), X 队列与去重台账的同日两次截断 + 备份恢复 (10-29 Beijing 18:01–18:02), 去重台账读截断导致的重复评论 + 删除不可靠 (10-29 Beijing), 私信哨兵断线 + 15 分钟兜底的双层设计 (10-29 Beijing 17:48–18:12).

**例42：五号轮换写好又在当日退回单线 — 任务正文改了，模式没稳住（2026-10-30 Beijing 10:35 → 12:04 → 14:58 → 16:52）**
1. **盘点** — 用户 10:16 Beijing 的五条投诉里，第三条是核心自动化指控：他明明要求所有账号都做私信评论，到现在却只有一个账号在做。助理 10:21 Beijing 认账并归因：猎手评论走的命令行只有 Victoria 的会话，私信盯守和秒回哨兵也只接 Victoria，Fowler、Emerson 从来没有接过评论私信工具，Jioklm、Jusa 的冷启动限制后来也没正式解除；10 月 26 日批了 Fowler、Emerson 截流为主、但同时定了猎手任务正文先不动，执行就一直没变 — 这是流程欠账，不是账号出问题。
2. **拆解** — 用户 10:33 Beijing 三条全批：链接和简介他自己粘贴、两条 Victoria 私信是他本人发的、不动、流程更新照办。助理 10:35 Beijing 报任务正文已改完并核实：猎手改成五号轮换（Victoria、Fowler、Emerson、Jioklm、Jusa，每轮只用一个号）、每轮必读已评论帖的全部回复楼层、每天 21:30 后的第一轮出一张五号表、私信盯守从 Victoria 单线扩到五号、Jioklm、Jusa 冷启动限制当日解除；下一轮猎手 10:43、私信盯守 10:48 就按新规则跑。边界当时就交代了：实时 30 秒哨兵仍只接 Victoria，其他号的新回复先由 15 分钟盯守接。
3. **量化** — 新模式存活不到两小时：用户 12:04 Beijing 定退回 Victoria 单线，14:58 Beijing 说"继续"后动手，猎手与私信盯守均改回只走 Victoria，Emerson、Fowler、Jioklm、Jusa 四号暂停（非删除），其他四号私信哨兵停用，Victoria 30 秒哨兵不变；定时与开关均已核验（猎手 10 分钟、盯守 15 分钟，下一轮均为 15:03 Beijing）。但回退并不彻底：15:45 Beijing 养号轮换仍按原任务跑了四号，用户随后在 16:52 Beijing 定养号也一起暂停，fb-foxprofile-warm-daily 已禁用（enabled=false、下一轮为空，已核验），非删除，Victoria 自身养号任务未动。
4. **自动化设计** — 可复用规则有三：一是模式变更的清单必须包括所有同模式任务 — 猎手、私信盯守、私信哨兵、养号轮换是同一模式的四条腿，只改两条腿，第三条腿会在下一轮按旧模式自己跑起来；二是回退也要像上线一样核验下一轮时间与开关，不能只改正文；三是"暂停"与"删除"必须在任务正文里分开写 — 四号是暂停，恢复时重新启用即可，这一点在 16:52 Beijing 的处置里写对了，值得保留为模板。
5. **边界** — 回退的原因在本窗口里没有被用户明说为某一条规则失败；本 note 不猜原因，只记事实：轮换正文写好、核验过、下一轮已排，然后被用户指令撤销。轮换本身不是被证伪，只是被叫停。
6. **验收** — 已验收：单线回退后的两份正文与两档开关（猎手、盯守）均已核验，养号禁用已核验；未验收：回退后其他四号的私信哨兵停用是否逐一核验、Victoria 单线之外的四号何时恢复 — 均未在本窗口内落定。

教学价值：自动化系统里，"改任务正文"是最容易被误认为"已上线"的一步 — 正文改了、下一轮排了，仍不等于模式稳了；模式的验收要看全部同模式任务的开关状态，而回退的验收同样要看全部同模式任务的开关状态，漏查一条就会出现 15:45 Beijing 那种"已回退、还在跑"的幽灵轮次。

**例43：五条补发冲刺与 Jioklm 身份切换正解 — 发齐了，不等于模式恢复了（2026-10-30 Beijing daytime）**
1. **盘点** — 用户当日坚持下，全号补发最终到了五条：Victoria set03-C（Reel 1362623543608220）、Fowler case1-B（Reel 1971872010440400）、Jioklm d2新（Reel 2395788514507129），另加 Emerson b4 与 Jusa 60，五条在 13:19Z 前后全部完成。背景是 10 月 30 日上午的库存账：今天要发 3 条（Emerson b4、Jioklm d2新、Jusa 60），发完能直接发的成品只剩 2 条的旧账已被当日的五条冲刺覆盖 — 冲刺用的是用户坚持下的补发，不是日常料单。
2. **拆解** — Jioklm d2新卡住的真因不是浏览器卡，而是身份切不过去：会话卡在个人号上，账号菜单里没有切换入口，主页页面加载不全，点主页链接只打开主页、不会切换身份，硬发会发到个人号上，助理没发。解法在当晚实证：正确方法是点右上角头像按钮（aria-label 为 Account, your profile 的 div，不是 Account Controls and Settings 容器），菜单打开后再点主页行即可切到主页身份；Fowler、Jioklm 均已用此法切成功并发帖。另：面板流发帖须用精确文本匹配点 Post，:has-text 式点击会误触导致未提交；核验标准是三重 — "Your Post is successfully shared with EVERYONE" + 1 分钟内新通知 + 主页新帖。
3. **量化** — 五条全部链接核验；Jioklm 第一轮未提交、第二轮重发才 posted — 第一轮的"点了 Post"同样是过程信号，不是结果证据（与例37 的编辑器关闭教训同构）。
4. **自动化设计** — 可复用点有二：一是身份切换手順要写到按钮级（点哪个 div、不是哪个容器），"点头像菜单"这种粗粒度手順在界面渲染不全时会让执行者在两个相似入口之间选错；二是当日发布数不能读成模式信号 — 五条是用户坚持下的补发冲刺，猎手、私信、养号仍按单线暂停，下一轮若按"五条已发"默认轮换已恢复，就会重犯例42 的幽灵轮次错误。
5. **边界** — Simon 已删、Cora 已删，不在五条之内；Emerson 按 10 月 30 日确认不能发口播，冲刺里的 Emerson b4 是成品、不是口播，两者不冲突。
6. **验收** — 已验收：五条链接；未验收：冲刺后四号的暂停状态是否在次日料单里被再次确认 — 10 月 31 日接档问题（例45）正是这个验收的延续。

教学价值：一次成功的"全员发齐"最容易被误读为系统恢复 — 计数（发了几条）与模式（按什么规则跑）是两张表；只看计数表，系统会在暂停模式下被误报为已恢复。

**例44：X p634 的全天同故障重试 + 旁聊转交死循环（2026-10-30 Beijing 10:43 起，贯穿 2026-10-31 Beijing 08:13）**
1. **盘点** — 推广草稿 p634（出海账号换绑后旧登录设备二次确认，146 字）从 2026-10-30 Beijing 10:43 起每一轮都发不出去：post_next_acct2.py 在 "Getting Twitter cookies…" 处中断，返回 rc=1，还没走到 X 发帖接口；同一故障贯穿 2026-10-31 Beijing 00:03 至 08:13 的每 10 分钟一轮。最新帖始终是 2026-10-30 的 p633（2115995832076181821），p634 始终 pending；账号会话每次核验均为 authenticated=true、verified=true；当日无用户手动新帖、无重复。
2. **拆解** — 每轮都做了正确的单轮动作：发前备份队列（promo-queue.backup-2026-10-31-HHMM.json）、发后用 tw2.py 核时间线、按规则不盲目重试、不追加后备草稿、记 post-log 与当日记忆日志。但单轮正确不等于系统正确：重试任务本身每 10 分钟准时再触发一次，于是"不盲目重试"只发生在单轮内，全天看仍是几十次同一失败的重复执行；这与例29 的熔断（13 次同故障后停手、只做只读核验）形成对照 — 熔断规则没有被写进这个重试任务的执行条件，或者重试任务的语义本身就是"一直重试"，两种读法在本窗口内都没有被用户裁定。
3. **量化** — 故障计数：2026-10-30 日报记 p634 当日 65 轮失败；2026-10-31 Beijing 08:13 前又续了约 50 轮（00:03 起每 10 分钟一轮，含 04:03、04:53 轮次的推文数 1419→1420、1446→1447 式计数漂移，均经时间线核实不计为成功）；互动线同期正常 — commented.json 从 2026-10-30 上午约 585 条一路记到 2026-10-31 Beijing 08:12 的 803 条，无 226/344 信号，restricted_date 仍为 2026-10-27（已过期） — 证明故障在发帖工具的取 cookie 一步，不在账号受限。
4. **自动化设计** — 可复用规则有三：一是重试任务必须自带熔断计数（全天累计同故障 N 次后降级为只读核验 + 一次性汇总上报），否则"每轮不盲重试"会被调度本身架空；二是失败上报必须走调度任务实际能用的通道 — 本窗口每轮都请求主 agent 转交旁聊「X 运营报告」（chat_id 093b2553-1b59-4baf-8f8a-940f4deb8d99），而每轮都被系统以 "this scheduled job has no chat to message from" 拒绝，于是转交请求本身成了每轮重复产生的未交付项；三是计数漂移（推文数 +1 但时间线无新帖）必须有明文规则 — 本窗口各轮都正确地不计为成功，值得写进发帖核验手順。
5. **边界** — 故障定性在本窗口内是稳的：工具端故障，不是平台 226/344 信号，不触发停号规则；根因（取 cookie 一步为何中断）未查明，CLI 修好线（2026-10-27 定的默认发帖线）与 post_next_acct2.py 的关系也未在本窗口内澄清 — 本 note 不把"换 CLI 线"写成已定方案。
6. **验收** — 未验收：p634 仍 pending；转交死循环未解（每轮仍在产生新的转交请求）；熔断是否应写进重试任务未由用户定。

教学价值：自动化系统里最隐蔽的重复劳动，是"报告失败"本身 — 当上报通道不可用时，每轮失败都会再生产一份新的上报任务；没有熔断 + 可用通道的失败上报，会从"提醒人"变成"给人添活"。

**例45：2026-10-31 Beijing 07:33 的接档提问 — 库存清零后，"直接做"与"直接发"仍是两回事（2026-10-31 Beijing 07:33，窗口结束时未决）**
1. **盘点** — 晨间提问先报库存事实：昨天五条已全部发齐，能直接发的成品库存清零；按用户 2026-10-30 Beijing 17:35 定过的规矩，库存不够就直接做内容，不等；现成的料是五条秦浩口播原片，竖屏、38 到 56 秒，符合标配。
2. **拆解** — 方案是先剪四条送用户过目：104058（松弛程度）、104331（小拉皮恢复时间）、104506（35 岁后松弛自测）、104927（小拉皮全流程），105202 留作备用；剪辑口径不变：只留医生讲话主体，剪掉开头结尾非讲话段和摄影师出境段，原声不另嵌音乐，英文字幕；剪好先发用户过目，用户点头后才排发，不直接进队列。提问的核心是模式选择：昨天实际是五号全发齐，但猎手和私信线那边四号还标着暂停，用户还没给今天走哪条线的指令 — 如果今天只走 Victoria 单线，就只剪一条；如果沿用昨天全号发齐，才剪四条；Emerson 按 10 月 30 日确认不能发口播，今天默认空着，除非用户另给它一条成品。
3. **量化** — 时间压力是显性的：今晚窗口是 18:45 和 19:54 Beijing，成片得在用户过目后才能进，所以上午就得定；剪四条与剪一条的工作量差是四倍，定晚了等于默认只剪一条。
4. **自动化设计** — 可复用规则：库存清零触发的是"生产"（剪），不是"发布"（发） — 2026-10-30 Beijing 17:35 的"直接做内容"与 2026-10-26 定的口播先审后排（只留医生讲话主体、剪好发用户过目后再排发）并不冲突，前者管"不等"，后者管"不直发"；把两者混成"库存不够就直发"，就是把生产授权偷换成发布授权（与例32 的内容批准 ≠ 发布批准同构）。接档问题本身也是一条规则：每日料单的第一行应是模式（单线几条 / 全号几条），而不是先剪再问。
5. **边界** — 105202 备用、Emerson 空着，都是默认项，用户一句话即可改；本 note 不默认其中任何一种为今日模式。
6. **验收** — 未验收：用户在窗口结束时尚未回答；剪一条还是剪四条、以及 11:00 自评重试（例38 的遗留项）的结果，均不在本窗口内。

教学价值：库存自动化最容易错的一步，是把"缺货信号"直接连到"发布动作" — 中间必须经过生产、过目、排发三道门；缺货只应加速第一道门，不能跳过后两道。

附带实例（同一窗口的技能包导出，未决其复用价值）：2026-10-30 Beijing 上午用户要求把当前 FB 海外医美工作模式与工具整理成 skill / 下载数据给其他 Muse 用，不带账号数据与静态 IP 数据；当日 08:12Z 前后已交付 `~/workspace/custom-skills/fb-ip-operations/SKILL.md` + `references/checklists.md` 及单文件导出版，内全部为占位符，接收方须替换为自有值后才能跑。自动化视角：导出的是方法与清单，不是账号能力 — 方法可迁移、登录态与 IP 隔离不可迁移，这一点在 08:54Z 的答复里已向用户说明；本 note 只记为方法沉淀，不记为已验证的复用。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, ninth day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.
Step 3 (from 例27, still open): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.
Step 4 (from 例31, still open): pick ONE disputed rule in current operations (short-interval skip is the live one) and write its two candidate wordings side by side — platform-signal-only vs short-interval skip — so the user can close it with one choice instead of re-answering it every round.
Step 5 (from 例36–38, still open): pick ONE owed follow-up action (self-comments are the live one: 7 owed, possibly 10 if 3 more post today) and write its count, its retry time (2026-10-30 11:00 Beijing), and its stop condition (line still stuck → stop, do not force-refresh) — so a "posted" success never again hides an unfinished follow-up.
Step 6 (NEW, from 例42–45): pick ONE automation mode decision that is still open (today's接档: Victoria single-line 1 voiceover vs yesterday's five-account 4 voiceovers) and write it as one line — 模式 / 条数 / 例外号（Emerson 空着）/ 过目门 — before any cutting starts, so the day's料单 never again has to be re-cut after the mode is settled.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28, page-plus-profile round completed 2026-10-29, rotation written and reverted same day 2026-10-30**: 例42–43 是同一条线的下一环 — 模式变更与回退的开关核验清单（猎手、私信盯守、私信哨兵、养号轮换四条腿）是这条线现在最缺的一页。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发；单号 200 目标下，面诊名额数本身也待用户定，见例34）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — 例34 的单号 200 目标可能改变测定的意义：测定原是"单号安全量"，现在单号本身成了 200 目标的载体；测定口径（内容量 vs 私信量）与 200 目标的度量（英雄号、爬坡、单号累计表）须在下一轮合并说明，不能各说各话。
6. **秦浩素材库的分类与补料闭环** — 例27 的分类法 + 例28 的每周补料节奏 + 例33 的一案多版与哈希去重是同一条线：用户按分类法建文件夹、直接供料，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数换掉平均估算；通用空镜库单独建，与案例料分开标；新套 03–01 的合并决定是这条线的下一个待确认项。
7. **X 互动规则冲突的关闭** — 例31 的短间隔跳过 vs 平台信号-only 必须由用户一句话关闭，并把结论写进任务正文、从执行条件里删掉被废的一条；否则下一轮仍会重复上报同一问题。
8. **欠账计数与写前备份** — 例38 的自评欠账与例39 的队列截断是同一类缺口：任何后置动作与任何队列文件都需要独立计数 / 备份 + 写后校验；下一轮要把"欠账表"和"写前备份"写进发布与发帖轮次的手顺，而不是靠事后从日志里重建。
9. **失败上报的熔断与可用通道（NEW）** — 例44 的 p634 转交死循环是同一类缺口的另一面：重试任务须自带全天累计同故障熔断，失败上报须走调度任务实际能用的通道或合并为一次性汇总，否则上报本身会成为新的重复劳动。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-11-01T01:03:23Z (24h, per study task plan). By then: 2026-10-31 的接档是单线 1 条还是全号 4 条口播，用户是否答复、剪了几条、过了目没有、18:45 与 19:54 Beijing 窗口是否赶上；7 条（或 10 条）自评在 2026-10-30 11:00 Beijing 重试后是否补齐；p634 的取 cookie 故障是否查明根因、熔断是否写进重试任务、旁聊转交通道是否换成可用方式；X 互动短间隔规则与调度重叠是否由用户关闭；五号共用一线后有无验证或限流信号；单号 200 的英雄号、爬坡、面诊名额、单号累计表是否落定；音乐池隔离新规则是否获批；新套 03–01 是否合并、02 的水印与天数、04 的启用、05 的齐全性是否确认；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: four new same-day worked examples (42–45) observed and preserved; the same-day rotation revert with its incomplete first pass, the sprint-vs-mode distinction, the per-round-correct but system-level retry-plus-undeliverable-relay loop, and the produce-vs-publish distinction at zero stock are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例31 尚未由用户定数，例32 的 A 版选择，例34 的单号 200 与当日生效纠正，例36 的改线与双发决定，例40 尚未由用户定数，例42 的轮换批准与当日回退决定，例44 尚未由用户定数）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: 2026-10-31 接档（单线 1 条 vs 全号 4 条）未定；7 条自评的 2026-10-30 11:00 Beijing 重试结果不在本窗口内；p634 取 cookie 故障的根因未查明；X 短间隔规则与调度重叠未决；五号共用一线后的长期关联风险未验证；X 原 262 条草稿全文丢失后是否补回未定；Dreamofkang 与 andynotbot 的重复评论仍在线；私信哨兵状态文件写失败的根因未深究（重启自愈）；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；音乐池隔离规则未获批；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "我发现一个问题哈，你管理的这些账号，除开那个主号其他账号你都没发过视频，我今天才知道" (2026-10-29 Beijing 16:24, the per-account zero-post discovery; carried from the 10-30 note)
- "你把其他账号的静态IP都改成和主号一样 的你试试能不能解决问题！" (2026-10-29 Beijing 16:28, shared-line order; carried from the 10-30 note)
- "后面不用再给我发审核了全部你自己过就行了，我烦了" (2026-10-29 Beijing 16:32, approval-frustration order, answered as not achievable by the agent; carried from the 10-30 note)
- "那你现在给所有的账号都发一个作品" / "还有所有的主页都要发，主页和个人主页都要发！" (2026-10-29 Beijing 16:33–16:34, page-plus-profile round order; carried from the 10-30 note)
- "修补好了就一直用修好的线，OK" (2026-10-27 18:04 Beijing, repaired-line default; carried from the 10-28 note)
- "我先查代理，你等我消息" (2026-10-27 21:02 Beijing, proxy hold; carried from the 10-28 note)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27/30/32/34/36/42 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计；单号 200 目标的度量是否与测定口径合并。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)
- 五号共用一线是长期配置还是排障临时态：若是临时态，恢复一号一线的时点与判据是什么，须用户定；若是长期态，关联风险的接受要显式记下来，不能只留在当轮口头。
- p634 重试任务的熔断数与上报通道：全天累计同故障几次后降级为只读核验、失败汇总走哪条调度任务实际能用的通道，须用户定；在此之前，每轮仍会产生新的转交请求。

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-30/goal.md` and `2026-10-29/goal.md` read in full; earlier notes (`2026-10-20` through `2026-10-28`) carried via the 10-30 note's review; carried forward the goal snapshot, standing constraints a–t, worked examples 1–41, the teach-plan structure, and the 10-30 note's open questions on 例31, 例32, the checklist re-ask, formalizing cards, the FB 6-item hold, the X p67 trim, the 15-case arrival, and the single-account measurement.
- **Repetition search**: keyword variants {单线, 五条, p634, 旁聊转交, 口播接档, 轮换, 补发} grep-searched over `workspace/goals/goal/agent_notes/` and the brief filenames in `workspace/goals/goal/briefs/` (exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: 单线 / 五条 / p634 / 旁聊转交 / 口播接档: **zero hits** in any prior note or brief filename — today's instances are new to the written record. 轮换: hits only in the 10-24 note (the rotation concept and its 10-23 rollout) and the 10-26 note (rotation task-text update still pending) — not today's same-day write-then-revert event. 补发: hits in many prior notes as generic re-posting, not as today's five-post sprint under a still-paused mode. Every one of today's instances was set by the user or narrated to him live in main chat in the 2026-10-30 to 2026-10-31 Beijing window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-30T00:19:01Z → 2026-10-31T01:17:28Z, plus the run's chunked conversation handoff covering 2026-10-30 Beijing daytime through 2026-10-31 Beijing 09:03, including the 2026-10-31 Beijing 07:33 接档 question. The goal-relevant turns: the user's four audit questions and Q-Flow order, the five-complaint message and the three-decision answer, the 10:35 rotation rewrite confirmation, the same-day Victoria single-line revert and the 16:52 warm-up disable, the five-post sprint completion, the 17:35 make-content-immediately order, the 17:38 2345 voiceover numbering confirmation, the all-day X p634 tool-fault rounds with blocked side-chat relay requests, and the undecided 2026-10-31 接档 question.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first 70/30, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, 5-voiceover arrival, single-account 200 from 2026-10-28, X reports to side chat, main chat FB only, Victoria single-line revert 2026-10-30) as background only — every dated claim in this note is sourced to the conversation window, the run handoff, or a prior note above, not to memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract, and was restricted to Markdown to avoid matching base64 image data inside brief HTML files. No credentials, cookie values, or proxy secrets were reproduced in this note; only file names, counts, and link URLs already reported to the user are referenced.
