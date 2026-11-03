# Study Notes - 2026-10-21 - 重复工作自动化
<!-- studying-run-start: 2026-10-20T19:12:08.071758+00:00 -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request in main chat; current_state: 已定下目标，下一步先盘点现有重复工作清单.
- Description: 把每天、每周重复做的工作自动化掉，不再靠人力硬扛。从盘点开始：列出所有重复事项，逐个改成自动流程或交给我来执行，让时间花在真正需要人的地方。
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (zero observed performances so far); evidence label `tentative`.
- Prior note exists: `workspace/goals/goal/agent_notes/2026-10-20/goal.md` (read in full this run). Prior brief exists: `workspace/goals/goal/briefs/Brief (2026-10-19 19.34.10).html` (read in full this run).

## Already Covered in Main Chat

None found. The entire window (2026-10-19T19:26:39Z to 2026-10-20T19:14:50Z) was about IG/FB/TikTok/X operations and the Personal Agent PPT rework; neither the user nor the main agent mentioned 重复工作自动化, the task-card ask, or the pending task list.

## What this study adds

The decisive new finding: milestone 1's blocker ("等待用户自己列出重复工作清单") no longer needs to be the plan. Today the user's repetitive work is directly observable from a full day of conversation — Muse no longer has to wait for a self-reported list. It can **draft the candidate 盘点清单 from evidence** and hand it to the user to confirm/edit. That changes the plausible next move for this goal: from passive waiting to an evidence-backed draft.

Candidate list drafted from today's window (all grounded in the conversation fetched this run):

1. **三平台每日发布流水线** — 每天 09:45 自动备料（从 @tan.iasampson 挑 Top 3、SaveFrom 下载），做差异版+水印+文案，17:45/19:45/22:45 三轮定时发 IG + TikTok + FB，发完汇报链接。用户已明确授权 "后续你就自己找，找到合适了的就自己做好排好期自己发" (2026-10-20T07:51:02Z, msg fc96d4d5)。2026-10-20 当天三轮全部发完（r1 links IG p/DetWf3atGPS, TikTok 7698655730760551700, FB reel 1439061491530501; r3 TikTok 7698762148239117589, FB 873312822537059）。**已基本自动化**（ig-matrix-prep-daily / ig-matrix-post-r1/r2/r3 cron 族在跑）。
2. **获客巡查** — IG/TikTok 每 1 小时扫评论和私信（用户把 2h 压缩到 1h, 2026-10-20T07:49:00Z, msg 2cce5d3d），拿到客资立刻通知+记台账；FB 3 小时客资雷达 (fb-lead-scan)。TikTok 10-20 上午真实私信 marvinsansan 的 "hi" 已按流程回复。**自动化运行中，覆盖范围是逐日手动调大的**（值得复盘：巡查频率决策是规则化的，还是人凭感觉的）。
3. **账号养号** — TikTok/IG/FB 每天早晚两场真人式刷视频。10-20 当天 TikTok 被弹 11 次人机验证（80 分钟内），用户授权 "继续自动刷，被验证你接管浏览器过" (2026-10-20T11:34:52Z, msg f8d08954)。**自动化的，但属于高运维成本**——验证接管需要用户在线配合浏览器，流程有脆弱点。
4. **FB 猎手截流 + 每日互动** — 6h 一次的同行评论截流、每日互动任务，两轮曾重发同一评论区（R1/R2 与 T2/T3 重叠），已修成共用去重台账 (2026-10-20T12:28:48Z)。**昨天还是 bug，今天成了自动化台账规则**——是很好的"一个一个干掉"实例。
5. **X 双号运营** — 每号每天 1 帖、21:45 中文日报、互动上限 30。当天大号 acct1 撞 226 停手、acct2 疑似账号级限制（粉丝 5→0）。**自动化运行中，带风控熔断**。
6. **PPT 反复改版循环** — 当天最重的手动耗时。Personal Agent PPT 从 14 页 v1 逐版改到 20 页"顺序版"，经历 7 次用户反馈轮次：加图 (217bfe67) → 原生绘制要求 (msg f9f29707, 12:22Z) → 豆包风格借鉴 (msg 5868d288, 12:29Z) → 顺序错乱 (msg 4d837308, 13:34Z; msg 134b576b, 13:58Z) → 逐页拼图核对 (assistant-msg-aa27a176) → 新音乐规后重排。每一轮用户都在纠同样的事：**顺序**。这件事今天花了用户大量的注意力和往返。**自动化切入点最深的候选**：版式模板化 + 顺序约束规则 + 每页自动验（逐页渲染检查 Muse 已在做，但顺序核对靠的是用户肉眼）——下一次同类 PPT（团队周报、客户提案）可以直接套。
7. **一次性的手动卡点** — IG 主页链接只能手机 App 加（网页版"网站"栏被 IG 禁用，assistant-msg-0d01ebfd）；FB 帖子被设成 private 得用户手动改 audience (assistant-msg-44bb06e2)。**属于"本来就知道但绕不过平台"的**——记下来是为了下次直接告知，而非反复排查。

