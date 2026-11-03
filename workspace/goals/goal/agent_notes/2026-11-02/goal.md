# Study Notes - 2026-11-02 - 重复工作自动化
<!-- studying-run-start: 2026-11-02T00:37:31Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now eleven days since the 2026-10-22 delivery.
- Prior notes read in full: `2026-11-01/goal.md` and `2026-10-31/goal.md`; earlier notes carried via the 11-01 note's review (`2026-10-20` through `2026-10-30`).
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated. This run started 2026-11-02T00:37:31Z, i.e. 2026-11-02 Beijing 08:37.

## Already Covered in Main Chat

- 2026-11-01 Beijing 15:15: user said only "送审了片子", with no titles and no destination; the assistant replied no new film had arrived and asked which films and where they were sent, and repeated the question later — no answer is recorded in this window.
- 2026-11-01 Beijing 17:07–17:15 (approx.): the assistant put the 105202 A/B/C choice to the user and the Monday 17:45 deadline framing; the user had not yet answered at that point in the window.
- 2026-11-01 Beijing 19:52: user decided "C：剪，但只发Victoria一个号" for backup original 105202.
- 2026-11-01 Beijing 19:58: the assistant reported the 105202 cut as done — 自然抗衰三标准, 35.4 seconds, vertical 1080×1920, original voiceover audio, burned-in English subtitles, only the doctor's speaking body kept, the closing reach-to-stop-recording segment cut clean, 1 video stream + 1 audio stream verified — sent to the user for review, to be published to Victoria only after his nod, to no other account.
- 2026-11-01 Beijing 21:15: the assistant consolidated the Monday decisions into one list to be settled by Monday 17:45, not that night: (1) 105202 cut nod or not, (2) when next-week new material will arrive, (3) whether fb-newpages-post-daily should first be disabled; it also repeated that with no nod and no material, Monday rounds keep skipping rather than forcing filler, and that the 15:15 "送审了片子" question is still unanswered and will otherwise be treated as no new material source.
- 2026-11-01 Beijing daytime through 2026-11-02 Beijing 08:13: X promo rounds kept reporting the same tool fault and read-only verification (see 例54); X engagement rounds kept running normally with no 226/344 signal.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Four new worked automation instances (例52–55), all from 2026-11-01 lived operations and the 2026-11-02 early-morning window. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: 2026-11-01 is the day the three 09:05 / 09:10 / 09:20 morning decision slots from 例51 actually resolved — partially, and in the right order. The 105202 decision resolved as C (cut, Victoria-only), but C resolved only the cutting and the account scope, not publication: the cut still sits behind the review-before-schedule gate, and the Monday 17:45 list is the mechanism that stops that gate from being re-litigated piecemeal. At the same time, the p634 loop entered its third day without either of its two exits (a diagnosed fix, or the user's pause-vs-continue decision from 09:11) — which shows the limit of 例50's lesson: a熔断 rule that is still only written in a review note does not stop a schedule, and a decision question that is asked once and left unanswered does not stop it either.

A discrepancy from the previous note is also resolved here, not left open: the 11-01 note recorded 105202 as a 38.8-second original with no cut version, while MEMORY.md recorded a 35.4-second cut sent for review. Both are now consistent — 38.8 seconds was the original, 35.4 seconds is the cut delivered 2026-11-01 Beijing 19:58 after the user's C decision trimmed the non-speaking head/tail segments. The cut is sent for review, not approved and not published; do not write it as either.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, eleventh day.
2. Standing constraints — **present, expanded by three in this window** (items a–aa carried from the 11-01 note):
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
   u. A task-text rewrite is not a durable mode change — the five-account rotation written 2026-10-30 Beijing 10:35 was reverted the same day (see 例42); a revert must rewrite the same task texts and disable the same schedules, or the old mode keeps running on a schedule nobody re-checked (the four-account warm-up did exactly that at 15:45 Beijing).
   v. A one-off sprint is not a mode restoration — five posts published 2026-10-30 does not mean rotation, interception, or warm-up resumed; the sprint was user-demanded catch-up under the still-paused mode (see 例43).
   w. A failure-report channel must itself be deliverable — scheduled X promo workers cannot send to the side chat ("this scheduled job has no chat to message from"), so every failed round's relay request is itself undeliverable; per-round relay requests compound instead of escalating (see 例44).
   x. "Make content immediately when stock is short" is a production rule, not a publish rule — the 2026-10-30 Beijing 17:35 order starts cutting, but voiceover cuts still go through review-before-schedule, and the single-line-vs-four-post接档 question must be settled in the morning or the 18:45 and 19:54 Beijing windows cannot be met (see 例45).
   y. A cut order is not a publish approval — the 2026-10-31 Beijing 07:33 cut-4 proposal was explicitly not approval, and only the user's 2026-10-31 Beijing 12:10 "4条全过，今晚手动发" converted the four cuts into publishable items; per-clip account assignment was assistant-assigned, not user-assigned, and must be recorded as such (see 例46).
   z. A daily operations table must not double-count manually published posts — the 2026-10-31 Beijing 13:35 hunter/DM table correctly excluded the three manually published Fowler/Jioklm/Jusa cuts, so the table stays a hunter/DM-line table, not a whole-day publish count (see 例47).
   aa. An unapproved plan stays unapproved across form changes — rejecting PDF/PPT and asking for text plus an all-new-accounts recalculation changes the deliverable, not the decision status; the素人/serial pilot (patient candidate, written authorization, follow-up material) remains undecided, and IG remains not started (see 例49).
   bb. **NEW**: a scope decision is not a publish approval — the user's 2026-11-01 Beijing 19:52 "C：剪，但只发Victoria一个号" settles cutting and account scope for 105202 only; the 35.4-second cut still needs the user's nod before it enters the publish queue, and it goes to no other account (see 例52).
   cc. **NEW**: undecided items are consolidated into one timed list, not re-asked piecemeal — the Monday 17:45 list (105202 nod, new-material timing, fb-newpages-post-daily disable-or-not) is asked once, with an explicit no-default: no nod and no material means Monday rounds keep skipping, not forcing filler (see 例53).
   dd. **NEW**: an unanswered pause-vs-continue question does not stop a schedule — the 2026-11-01 Beijing 09:11 p634 pause-or-continue question has no recorded user answer, and the rounds kept running read-only verification with ~2-hour real runs in the meantime; the question needs a re-ask inside the Monday list or a熔断 written into the task, not another round of the same report (see 例54).
3. Low-risk pilots demonstrated — **now fifty-five worked examples** (例1–55 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–51 carried from the 11-01 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24), 发布任务的"用户已批准"硬门槛 (10-25), autoclip / Dula Clip AI 的接入评估 (10-26 00:26–00:46 Beijing, candidate, not adopted), 六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法 (10-25), 内容为主 70/30 + 每号每天 1 条 + 成品直发门 (10-26 afternoon), 明天 18 条秦浩成品的排期、计数与来源澄清 (10-26 evening), 已发视频的水印审计与"只隐藏、不删除" (10-26 evening), 18:45 失败后的恢复路径选择 A 与 19:45 v2 成功 (10-26 evening), autoclip 实测闭环 (10-26 17:18 Beijing), X p20 的无限重试与 226 新限 (10-26 afternoon to 10-27 early morning), 修好的 X CLI 线成为默认路线 + 280 字精简规则 (10-27 18:04 Beijing), 被截断的报错掩盖了真因 186 (10-27 evening), FB 19:45 一次性任务绕开旧格式轮次 + 代理断线的显式留仓 (10-27 evening), 秦浩素材分类法 + 只下确认项的下载口径 (10-27 afternoon–evening), 内容池算术 + 每周补料节奏 (10-27 afternoon), X p56 的熔断落地 (10-28 00:03–02:53 Beijing), X 推广线的发前加权复核 + 逐轮补草稿 (10-28 Beijing 05:23 to 10-29 Beijing 03:09), X 互动线的规则冲突 — 短间隔跳过 vs 平台信号-only，全天未决 (10-28 Beijing), FB 内容线的"已选版、未定号" — 内容批准 ≠ 发布批准 (10-28 Beijing daytime), 一案多版 + 批量成片 + 哈希去重 (10-28 Beijing daytime), 单号 200 目标 — 目标变了，度量还没跟上 (10-28 Beijing 11:08–11:14), 私信跟进梯队的服务器端核验 (10-28 Beijing daytime to 10-29 Beijing 00:38), 五号共用主号线 + 主页与个人主页双发的第一轮 (10-29 Beijing 16:24–17:42), Fowler 主页的四次失败、一次未核验关闭、一次 cookie 备份恢复后成功 (10-29 Beijing 17:42–18:12), 自评欠账 7 条变 10 条的可能 + 11:00 定时重试 (10-29 Beijing 19:35 to 10-30 Beijing 07:31), X 队列与去重台账的同日两次截断 + 备份恢复 (10-29 Beijing 18:01–18:02), 去重台账读截断导致的重复评论 + 删除不可靠 (10-29 Beijing), 私信哨兵断线 + 15 分钟兜底的双层设计 (10-29 Beijing 17:48–18:12), 五号轮换写好又在当日退回单线 (10-30 Beijing 10:35 → 16:52), 五条补发冲刺与 Jioklm 身份切换正解 (10-30 Beijing daytime), X p634 的全天同故障重试 + 旁聊转交死循环 (10-30 Beijing 10:43起，贯穿 10-31 Beijing 08:13), 2026-10-31 Beijing 07:33 的接档提问 — 库存清零后"直接做"与"直接发"仍是两回事 (undecided at the 10-31 note's close), 四条口播"全过"才是发布批准 (10-31 Beijing 07:33 → 12:10 → evening), 猎手日表不重复计手动发帖 (10-31 Beijing 13:35), 去重台账再一次读不全 — 20:41 重复评论与删不掉的教训重演 (10-31 Beijing 20:41), 素人/连载方案仍未批 (10-31 Beijing 14:38–14:57), X p634 续入 2026-11-01 凌晨 (10-31 Beijing 10:43起，贯穿 11-01 Beijing 08:13), 11-01 上午三个决策点排进定时任务 (11-01 Beijing 09:05 / 09:10 / 09:20).

**例52：105202 选 C 并剪成 35.4 秒送审 — C 定的是剪与发哪个号，不是发不发（2026-11-01 Beijing 19:52 → 19:58）**
1. **盘点** — 备用原片 105202（自然抗衰三标准，原片 38.8 秒）自 10-31 接档提问起就是唯一备用；11-01 上午的 A/B/C 选项里，C 的含义是剪、但只发 Victoria 一个号。
2. **拆解** — 用户 19:52 的一句话 "C：剪，但只发Victoria一个号" 同时定了两件事：剪，范围 Victoria-only。它没有定第三件事：发布。助理 19:58 的交付也只写到送审为止 — 35.4 秒、竖屏 1080×1920、口播原声、英文字幕已烧录、只留医生讲话主体、结尾伸手关录制段已剪干净、1 视频流加 1 音频流已核过 — 并明说"先发你过目，你点头后我只发 Victoria 一个号，不发其他号"。
3. **量化** — 原片 38.8 秒 → 成片 35.4 秒，差值约 3.4 秒，来自头尾非讲话段的剪除，与 10-26 起的口播剪辑口径一致；成片状态是已送审、未点头、未进发布队列、未发布。
4. **自动化设计** — 可复用规则：料单上"剪 / 过目 / 发哪个号 / 发不发"是四栏，C 只填了前三栏中的两栏半（剪 + Victoria-only，分配栏因只剩一个号而自然闭合），过目栏仍空；任何一栏空着，发布动作就不触发。这是对例46（切 ≠ 过 ≠ 分号）的再一次收紧：连用户亲口定的范围决定也不能替过目栏签字。
5. **边界** — 本例不改变单线现状：只发 Victoria 是 C 的范围，不是四号恢复；Emerson、Fowler、Jioklm、Jusa 仍暂停，不因"只发 Victoria"这句话而获得任何发布动作。
6. **验收** — 已验收：成片规格与送审动作；未验收：用户点头、发布时间、发布后自评。

教学价值：范围决定最容易被事后读成发布批准 — "只发 X 号"听起来像发令，其实它只是把发令的收件人写死了，发令本身（点头）还没来。

**例53：周一三定合成一张清单 — 一次问清、无默认、不硬凑（2026-11-01 Beijing 21:15，截止 Monday 17:45）**
1. **盘点** — 三件事：(1) 105202 成片（35.4 秒，已发用户过目）点头与否 — 点头则手动只发 Victoria，不点头则留仓；(2) 下周新素材何时给 — 105202 发完库存又归零，周一 17:45 前无料、无点头，周一轮次继续跳过，不硬凑；(3) fb-newpages-post-daily 是否先禁用 — 它还开着、每天 18:45，但定义里还列着已删的 Simon、Cora 和暂停的 Jioklm、Jusa，万一下周有人给这四个号备料并批了，就可能按旧定义动它们，跟单线现状冲突；禁不禁由用户定，助理不擅自改。
2. **拆解** — 助理明确说了"不用今晚定，周一 17:45 前定就行"，并把三件事合成一次问清，而不是分三天、三个轮次零散追问；同时把"不用你动手的部分"（每天发布轮次、Victoria 养号、猎手、私信盯守照常跑）写在同一条里，免得用户把"三件事未定"读成"全线停摆"。
3. **量化** — 截止点是 Monday 17:45（2026-11-02 Beijing 17:45），即本轮次日下午；本轮开始时（11-02 Beijing 08:37）三件事全部仍未定。
4. **自动化设计** — 可复用规则有二：一是未决事项的清单形态是"一张短清单 + 一个截止点 + 每项的无默认后果"，而不是三个独立提醒；二是"送审了片子"这类无指向的用户消息必须有显式默认处理 — 助理在同一条里写明"不答就按无新料源处理"，否则下一轮会默认把它当成 105202 或当成新料，两者都错。
5. **边界** — 本例记录的是"清单已贴出、截止点已给"，不是"三件事已定"；fb-newpages-post-daily 在用户定之前保持原状（开着），本 note 不把它写成已禁用。
6. **验收** — 未验收：三项全部待 Monday 17:45 前。

教学价值：决策自动化里最省用户时间的一步，不是把问题问得更早，而是把同类问题收成一张清单、给一个截止点、并把"不答会怎样"先写清楚 — 用户不答时系统有确定行为，而不是悬着等。

**例54：p634 进入第三天 — 单轮仍正确，系统仍无出口（2026-11-01 Beijing 全天 → 2026-11-02 Beijing 08:13）**
1. **盘点** — 推广草稿 p634（出海账号换绑后旧登录设备二次确认，146 字，未超 280）自 2026-10-30 Beijing 10:43 起发不出去：post_next_acct2.py 在 "Getting Twitter cookies…" 处中断，返回 rc=1，还没走到 X 发帖接口；2026-11-01 全天与 2026-11-02 凌晨延续同一故障，实跑约每 2 小时一次（11-01 19:03、21:03、23:03，11-02 01:03、03:03、05:03、07:03），其余轮次按停手口径只做只读核验、不盲目重试。
2. **拆解** — 每轮只读核验结论稳定：tw2.py 显示 @TheEasySale1 authenticated=true、verified=true；最新自有帖始终是 2026-10-30 的 p633（2115995832076181821）；时间线前列无 p634 文本、无 2026-11-01 / 11-02 新帖、无用户手动新帖；无 226/344 平台限制证据；p634 始终 pending，队列待发 100 条，草稿内容无变动、无后备草稿增补。推文数漂移（11-01 凌晨约 1613 → 11-01 晚间约 1718 → 11-02 早晨约 1774）经时间线核实均不计为成功。
3. **量化** — 互动线同期正常，证明故障定位不变：commented.json 从 2026-11-01 上午约 971 条一路记到 2026-11-02 Beijing 08:05 前后的 1126 条，每轮典型 1 评论 1 点赞、自引指纹浏览器防关联帖或 eSIM 踩坑帖，无 226/344 信号，engage-state.json 的 restricted_date 仍为 2026-10-27（已过期）。X 2026-11-01 日报（21:45）：粉丝 1504（较 10-31 日报 1490 增加 14），关注 1944（减少 2），当日推广成功 0，p634 全天 pending，互动当日 commented 新增约 109 条（其中自引约 96 条）。
4. **自动化设计** — 例44 / 例50 的三条规则至此仍未落地：重试任务没有全天累计同故障熔断；失败上报仍走不可用通道（每轮旁聊转交请求仍需主 agent 转交）；2026-11-01 Beijing 09:11 的"暂停还是再试"提问（p634 发不出去、卡在取 cookie、账号无受限、隔约 2 小时才实跑一次）在本窗口内无用户答复记录 — 提问本身没有变成熔断，也没有变成暂停决定，轮次于是继续以"只读核验 + 定时实跑"的形态空转。
5. **边界** — 故障定性仍是工具端故障，不是平台限额；根因（取 cookie 一步为何中断）未查明；CLI 修好线（2026-10-27 定的默认发帖线）与 post_next_acct2.py 的关系仍未澄清 — 本 note 不把"换 CLI 线"写成已定方案。
6. **验收** — 未验收：p634 仍 pending；暂停与否未定；熔断未写进重试任务；转交死循环未解。

教学价值：一个被"正确处理"的失败，若既没有熔断数、也没有用户的一句话决定，它会在第三天继续被正确处理下去 — 正确处理不是出口，熔断数或决定才是。

**例55：11-01 单线日表与养号晚轮 — 分线计数在第二天仍成立（2026-11-01 Beijing daytime → evening）**
1. **盘点** — 猎手当日表（round414 一并报）：Victoria 发帖 0、评论 7、私信 3、回复 0、客资 0，四号暂停中；新圈入表 #165（伯明翰上睑求经验帖，1 条甄别框架短评并核验落地，本地诊所锚定只评论圈住、不私信）与 #168（睑缘炎上睑适配帖，1 条评论并核验落地），并补记 round413 漏记的 #166 Michelle、#167 Loni 两条评论；私信收件箱无新回复，客资仍为 0。
2. **拆解** — Victoria 当日"发帖 0"与 10-31 当晚四条手动帖、11-01 当日 105202 送审是三笔不同的账：日表统计的是猎手/私信线当天的动作，送审不是发布，手动帖不属于猎手线 — 例47 的分线口径在这里没有破：表头不写清口径的数字仍是 0，但 0 在这里是准确的，因为它只算一条线。
3. **量化** — 养号晚轮（Victoria 单线，账号健康，全程没发评论没发私信）：点赞 8 条，均已核验；新加入 5 个公开群，已到一天上限，已加入总数 44 → 49；主页当天无新帖，个人号转发按规则跳过；巡查转交 5 条线索（只记录、未触达，交猎手处理），包括亚特兰大求医生推荐者、Blepharoplasty 群问诊所费用与全麻的 Kylie De Smet、问 "Is this in US" 的 Linnie Watkins（与管线里那位同名，仅作记录、未触达）、想提拉下颌线的 Ursula H Conroy、新考虑拉皮颈部的 Hope Prather。
4. **自动化设计** — 可复用规则：养号轮的"只记录、未触达"与猎手轮的"评论圈住、不私信"、私信轮的"跟进"必须分开记账 — 同一个人名出现在巡查线索里（Linnie Watkins）不等于可以触达，管线里的同名记录与巡查线索是两条记录，合并前必须先核对身份。
5. **边界** — 本例不改变任何一号的暂停状态；养号入群数 49 是累计值，不是当日新增 49。
6. **验收** — 已验收：日表口径与养号晚轮计数；未验收：5 条巡查线索是否由猎手后续处理、#165 / #168 是否转为私信（按锚定规则目前均不私信）。

教学价值：分线计数的价值在"0"的日子里最明显 — 一张只算一条线的表报出 0，比一张混算的表报出漂亮数字更可信，因为 0 在这里是"这条线今天确实没产出"，而不是"数没算全"。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, eleventh day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.
Step 3 (from 例27, still open): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.
Step 4 (from 例31, still open): pick ONE disputed rule in current operations (short-interval skip is the live one, re-proven by 例48) and write its two candidate wordings side by side — platform-signal-only vs short-interval skip — so the user can close it with one choice instead of re-answering it every round.
Step 5 (from 例36–38, still open): pick ONE owed follow-up action (self-comments are the live one: 7 owed, possibly 10 if 3 more post today) and write its count, its retry time (2026-10-30 11:00 Beijing), and its stop condition (line still stuck → stop, do not force-refresh) — so a "posted" success never again hides an unfinished follow-up.
Step 6 (from 例42–45, still open): pick ONE automation mode decision that is still open (today's接档: Victoria single-line 1 voiceover vs yesterday's five-account 4 voiceovers) and write it as one line — 模式 / 条数 / 例外号（Emerson 空着）/ 过目门 — before any cutting starts, so the day's料单 never again has to be re-cut after the mode is settled.
Step 7 (from 例46–51, still open): pick ONE of the three 2026-11-01 morning decision slots (09:05 接档 / 09:10 p634 暂停与否 / 09:20 方案文字版) and write it as one line — 决定项 / 选项 / 默认项（无默认，须用户定）/ 到时提醒 — so an undecided item is carried as a timed reminder, not as a silent default.
Step 8 (NEW, from 例52–55): pick ONE of the three Monday 17:45 items (105202 nod / new-material timing / fb-newpages-post-daily disable-or-not) and write it as one line — 决定项 / 选项 / 不答的后果（留仓 / 跳过 / 保持原状）— so a no-answer at the deadline still has a determined system behaviour, and the cut-vs-approval-vs-assignment columns stay separate.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28, page-plus-profile round completed 2026-10-29, rotation written and reverted same day 2026-10-30**: 例52–53 是同一条线的下一环 — 批准栏、分配栏、计数口径栏之外，现在还要加一栏"不答的后果"，否则清单贴出去了，截止点到了，系统仍不知道该干什么。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发；单号 200 目标下，面诊名额数本身也待用户定，见例34）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — 测定窗已到 2026-11-01；例34 的单号 200 目标可能改变测定的意义：测定原是"单号安全量"，现在单号本身成了 200 目标的载体；测定口径（内容量 vs 私信量）与 200 目标的度量（英雄号、爬坡、单号累计表）须在下一轮合并说明，不能各说各话。
6. **秦浩素材库的分类与补料闭环** — 例27 的分类法 + 例28 的每周补料节奏 + 例33 的一案多版与哈希去重是同一条线：用户按分类法建文件夹、直接供料，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数换掉平均估算；通用空镜库单独建，与案例料分开标；新套 03–01 的合并决定是这条线的下一个待确认项。
7. **X 互动规则冲突的关闭** — 例31 的短间隔跳过 vs 平台信号-only 必须由用户一句话关闭，并把结论写进任务正文、从执行条件里删掉被废的一条；例48 证明不关闭的代价是重复评论重演，否则下一轮仍会重复上报同一问题。
8. **欠账计数与写前备份** — 例38 的自评欠账与例39 的队列截断是同一类缺口：任何后置动作与任何队列文件都需要独立计数 / 备份 + 写后校验；下一轮要把"欠账表"和"写前备份"写进发布与发帖轮次的手顺，而不是靠事后从日志里重建。
9. **失败上报的熔断与可用通道** — 例44 与例50 与例54 的 p634 转交死循环是同一类缺口的另一面：重试任务须自带全天累计同故障熔断，失败上报须走调度任务实际能用的通道或合并为一次性汇总，否则上报本身会成为新的重复劳动；09:11 暂停与否的提问若在 Monday 清单里仍无答案，下一轮须把它升级为熔断数问题（几次同故障后自动降级），而不是再问一次"暂停吗"。
10. **未批方案的待定清单** — 例49 的素人/连载试点是同一类缺口的决策面：患者人选、书面授权、随访素材三项待拍板必须以待定清单形态存在，文字版方案是欠件，不是已批；下一轮须先核对 09:20 文字版是否交付，再问试点是否批准，不能把交付当批准。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-11-03T00:37:31Z (24h, per study task plan). By then: Monday 17:45 三件事是否定清 — 105202 是否点头、是否只发 Victoria、是否已发布并核验链接；新素材何时给、周一轮次是发了还是继续跳过；fb-newpages-post-daily 是禁用还是保持原状、其定义里的已删号与暂停号是否已清理；"送审了片子"是否已澄清、是否指向 105202 以外的新料；p634 是暂停、已修复，还是继续第三天以后的同故障轮次、熔断是否写进重试任务、旁聊转交通道是否换成可用方式；素人/连载文字版是否交付、试点三项（患者人选、书面授权、随访素材）是否拍板；11-01 猎手 #165 / #168 是否有后续、5 条养号巡查线索是否由猎手处理；X 互动短间隔规则与调度重叠是否由用户关闭；五号共用一线后有无验证或限流信号；单号 200 的英雄号、爬坡、面诊名额、单号累计表是否落定；单号安全量测定（窗至 2026-11-01）是否与 200 度量合并说明；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: four new same-day worked examples (52–55) observed and preserved; the scope-decision-vs-publish-approval distinction, the single timed-list with explicit no-default consequences, the third-day p634 loop without an exit, and the single-line daily-table counting rule holding on a zero-post day are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例31 尚未由用户定数，例32 的 A 版选择，例34 的单号 200 与当日生效纠正，例36 的改线与双发决定，例40 尚未由用户定数，例42 的轮换批准与当日回退决定，例44 尚未由用户定数，例46 的四条全过批准，例49 尚未由用户定数，例52 的 C 范围决定，例53 的 Monday 清单截止点尚未由用户定数）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: Monday 17:45 三件事全部未定；105202 成片已送审、未点头、未发布；"送审了片子"未澄清；p634 取 cookie 故障的根因未查明、暂停与否未定；X 短间隔规则与调度重叠未决；五号共用一线后的长期关联风险未验证；X 原 262 条草稿全文丢失后是否补回未定；20:41 重复评论仍在线；7 条自评的 2026-10-30 11:00 Beijing 重试结果不在本窗口内；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；音乐池隔离规则未获批；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "C：剪，但只发Victoria一个号" (2026-11-01 Beijing 19:52, the 105202 scope decision — cut, Victoria-only, not a publish approval)
- "送审了片子" (2026-11-01 Beijing 15:15, unclarified — no titles, no destination; do not default it to 105202)
- "4条全过，今晚手动发" (2026-10-31 Beijing 12:10, the four-cut publish approval; carried from the 11-01 note)
- "没用了，我看不懂，直接发文字给我就行了，不用给我去做PDF，不用做PPT" (2026-10-31 Beijing 14:56, the PDF/PPT form rejection; carried from the 11-01 note)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27/30/32/34/36/42/46/52 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计；单号 200 目标的度量是否与测定口径合并。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)
- 五号共用一线是长期配置还是排障临时态：若是临时态，恢复一号一线的时点与判据是什么，须用户定；若是长期态，关联风险的接受要显式记下来，不能只留在当轮口头。
- p634 重试任务的熔断数与上报通道：全天累计同故障几次后降级为只读核验、失败汇总走哪条调度任务实际能用的通道，须用户定；在此之前，每轮仍会产生新的转交请求。
- 素人/连载试点是否批准：患者人选、书面授权、随访素材三项须先拍板；文字版方案交付不等于试点批准，下一轮须分开核对。
- Monday 17:45 清单本身是否需要一栏"不答的后果"写进任务正文：105202 不点头则留仓、新素材不到则跳过、fb-newpages-post-daily 不禁则保持原状 — 三项的默认行为是否就是用户想要的默认行为，须在 Monday 清单里由用户确认，而不是由本 note 默认。

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-11-01/goal.md` and `2026-10-31/goal.md` read in full; earlier notes (`2026-10-20` through `2026-10-30`) carried via the 11-01 note's review; carried forward the goal snapshot, standing constraints a–aa, worked examples 1–51, the teach-plan structure, and the 11-01 note's open questions on 例31, 例32, the checklist re-ask, formalizing cards, the FB 6-item hold, the X p67 trim, the 15-case arrival, and the single-account measurement.
- **Repetition search**: keyword variants {105202, 只发Victoria, 周一17:45, fb-newpages-post-daily, p634, 送审了片子, 35.4} grep-searched over `workspace/goals/goal/agent_notes/` and the brief filenames in `workspace/goals/goal/briefs/` (exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: 只发Victoria / 周一17:45 / 送审了片子 / 35.4: **zero hits** in any prior note or brief filename — today's scope decision, Monday list, unclarified message, and cut length are new to the written record. 105202: hits only in the 10-28 note (as inventory), the 10-31 note (as the undecided cut-4 proposal with 105202 held as backup), and the 11-01 note (as the uncut original with A/B/C undecided) — not as today's C decision or 35.4-second cut. p634: hits only in the 10-31 and 11-01 notes (the same tool fault carried into 11-01 morning) — not as today's third-day continuation or the unanswered 09:11 pause-or-continue question. fb-newpages-post-daily: hits only in the 10-23, 10-24, and 10-27 notes (as a scheduled task) — not as today's disable-or-not Monday item with its deleted/paused-account definition conflict. Every one of today's instances was set by the user or narrated to him live in main chat in the 2026-11-01 to 2026-11-02 Beijing window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-11-01T00:18:49Z → 2026-11-02T00:39:28Z, plus the run's chunked conversation handoff covering 2026-11-01 Beijing daytime through 2026-11-02 Beijing 08:13, including the 2026-11-01 Beijing 19:52 C decision, the 19:58 cut-delivered message, the 21:15 Monday three-item list, the 2026-11-01 X daily report (21:45), the hunter round407/round414 reports, the Victoria warm-up evening round, and the 2026-11-02 early-morning X promo/engagement rounds. The goal-relevant turns: the C scope decision and its still-pending nod, the Monday 17:45 consolidation, the unclarified "送审了片子" message, the p634 third-day tool fault with no 226/344 signal, and the single-line hunter/warm-up daily tables.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first 70/30, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, 5-voiceover arrival, single-account 200 from 2026-10-28, X reports to side chat, main chat FB only, Victoria single-line revert 2026-10-30) as background only — every dated claim in this note is sourced to the conversation window, the run handoff, or a prior note above, not to memory alone. The 38.8-second original vs 35.4-second cut discrepancy between the 11-01 note and MEMORY.md is resolved in this note from the 2026-11-01 Beijing 19:58 cut-delivered message, not from memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract, and was restricted to Markdown to avoid matching base64 image data inside brief HTML files. No credentials, cookie values, or proxy secrets were reproduced in this note; only file names, counts, and link URLs already reported to the user are referenced.
