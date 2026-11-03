# Study Notes - 2026-10-23 - 重复工作自动化
<!-- studying-run-start: 2026-10-22T19:56:04.864564+00:00 -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (zero observed performances — user has not attempted retrieval or a five-field card); evidence label `tentative`.
- Goal timeline has **zero entries** since creation. The 盘点清单 brief (`goal_briefing_135212c5fa67`) was delivered to the user in main chat at **2026-10-22T07:26:08Z** (with the assistant's live checklist explanation at 07:26:20Z); the 任务卡 brief was last delivered 2026-10-21T04:46:42Z. Neither delivery produced a user reply yet.
- Prior notes read in full: `2026-10-20/goal.md`, `2026-10-21/goal.md`, `2026-10-22/goal.md`. Prior briefs verified by title/filename topic index (not re-read in full): `Brief (2026-10-19 19.34.10).html` = 第一张任务卡， `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单.

## Already Covered in Main Chat

- 2026-10-22T06:26:08Z: main agent delivered the "在跑能力 + 每日安排" inventory (FB 3号→7号矩阵、X 两号、内容生产、私信打法、微信 ClawBot、情报 + 每日北京时间排期；已停 IG/TikTok/LI Feng/飞书) — the raw material the user can now map onto the automation checklist.
- 2026-10-22T07:26:20Z: main agent delivered this goal's 第一份盘点清单 live: 7 项候选（三平台发布流水线、评论私信巡查、评论区截流、X 双号运营+日报、PPT 改版循环、备料换音乐、三平台养号），asked the user to just check which ones he still does by hand, promised to rank by 耗时×频率 and start with item 5 (PPT). **No user reply to this ask exists in the window.**
- 2026-10-22T13:35:24Z: in the day's work summary the assistant named this goal explicitly: "重复工作自动化：盘点清单已发你，还等你挑先做哪一项。" No user reply.
- Today's automation events were all narrated to the user live and mostly approved by him: 评论单出口拆分 (user approved 17:45, "按拆分方案改"), hunter 评论 13/12 超额 admission + 串行锁 fix (12:47), 私信"假气泡" debacle + 服务器端核验新规 (20:47–20:50), Kevin 直发核验 (21:10), 4 新号纳入日常运营 with 2 new scheduled tasks (user 👌 at 19:26). He experienced all of these.
- 2026-10-22T17:49:12Z: user asked "今晚需要我审核的你直接全部自动过" — assistant answered honestly: approval cards are system-level security prompts the agent cannot bypass or disable; will batch work, hold anything needing approval, never disturb him at night; tip: choose "始终允许" next time. This is a **new boundary** for this goal (approval clicks are not automatable).

## What this study adds

Today the goal record gains three new worked automation instances — all narrated live today but preserved here as teach-plan evidence (examples 4–6 below). They strengthen the "盘点→拆解→量化→规则化→验收" pattern with same-day incidents:

1. **例4：评论单出口拆分（2026-10-22）** — two tasks (fb-engage-daily, fb-competitor-watch) both publishing comments, no shared budget check; hunter hit 13/12 yesterday from misaligned counts. Design: single comment outlet (hunter), fb-engage-daily downgraded to pure warm-up (browse/like/join groups, no comments/DMs). User approved at 17:45; verified in effect the same evening.
2. **例5：串行锁记账规则（2026-10-22）** — same root cause family as 例2 (FB dedup ledger): fix was making each round re-read the live daily counter before publishing and write the ledger immediately after each comment, not batch at round end.
3. **例6：私信服务器端核验新规（2026-10-22）** — browser "Message sent" bubbles proved fake (4 of 7 DMs never reached the server; user caught it on his phone). Rule: a DM counts as sent only after the server-side thread/message is verified; existing conversations use the direct tool-send path with immediate verification. This is the strongest "验收" lesson: never trust UI state.

Also new to the record: **例3（FoxProfile 免扫码，from 10-22 note) remains the goal's only completed automation card**, still unlogged to the goal timeline, and the "自己发视频" half of the user's original pick is still unresolved (open question carried forward).

Prerequisite re-check: inventory is now **delivered and seen by the user** (07:26Z) but **not yet confirmed/checked** — the blocker moved one step: from "waiting for list" → "list delivered, awaiting user's ticks."

## Prerequisite check

1. A concrete inventory of the user's recurring tasks — **delivered**: 7-item draft checklist (10-20 brief, delivered in main chat 2026-10-22T07:26:08Z) + capability/daily-schedule inventory (06:26Z). Not yet confirmed by the user — that is now the single open ask.
2. Standing constraints recorded — **present**, one new addition: approval/permission popups are system-level and cannot be bypassed or auto-approved by the agent (2026-10-22T17:49Z).
3. Low-risk pilots demonstrated — **present, now six worked examples** (see below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

Keep 例1 团队周报 (2026-10-19, from 10-20 note), 例2 FB 去重台账 (2026-10-20, from 10-21 note), 例3 FoxProfile 免扫码登录 (2026-10-21, from 10-22 note).

**例4：评论单出口拆分（2026-10-22，当天真实事件）**
1. **盘点** — 每天两轮评论输出：猎手（fb-competitor-watch）+ 互动任务（fb-engage-daily）。
2. **拆解** — 两任务各自独立发评论，无人检查 12/天 上限；且会撞同一帖（10-21 双评事故）。
3. **量化** — 10-22 猎手实际发出 13/12，多发 1 条（轮次间数据没对齐）；删不掉，已是事实。
4. **自动化设计** — 评论只由猎手发（它的定义里本来就有上限+去重台账）；fb-engage-daily 改纯养号（只浏览点赞+申群+巡查转交线索，不发评论不私信）。用户 17:45 批准，当晚生效。
5. **边界** — 撞限即停护栏不变；专家评论仍逐条人写内容。
6. **验收** — 改完回读验证生效；下一轮看评论数是否 ≤12。

**例5：评论计数串行锁（2026-10-22，与例4同一天）**
1. **盘点** — 猎手每轮发多条评论。
2. **拆解** — 发之前按"轮次开始时读到的计数"判断额度，发完攒到最后统一记账。
3. **量化** — 两轮次并行时各自按过期数据判断 → 超发 1 条。
4. **自动化设计** — 每次发布前重读当天实时计数；发完一条立刻记账再发下一条。
5. **边界** — 只约束计数读写顺序，不改变评论内容规则。
6. **验收** — 待下一轮验证（alignment 标注为"待下轮验证执行"）。

**例6：私信服务器端核验（2026-10-22，当天真实事件）**
1. **盘点** — 每天最多 6 条陌生人私信；当天"已发送"7 条（含补发）。
2. **拆解** — 浏览器弹窗显示"Message sent"气泡 → 当成已发送上报。
3. **量化** — 用户用手机 App 当场揭穿：Charlene、Judi 补发、Lucy、Kevin 四条服务器端根本不存在；只有 Anne、Sarah 真送达。**信任账户最大的一次扣分。**
4. **自动化设计** — 新规：任何私信必须经 hatch_messenger_cli 查到线程+内容才算"已发"；浏览器气泡=未核验，不得汇报；已有会话改走工具直发路线、当场核验。已写入 fb-dm-thread-watch 任务。
5. **边界** — 24 小时新消息请求上限等平台风控仍是硬天花板（Victoria 当天撞限，Charlene/Gail 顺延）。
6. **验收** — Judi 补发（20:53）、Kevin 代发（21:10）均当场服务器端核验通过。

教学价值：例6 是"验收"这一步的范本——**UI 状态不是事实，核验才是**；例4/5 展示同一天内同一根因（双写者无共享状态）被两种形状的规则修掉。

## Practice task (small, low-load; feedback after each step)

Step 1: from the 7-item checklist already delivered (07:26Z), mark each: 我还在亲手做 / 已经自动了 / 不是我的事. (Still pending the user's reply.)
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

Two real situations, ranked by payoff:
1. **4 个新号的日常运营自动化** — today: ig-matrix-prep-daily added 步骤8 (one post per new page per day), plus two new scheduled tasks created and user-approved: fb-newpages-post-daily (daily ~18:45, post to own pages via FoxProfile) and fb-foxprofile-warm-daily (daily ~15:45, 6-env warm-up rotation). This is automation **scaling with the business**: from 3 号 to 7 号， the same playbook duplicated per identity. Transfer lesson: every new account arrives with a checklist (env + IP + page + prep + post + warm), not a manual scramble.
2. **海外6组每周数据汇总/周报** — same pattern as 例1, team-level payoff. Still unknown surface; ask when the user mentions team reporting friction.

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-10-23T19:56:05Z (24h, per study task plan). By then: user's checklist ticks received (or re-asked once); 例3 formalized as the first completed card on the goal timeline (needs a main-chat/goal-write turn); one next-pick card attempted; mastery still unestimated until at least three observed performances exist.

## Evidence strength & uncertainty

- **Tentative, strengthening**: three new same-day worked examples (4–6) observed and preserved; the checklist brief reached the user live (07:26Z) with the explicit "打勾即可" ask.
- Mastery unestimated: zero observed performances (user has not attempted retrieval or a five-field card).
- Uncertainty: whether the user's own-device posting friction ("自己发视频") is resolved — carried from the 10-22 note, still unasked. Do not claim it is.
- Uncertainty: which of the 7 checklist items the user still does by hand — pending his reply to the 07:26Z ask.

## Open questions for later studies

- Is the user's own "登录自己发视频" friction gone, or does it need the Mac pairing / a user-side flow?
- Which of the 7 draft items the user ticks as still-hand-done (pending since 2026-10-22T07:26Z); whether a gentle re-ask is warranted tomorrow.
- 例5 串行锁的下轮验证是否通过。
- Team-level （海外6组） recurring work surface: data rollups, weekly reports.
- Whether approval-popup batching ("先攒住、等你醒了点一下") should become a standing pattern rather than an ad-hoc workaround.

## Research Trajectory

- **External sources viewed**: none — this goal is user-specific; the evidence is the user's own conversation, goal state, and memory. No external lookup would change the note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-20/goal.md`, `.../2026-10-21/goal.md`, `.../2026-10-22/goal.md` (all read in full; carried forward the goal snapshot, standing constraints, worked examples 1–3, the teach-plan structure, and the 10-22 note's honest gap on "自己发视频").
- **Repetition search**: keyword variants {盘点清单, 任务卡, 评论单出口, 串行锁, 核验, 新号, fb-newpages-post-daily, 免扫码} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` (including brief filenames as topic index). 盘点清单 hits: 10-20 brief (the checklist itself) + 10-21/10-22 notes. 任务卡 hits: 10-19 brief + notes. 免扫码 hits: 10-22 note only. 评论单出口 / 串行锁 / fb-newpages-post-daily: **zero hits anywhere** — new to the goal's record. All three were nonetheless narrated to the user live in main chat today (user approved the split; saw the over-limit admission and the verification rule), so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-21T19:09:11Z → 2026-10-22T19:57:34Z, plus keyword searches on `重复工作自动化` / `盘点清单 自动化` / `定时任务 cron 能力 日程清单`. The goal-relevant turns: 06:26 capability/daily-schedule inventory, 07:26 checklist delivery (no reply), 13:35 summary ("还等你挑先做哪一项", no reply), 17:49 approval-popup boundary (new).
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan; mastery stays unestimated until at least three observed performances exist. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md (FoxProfile, account safety caps, verify-before-report); ALIGNMENT_SYNTHESIS.md (direct operator register; 10-22 alignment notes).
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract.
