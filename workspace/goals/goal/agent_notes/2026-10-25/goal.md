# Study Notes - 2026-10-25 - 重复工作自动化
<!-- studying-run-start: 2026-10-24T19:09:08Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and no reply to the checklist in the 2026-10-24 window either.
- Prior notes read in full: `2026-10-20/goal.md`, `2026-10-21/goal.md`, `2026-10-22/goal.md`, `2026-10-23/goal.md`, `2026-10-24/goal.md`.

## Already Covered in Main Chat

- 2026-10-24 17:56 Beijing: user set 视频先审后排 — every finished video must be shown to him first, and only enters the publish queue after he approves it.
- 2026-10-24 18:0x Beijing: user corrected the DM playbook — first messages must not feel like a broadcast, must not ask for a number up front, and the number-ask hook is now 秦浩医生线上远程视频面诊.
- 2026-10-24 18:06 Beijing: user set the precise approval-card trigger — if he has not clicked a card 3 seconds after it appears, Muse must WeChat him immediately.
- 2026-10-24 18:17 Beijing: user set 发后自评引流 — after each video publishes, the same account comments on it guiding viewers to the homepage WhatsApp link (no link or number in the comment itself).
- 2026-10-24 19:58 Beijing: user ordered 补发 of the three new-page text posts after the 18:45 round failed;补发 succeeded 20:14 Beijing, Jioklm still without usable video material.
- 2026-10-24 21:46 Beijing: assistant corrected the X p6 failure cause in the daily report — twitter-cli initialization failure, not the 344 platform limit claimed that morning, and the same tool fault recurred on 2026-10-19, 2026-10-20, and 2026-10-21.
- 2026-10-24 22:36 Beijing: user set the highest-priority reporting rule — any problem on any platform or account must be reported immediately in main chat plus WeChat, naming platform, account, problem, and whether he needs to act.
- 2026-10-24 23:17 Beijing: assistant reported Mellissa's 21:03 first DM was not sent (browser task timed out with no result, no thread exists), and Linnie behind her was therefore also untouched.

## What this study adds

Five new worked automation instances (例10–14), all from 2026-10-24 lived operations. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user.

Key observation: the user's automation judgment is now expressed as precise thresholds and service levels, not just directions. On 2026-10-23 he set rules ("platform signals only", "real-time, not every 15 minutes"); on 2026-10-24 he set numbers and gates (3 seconds, immediate, review-before-schedule). A second shift: delegation within rules — for the five rewritten DM drafts he said "你决定就行" (2026-10-24 18:17 Beijing), moving from逐条点头 to deciding inside rules he set. That is the trust pattern this goal should track: rule-setting first, then delegated execution inside the rule.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, third day.
2. Standing constraints — **present, expanded by four on 2026-10-24**:
   a. Approval/permission popups are system-level; the agent cannot bypass or auto-approve them (2026-10-22).
   b. Guardrails must be platform-verified signals only; self-invented numbers deleted (2026-10-23).
   c. **NEW**: approval-card escalation trigger is exactly 3 seconds unclicked → WeChat immediately (2026-10-24 18:06 Beijing); the trigger applies to every task, not just DM sends, after the 2026-10-24 finding that cards timed out 15:45–16:34 Beijing with no WeChat call.
   d. **NEW**: any problem, any platform, any account → report immediately in main chat + WeChat with platform, account, problem, and whether the user must act; never deferred to a daily report (2026-10-24 22:36 Beijing).
   e. **NEW**: publish pipeline gates — video review-before-schedule (user approves before queueing) and post-publish self-comment guiding to the homepage WhatsApp link (2026-10-24 17:56 and 18:17 Beijing).
3. Low-risk pilots demonstrated — **now fourteen worked examples** (例1–14 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–9 carried from the 10-24 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23).

**例10：审批卡 3 秒微信触发（2026-10-24，当天真实事件）**
1. **盘点** — 2026-10-24 15:45–16:34 Beijing 一批审批卡超时无人点，Muse 没有微信喊用户；用户指出"今天你就没发过"。
2. **拆解** — 2026-10-23 的规则只说了"弹卡就微信喊"，没有给时间刻度，执行者按"超时了才喊"理解，正好与用户的意思相反。
3. **量化** — 用户定死刻度：卡弹出后 3 秒未点 → 立刻微信喊人，不等超时。
4. **自动化设计** — 该口径须写进猎手与私信两个任务正文（2026-10-24 当天曾因任务文本安全检查未通过而暂未写入，待用户点头后补写 — 本条是当日遗留动作）。
5. **边界** — 微信喊人替代不了点卡动作本身；"始终允许"只按收件人/类别生效，Lucy 的始终允许不管 Gail 的卡。
6. **验收** — 口径已记入记忆；任务正文补写尚未完成。