Two transfer-ready automation wins observed today that the prior note's worked example (周报) didn't have:
- The **dedup ledger fix** (FB 双任务重发 → 共用去重台账) is a clean second worked example of 盘点→拆解→量化→自动化→验收 inside this run's own window.
- The **音乐新规** (2026-10-20 15:35Z, msg ebee2316): "备料阶段直接换好音乐，三个成品交叉配乐，发布时直接传成品，不再进各平台曲库找音乐" — a standing-rule automation that eliminated a recurring manual decision (which song per post per platform) plus a daily bug (TikTok 没加音乐的遗漏). This shows the user accepts **规则化代替逐条决策** — which is exactly the automation pattern the goal is teaching.

Constraint check (from GOAL.md + standing context, all still holding): no automation of human-judgment steps （谈单、咨询转化、出镜拍摄）; new automations go live only after user confirmation; no new crons without approval; all user-facing text Chinese-only; safety caps (X ≤1 post/day/acct, FB no cold DMs).

## Prerequisite check

1. A concrete inventory of the user's recurring tasks — **previously MISSING; now CLOSABLE without the user**. Today's conversation supplies a full day's worth. The draft above is the candidate; next move is to hand it to the user for confirmation/editing rather than waiting for them to write one from scratch.
2. Standing constraints recorded — **present** (GOAL.md: no automation of human-judgment steps; user confirmation before any new automation goes live).
3. Low-risk pilots demonstrated — **present, now plural**: 团队周报 (2026-10-19 pilot), FB 去重台账 (2026-10-20), 音乐交叉配乐规则 (2026-10-20).

The first thing to close is no longer "wait for the list" — it is "present the draft list and let the user veto/edit."

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。"

## Worked example (fully worked, every step labeled)

Now two examples; keep example 1 from the prior note, add example 2 from today.

**例1：团队周报（2026-10-19 pilot，未变，沿用上一期）** — 盘点：每周一的团队周报；拆解：读数据→填四板块→术语翻译成人话→导出文件；量化：最贵的是改稿轮次（第一版把 X 业务和医美引流写混了）；自动化设计：固定模板+只用用户自家数据（verify-before-report）+Muse 起草→用户过目→用户上传；边界：数字只来自用户数据，终稿用户确认；验收：一次成功试点，后续看改稿轮次下降。

**例2：FB 猎手/互动重发 bug（2026-10-20，当天真实事件）** —
1. **盘点** — 每 6h 的同行截流 + 每天的互动任务，两个任务都会回评论。
2. **拆解** — 读高意向评论 → 写专家式回复 → 发布 → 记录链接。
3. **量化** — 2026-10-20 晚上两个任务前后脚跑，踩中同一评论区：Truesdale 61 岁帖和布里斯班帖都出现了我们两条回复（内容合规，但显得不自然）。耗时不大，风险是信誉。
4. **自动化设计** — 两个任务共用一个去重台账，每轮先查再回，不双发。
5. **边界** — 台账只记已回评论区的 URL；专家式回复内容仍逐条人写（判断类，不自动化）。
6. **验收** — 规则当天落地，验证方法：下一次双任务都跑完后抽查是否有同一 URL 出现两次。

