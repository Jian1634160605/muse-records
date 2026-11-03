# Study Notes - 2026-10-20 - 重复工作自动化
<!-- studying-run-start: 2026-10-19T19:26:40Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z (12:51 CST) at the user's own request in main chat; current_state: 已定下目标，下一步先盘点现有重复工作清单.
- Description: 把每天、每周重复做的工作自动化掉，不再靠人力硬扛。从盘点开始：列出所有重复事项，逐个改成自动流程或交给我来执行，让时间花在真正需要人的地方。
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (zero observed performances so far); evidence label `tentative`.
- No prior study notes and no prior briefs exist for this goal (both directories verified empty).

## Already Covered in Main Chat

- User chose this goal from efficiency options Muse floated: "重复性工作太多，想自动化" (user, 2026-10-19T04:50:59Z).
- Muse created the goal and set milestone 1: user lists daily/weekly hand-done repetitive tasks; Muse ranks them by 耗时×频率 and automates them one by one (assistant, 2026-10-19T04:51:50Z).
- User acknowledged ("好") but has NOT yet sent the task list (still pending at run end).
- GOAL.md constraints recorded: automation must not touch steps needing human judgment （谈单、咨询转化、出镜拍摄）; new automations go live only after user confirmation; no new cron jobs added without approval; existing account safety rules (X 1 post/day, FB no cold DMs) carry over.

## What this study adds

- First study pass for a brand-new goal: repetition search found zero prior notes/briefs, so everything here is new record, not re-confirmation.
- Consolidated the user's standing automation baseline from GOAL.md + memory (X crons fully running: x-viral-daily, x-promo-retry-p1, x-engage-daily, x-post-acct1-daily, x-daily-report; FB 秦浩 IP stack: content / hunter interception / 3h lead radar / reports; TikTok @faciallifting.qinhao just handed over; one Muse-written weekly report already piloted 2026-10-19). This baseline is the proof the pattern works and anchors the worked example.
- Sharpened the single open blocker: milestone 1 depends entirely on the user's pending task list. The note preserves a concrete one-task-card template so the ask is actionable, not abstract.
- For the novice teach plan: prerequisites, retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check, and next review are all preserved below.

## Prerequisite check

Before teaching new material, confirm prerequisites:

1. A concrete inventory of the user's recurring tasks — **MISSING**. This is the one gap to close first; nothing new gets automated until the list exists.
2. Standing constraints recorded — **present** (GOAL.md: no automation of human-judgment steps; user confirmation before any new automation goes live).
3. A low-risk pilot already demonstrated — **present** (weekly report written by Muse once, 2026-10-19).

Surface the missing inventory as the first thing to close. The retrieval prompt and practice task below are designed to make that ask concrete.

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。"

## Worked example (fully worked, every step labeled)

Real case, already piloted once on 2026-10-19: the team weekly report （周报）.

1. **盘点 (inventory)** — The recurring task: weekly team report, every Monday. Trigger: boss needs the numbers. Inputs: data-table screenshot the user uploads. Outputs: PPT page 2 + 板块二文案 + one-page PDF 战报图.
2. **拆解 (decompose)** — Read the data → fill four fixed sections （上周总结 / 存在问题 / 下周安排 / 工具推荐） → translate jargon into boss-readable plain language （截流→"去同行评论区找意向客户", 起号→"账号冷启动"） → export files.
3. **量化 (size it)** — 耗时×频率. The pilot took several rewrite rounds (first draft mixed up X-business content with 医美引流留资； the rewrite landed). Note: the expensive step was the plain-language translation, not typing.
4. **自动化设计 (design)** — Fixed template (four sections + plain-language rule) + pinned data source (numbers come only from the user's own table — verify-before-report, never fabricated) + Muse drafts → user reviews → user uploads.
5. **边界 (boundaries)** — Numbers only from user data; final wording approved by user before upload; no new cron without explicit confirmation.
6. **验收 (validate)** — One successful pilot. Next: time-per-report trends down, rewrite rounds trend down.

Check-your-understanding hook: the user's own phrasing in chat ("列几条发我，我按耗时×频率排个序，咱们一个一个干掉") already names steps 1 and 3. Ask the user which of the other four steps they can spot in the pilot.

## Practice task (small, low-load; feedback after each step)

Write ONE task card for a single recurring task this week, in five fields:

- 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）

Starter the user can copy: 任务名=每天看 X 账号数据；触发=每天早上；输入=账号后台截图；输出=三个数字发群里；耗时=10分钟.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

Point at the real situation — the pending inventory itself: "从你自己的清单里挑一个最烦的（比如收数据、做表、回消息、整理素材），按 task card 写出来发我，我来判断能不能交给我。" Team-level version: 海外6组每周的数据汇总/周报 — same pattern, bigger payoff.

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding.

## Next review

2026-10-20T19:26:40Z (24h). By then: user task list received or re-asked; first task card completed; mastery still unestimated until at least three observed performances exist.

## Evidence strength & uncertainty

- **Tentative**: single conversation touchpoint; the inventory — the core evidence for this skill — is still pending from the user.
- Mastery unestimated: zero observed performances.
- Standing constraints any later Letter must respect: all user-facing text in Chinese; every approval explained in Chinese before the popup appears; new automations need explicit user confirmation before going live.

## Open questions for later studies

- Which tasks the user actually does by hand daily/weekly (the pending list).
- Team-level （海外6组） recurring work surface: data rollups, weekly reports, material organization.
- Whether the user prefers the inventory collected by interview (Muse asks) or self-report.

## Research Trajectory

- **External sources viewed**: none — this goal is user-specific and was created 2026-10-19; no external lookup would change the note.
- **Prior trajectories reviewed**: none — `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` are both empty (verified by directory listing and grep).
- **Scaffolds and support tactics**: no scaffold registry was available in this step's inputs, so no tactic labels were applied. The teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get`; constraints read from `workspace/goals/goal/GOAL.md`.
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md / MEMORY.md standing context (Chinese-only requirement; approval explanations in Chinese; verify-before-report); `memory/2026-10-19.md` L175–199 (goal-creation log: milestone 1 pending user list, constraints); people/groups indexes consulted only to use corrected team-member names （江茜茜 / 蔡园庆） accurately in context.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Repetition search executed: keyword variants {重复工作自动化, repetitive work automation, 盘点重复工作清单, automation} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/`, plus filename listings of both directories — zero hits.