教学价值：规则没有时间刻度就等于没有规则；"第一时间"必须翻译成秒数才可执行。

**例11：有问题第一时间讲（2026-10-24，用户发火后定的最高优先规则）**
1. **盘点** — 两笔拖延账：Lucy B-18 审批卡 21:05 Beijing 弹出、用户 22:34 才批（近 90 分钟无人喊）；X 当天 p6 发帖失败拖到 21:45 日报才讲原因。
2. **拆解** — 汇报被批量推迟到日报，问题在等待中继续产生损失（Mellissa 首条未发、Linnie 被连带拖住）。
3. **量化** — 报告必须包含四样：哪个平台、哪个账号、出了什么问题、要不要他动手（点卡/重登/别的）。
4. **自动化设计** — 主聊天讲 + 微信同步喊，双通道；不许拖到日报、汇总才讲，不许只报"失败了"不讲原因和下一步。
5. **边界** — 该规则覆盖所有平台与账号，不只 FB 私信与 X。
6. **验收** — 当晚 23:17 Beijing Mellissa 未发即按此规则即时汇报（查到立刻讲），是规则生效后的第一个实例。

教学价值：这是本目标的元规则 — 自动化系统的故障报告本身也需要自动化（事件驱动、双通道、固定格式），而不是等日报轮询。

**例12：发布流水线的两道门（2026-10-24，当天真实事件）**
1. **盘点** — P0 样片：用户 17:56 Beijing 拍板"发吧"后才进 19:45 轮，19:45 发出并核验（音轨 1 条、无平台音乐、无静音），发完即按新规在评论区留引导评论。
2. **拆解** — 此前发布队列是"备好即排期"，用户在成品环节没有否决点；误发风险（如 2026-10-24 早上的假对比成品）只能靠事后隔离。
3. **量化** — 两道门：门一，确定好的视频先发用户看、用户点头才排期；门二，发完本号在评论区留一句引导点主页 WhatsApp 链接（评论本身不贴链接、不贴号码）。
4. **自动化设计** — 排期动作的前置条件改为"用户确认"；发完动作的后置步骤固定为"自评引流评论"。
5. **边界** — 未经用户确认的视频不许进队列、不许自动发；自评引流只适用于自家帖子（别人帖子评论区带链接仍是红线）。
6. **验收** — P0 是首条按此走的成品，19:45 发出 + 评论区引导已落地。

**例13：FoxProfile 链路抖动与重启补发（2026-10-24，当天真实事件）**
1. **盘点** — 15:45 养号轮 6 个号只跑成 1 个（Emerson）；18:45 四个新主页 0 条发出（Jioklm 缺料、Jusa 代理启动抖动、Simon/Cora 首页导航超时）。
2. **拆解** — 直连测代理都是通的，抖动在 FoxProfile 启动链路，不在账号本身（无 checkpoint、无验证码）；与 2026-10-23 的代理抖动同一家族。
3. **量化** — 用户 19:58 Beijing 下令补发；链路复测通后补发轮次跑通，20:14 Beijing 三条文字帖全部发出，中间 FoxProfile 服务崩过一次、重启后成功。
4. **自动化设计** — 定时任务的"跑了"不等于"发了"：每轮必须以服务器端可查的发出结果验收；失败轮次要有重启 + 补发路径，而不是等下一天。
5. **边界** — Jioklm 无合格视频料，补发也补不了 — 缺料与链路故障是两类失败，不可互相顶替。
6. **验收** — 三条文字帖链接已核验发出；Jioklm 仍待新料。

附带实例（同一验收原则）：Mellissa 21:03 首条浏览器任务超时无结果 → 按规矩不算发了、无线程即未发，下一轮重新处理，不重复发。

**例14：X p6 归因纠错（2026-10-24，当天真实事件）**
1. **盘点** — 早上称 p6 未发是撞 344 平台限额；21:46 Beijing 日报纠正为工具端 twitter-cli 初始化故障，根本没到 X 的发帖接口。
2. **拆解** — 344 是平台信号，初始化失败是工具故障；两者停手含义完全不同（前者等窗口，后者修工具）。
3. **量化** — 同一故障在 2026-10-19、2026-10-20、2026-10-21 都出现过，是老毛病而非偶发。
4. **自动化设计** — 故障归因必须以实测/台账为准，日报纠正上午的说法；工具老毛病列入待根治项，下次 10:45 再试 p6 时看结果再报。
5. **边界** — 账号会话正常，用户无需重新登录 — 纠错同时排除了一个错误动作（重登）。
6. **验收** — 日报已以台账为准；根治结论尚未出。