例2 的教学价值：它展示了"自动化"不只是定时任务——把一个**人工规则写进台账检查流程**也算自动化。

## Practice task (small, low-load; feedback after each step)

Updated for the new evidence: the user no longer starts from a blank page.

Step 1: present the 7-item draft list (above) and ask the user to mark each as "我还在亲手做" / "已经自动了" / "不是我的事".
Step 2: from the items they marked "我还在亲手做", pick the most annoying one and write ONE task card in five fields: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=改 PPT 顺序；触发=每次收到 PPT 初版；输入=初版文件；输出=按"开篇→目录→第一部分→第二部分→第三部分→第四部分→总结→谢谢观看"排好的文件；耗时=40分钟.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

"从上面这 7 条草稿里，挑一个今天你感觉最烦的——我猜是 PPT 改版——按 task card 写出来发我，我来判断能不能交给我，或者能不能变成一条规则（比如 音乐新规那样）。" Team-level version: 海外6组每周的数据汇总/周报 — same pattern, bigger payoff.

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding.

## Next review

2026-10-21T19:12:08Z (24h). By then: draft list presented and user feedback received (which items they still do by hand); first task card attempted from the confirmed items; mastery still unestimated until at least three observed performances exist.

## Evidence strength & uncertainty

- **Tentative, but stronger than yesterday**: the inventory was the core missing evidence; it is now drafted from a full day's observation, pending user confirmation. The draft list is grounded in today's conversation; team-level （海外6组） recurring work is still unknown.
- Mastery unestimated: zero observed performances (user has not yet attempted retrieval or a task card).
- Standing constraints any later Letter must respect: all user-facing text in Chinese; every approval explained in Chinese before the popup appears; new automations need explicit user confirmation before going live; no automation of 谈单/咨询转化/出镜拍摄.

## Open questions for later studies

- Which of the 7 draft items the user actually does by hand (confirmation pending).
- Team-level （海外6组） recurring work surface: data rollups, weekly reports, material organization.
- Whether the PPT rework pattern is the highest-value first automation, and whether the user wants the "顺序约束+模板+逐页自检" package for the next deck.
- Whether patrol-frequency decisions （如 2h→1h) should become rule-based rather than user-felt.

## Research Trajectory

- **External sources viewed**: none — this goal is user-specific; the evidence is the user's own conversation and goal state. No external lookup would change the note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-20/goal.md` (read in full; carried forward the goal snapshot, GOAL.md constraints, worked example 1, and the teach-plan structure) and `workspace/goals/goal/briefs/Brief (2026-10-19 19.34.10).html` (read in full; its center was "第一张任务卡": the weekly-report worked example plus the ask for the user to write the first task card).
- **Repetition search**: keyword variants {任务卡, 盘点, 自动化, 重复, automation, inventory, repetitive, task card} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` (including filenames as a topic index). Both variants hit the same two files already read; the prior brief covered the task-card ask and worked example 1 only — it did not contain the observation-drafted candidate list, the FB dedup-ledger example, or the music-rule example. The recent conversation (fetched via muse.context_fetch, window 2026-10-19T19:26:39Z–2026-10-20T19:14:50Z) held nothing about this goal; all evidence above is new-to-the-goal observation, not conversation repetition.
- **Scaffolds and support tactics**: no scaffold registry was available in this step's inputs, so no tactic labels were applied. The teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan; mastery stays unestimated until at least three observed performances exist. No learning-style claims were made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get`; constraints read from `workspace/goals/goal/GOAL.md`; conversation read via `muse.context_fetch` (conversation category).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md (account safety caps, verify-before-report, standing redlines); ALIGNMENT_SYNTHESIS.md (direct operator register, delegation datedness).
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract.