教学价值：例14 与例6 同源 — 验收不仅验"发没发"，还要验"为什么没发"，归因错了，停手策略就全错。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, third day): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24**: 18:45 轮 0/4 发出后经重启 + 补发救回 3 条文字帖；Jioklm 仍缺合格视频料。Transfer lesson confirmed again: 定时任务需要失败 → 重启 → 补发的闭环，缺料不可用别的料顶替。
2. 私信首接的事件驱动升级 — done as 例8; 2026-10-24 的新候选面：审批卡触发的双通道即时汇报（例10/11）已成规则，下一个可复用的面仍是海外6组每周数据汇总/周报（仍是未知面，等用户提团队汇报摩擦时再问）。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-10-25T19:09:08Z (24h, per study task plan). By then: 例10 的任务正文补写是否完成；例5 串行锁的下轮验证结果；X p6 根治结论；Jioklm 是否有新料；是否仍无 checklist 回复（若仍无，建议不再单独追问 — 2026-10-24 的规则制定本身已是实质进展，单独追问只会增加噪音）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: five new same-day worked examples (10–14) observed and preserved; the user's automation rules are now stated as precise thresholds (3 seconds, immediate, review-before-schedule).
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now number five user-articulated design decisions (例7, 例8, 例10, 例11, 例12), but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: 例10 的任务正文补写在 2026-10-24 当天因安全检查未完成，是否已补写未知；例5 串行锁的下轮验证结果仍未知；X p6 工具故障的根治方案未知；21:00 解冻是个约数、Mellissa 与 Christina 的时区核验细节未变。
- Uncertainty: checklist ticks pending (third day); the 10-24 note's "re-ask once tomorrow" now falls due, but the user spent 2026-10-24 setting rules live — a separate nag is judged lower value than the rules themselves.

User quotes preserved verbatim (evidence for the new rules):
- "以后你确定好的视频都要给我看一下我确定没问题你再排期" (2026-10-24 17:56 Beijing)
- "在你发送审核发过后，三秒以内如果说我没有点击审核卡的话，你就给我微信发消息" (2026-10-24 18:06 Beijing)
- "有问题你必须得第一时间跟我讲，无论是哪个平台遇到问题哪个账号有问题你就必须得给我讲" (2026-10-24 22:36 Beijing)

## Open questions for later studies

- Checklist ticks: re-ask decision due — recommendation above is to let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now five candidates exist, so the decision matters more than the count.
- 例5 串行锁的下轮验证是否通过；例10 任务正文补写是否完成；X p6 工具故障是否根治。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate now touches the same pipeline, so ask in that context, not as a separate item.)

## Research Trajectory

- **External sources viewed**: none — this goal is user-specific; the evidence is the user's own conversation, goal state, and memory. No external lookup would change the note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-20/goal.md`, `.../2026-10-21/goal.md`, `.../2026-10-22/goal.md`, `.../2026-10-23/goal.md`, `.../2026-10-24/goal.md` (all read in full; carried forward the goal snapshot, standing constraints, worked examples 1–9, the teach-plan structure, and the 10-24 note's open questions on 例5, the checklist re-ask, and formalizing cards).
- **Repetition search**: keyword variants {3秒, 微信喊人, 第一时间, 先审后排, 自评引流, FoxProfile, 补发, 面诊, 广播, 超时} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` (filenames included; briefs dir lists exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡， `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单）. 3秒 / 先审后排 / 自评引流 / 面诊 / 广播： **zero hits anywhere** — new to the written record. 微信喊人 / 第一时间 / 超时： hit only in the 10-24 note (general WeChat escalation, not the 3-second precision or the immediate-report rule). FoxProfile / 补发： hits in earlier notes (FoxProfile login, DM re-sends) but not today's chain-jitter + restart-recovery instance. Every one of today's instances was set by the user or narrated to him live in the 2026-10-24 main chat, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-23T19:29:15Z → 2026-10-24T19:09:14Z. The goal-relevant turns: video review-before-schedule (17:56 Beijing), DM no-broadcast correction + video-consult hook (18:0x Beijing), 3-second WeChat trigger (18:06 Beijing), post-publish self-comment rule (18:17 Beijing),补发 order and result (19:58 / 20:14 Beijing), X p6 cause correction (21:46 Beijing), immediate-report rule (22:36 Beijing), Mellissa timeout report (23:17 Beijing).
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md (2026-10-24 entries: 3-second WeChat trigger, immediate-report rule, video review-before-schedule, no-broadcast DM rule, video-consult hook, post-publish self-comment); memory search on 重复工作自动化 / 审批卡微信3秒 / 视频先审后排 confirming the checklist is still pending since 2026-10-19 and the old 10-19 draft was superseded by the 10-20 brief.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract.
