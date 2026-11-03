# Study Notes - 2026-10-26 - 重复工作自动化
<!-- studying-run-start: 2026-10-25T19:13:27Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed.
- Prior notes read in full: `2026-10-20/goal.md`, `2026-10-21/goal.md`, `2026-10-22/goal.md`, `2026-10-23/goal.md`, `2026-10-24/goal.md`, `2026-10-25/goal.md`.

## Already Covered in Main Chat

- 2026-10-25 Beijing afternoon: user approved the seven-part FB operating strategy ("我觉得可以"), and the main agent stated that approval covers only the strategy, not that day's v1/v2 videos, the Qin Hao material timing, or the puppet-animation length.
- 2026-10-25 Beijing afternoon: the main agent hardened four publish tasks with a "用户已批准" gate, moved Victoria's video destination from the personal timeline to the Dr.qh88 Page, and fixed the new-pages prep path; that evening's 17:45, 18:45, and 19:45 rounds all skipped by the gate, so Victoria published 0 videos that night.
- 2026-10-25 Beijing afternoon: all six FoxProfile environments were verified logged in with correct Page identities, including Cora via a 45-second wait for its old tabs to restore; the hunter task-text rotation update was explicitly deferred pending a re-check of the original text.
- 2026-10-26 00:26–00:46 Beijing: user asked whether the GitHub automatic-editing tools dulaautoclip and then autoclip could be used for the project's clipdraft Skill, and the main agent evaluated both, concluded zhouxiaoka/autoclip is a usable single-link candidate while Dula Clip AI is not recommended, and left a live test pending the user's go-ahead.
- 2026-10-25 Beijing afternoon: user asked whether Codex can be used on this machine and whether it is needed; the main agent answered it is installed (0.164.0-alpha.9) but not logged in, login needs the user's own OpenAI/ChatGPT account, and it is not needed for current operations work.
- 2026-10-25 Beijing morning: X p6 was sent successfully, and X interaction later hit the 344 daily limit again and stopped for the day.

## What this study adds

Three new worked automation instances (例15–17), all from 2026-10-25 lived operations and the 2026-10-26 00:26–00:46 Beijing autoclip discussion. All were raised by the user or narrated to him live — they are new to the goal's written record, not new to the user.

Key observation: the 2026-10-24 review-before-schedule rule has now hardened from a stated gate into a task-text precondition, and its first night produced a clean negative result (0 posts, by design, not by failure). A second shift: the user is now bringing external automation candidates himself (autoclip/Dula), so this goal's next work is evaluation and adoption decisions, not only rule-setting. The evaluation pattern is also now explicit and reusable: licence, callable interface, local-machine feasibility, and project-claim consequences.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged.
2. Standing constraints — **present, expanded by two on 2026-10-25/26**:
   a. Approval/permission popups are system-level; the agent cannot bypass or auto-approve them (2026-10-22).
   b. Guardrails must be platform-verified signals only; self-invented numbers deleted (2026-10-23).
   c. Approval-card escalation trigger is exactly 3 seconds unclicked → WeChat immediately (2026-10-24 18:06 Beijing); whether the 2026-10-24 task-text补写 for that trigger is complete is still unconfirmed in this window.
   d. Any problem, any platform, any account → report immediately in main chat + WeChat with platform, account, problem, and whether the user must act (2026-10-24 22:36 Beijing).
   e. Publish pipeline gates — video review-before-schedule and post-publish self-comment guiding to the homepage WhatsApp link (2026-10-24 17:56 and 18:17 Beijing).
   f. **NEW**: publish tasks now require a "用户已批准" marker in the task section itself; queue-file existence alone no longer triggers a publish (2026-10-25 Beijing afternoon).
   g. **NEW**: external-tool adoption test — licence, CLI/library callability, local-machine feasibility (2-core CPU, no GPU), and the effect on the project's "全原创" claim must all be checked before adoption (2026-10-26 00:26–00:46 Beijing).
3. Low-risk pilots demonstrated — **now seventeen worked examples** (例1–17 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–14 carried from the 10-25 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24).

**例15：发布任务的"用户已批准"硬门槛（2026-10-25，当天真实事件）**
1. **盘点** — r1/r2/r3 的任务正文原来没有先审门槛，只认队列里有没有文件；而 2026-10-25 的 v1/v2 文件已经躺在队列里，按原样当晚 17:45、19:45 会直接发出去。
2. **拆解** — 2026-10-24 定的是"先给用户看、点头才排期"的口头规则，任务正文的前置条件没有同步改，规则与执行条件脱节。
3. **量化** — 四个任务正文都改了：无"用户已批准"标记一律跳过并报告，绝不自动发；Victoria 目的地从个人时间线改到主页 Dr.qh88，以主页身份发 Reel，发不成就跳过、不退回个人号；新主页轮备料路径 bug 修掉（原来指向 pages/ 子目录，实际文件在队列根目录，很可能就是 2026-10-24 晚 18:45 那轮 0/4 的原因）。
4. **自动化设计** — 排期动作的前置条件改为任务节里的批准标记；发完动作的后置步骤仍是自评引流评论。
5. **边界** — 用户什么都不做时，四轮（17:45、18:45、19:45、22:45）没点头的视频一律跳过；跳过不是故障，是门槛在起作用。
6. **验收** — 当晚三轮如数跳过：17:45 r1 没启动浏览器、没发、没写发布记录；18:45 新主页轮料齐（Jioklm 视频、Jusa 文字、Simon 文字、Cora 视频）仍因无批准而跳过；19:45 r2 同样跳过。Victoria 当晚 0 条。

教学价值：口头规则必须落到执行条件里才算自动化；"没发"需要区分"门槛拦截"与"链路故障"，否则下一次复盘会把正确的拦截当成故障去修。

**例16：autoclip / Dula Clip AI 的接入评估（2026-10-26 00:26–00:46 Beijing，用户主动提出，未采纳）**
1. **盘点** — 用户先问 "dulaautoclip 这个 github 的自动剪辑工具我们的项目能用吗"，随即纠正为"自动剪辑，不是自己剪辑"；又问 "autoclip 这个呢"，并先后发来两条抖音视频链接。
2. **拆解** — "我们的项目"在主代理的对齐里是 clipdraft 的 AI 自动剪辑 Agent Skill：8 阶段流程（素材盘点→审查确认→文案→剪辑蓝图→达芬奇时间线构建→成片审计→补拍建议），配 ffprobe 黑帧/静音检测，pytest 20/20 全过，但本机没 Resolve、时间线那步只跑过 dry-run。
3. **量化** — 评估框架四点：协议、CLI/库可调用性、本机跑不跑得动、全原创口径。zhouxiaoka/autoclip 经 README 核实：MIT 协议，约 9.7k star（本研究打开时显示 9,716），有 CLI 与 MCP，`autoclip produce 素材.mp4 --srt 字幕.srt --platform douyin --json` 直接出 JSON，本地 CLI 只要 Python + FFmpeg、不要 Redis；无字幕时走本地 Whisper，在 2 核机上会很慢，有现成字幕可用 `--srt` 跳过转写；云端文字模型实测一条 1 小时 43 分的片出 10 条约 ¥0.09。
4. **自动化设计** — 结论是"借一环，不整体替换"：clipdraft Skill 可借它的 AI 选段一环（Skill 现在缺的真能力），竖裁跟拍与烧字幕也可对接；但 FB 每日线不适合，因为它是按字幕打分、跟拍说话人设计的，而手术过程型素材的价值在画面阶段不是台词，且它默认加品牌片尾、自动出封面文案，须关掉或丢弃，也过不了选片红线与先审门槛。
5. **边界** — Dula Clip AI 不是同一产品，不建议接：闭源、没有 CLI 接不进 Skill 流程、移动端工具、发行只走"热门软件合集/余温宝库"文件包、无官网/GitHub/直链、"免费获取"未证实价格与内购条款；只建议用户自己在平板上玩，不装到主力工作机。两条抖音的出处也已区分：图寻不熬夜 2025-10-05 视频推荐的正是 zhouxiaoka/autoclip（画面地址栏 github.com/zhouxiaoka/autoclip）；入目无他 2026-06-03 视频讲的才是 Dula Clip AI（21 条汽车片段剪出 13.5 秒）。
6. **验收** — 未验收：实测（拿一条带字幕素材跑 produce 看 JSON 结构与耗时）仍等用户点头；一旦接入，Skill 的口径须从"全原创"改为"原创流程 + MIT 第三方剪辑引擎"并注明来源。主代理此前"dulaautoclip 搜不到、疑为记混"的说法已被第二条视频纠正。

教学价值：外部工具的"能用"要拆成"哪一环能用"；通用词重名（auto clip）是最容易误判的点，出处必须按产品逐个核实，不能按名字合并。

**例17：六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法（2026-10-25，当天真实事件）**
1. **盘点** — 多号轮换上线的第一步是核验登录态；首轮核验 6 个号一个都没确认：Fowler、Emerson、Jioklm、Simon 报代理不通，Jusa、Cora 能拉起浏览器但 FB 页面加载超时。
2. **拆解** — 主代理亲自直连实测四条代理线，facebook.com 全通，说明线路没死，问题在 FoxProfile 拉起浏览器这一步（前一天也抖过几次），不是账号会话掉了、不是代理商问题，不用找代理商、不用重登。
3. **量化** — 重启服务后逐个验：Jusa 先确认（主页身份=眼部主页）；随后 Fowler、Emerson、Jioklm、Simon 也确认；Cora 单独重测仍失败，日志是浏览器标签页导航 15 秒超时。
4. **自动化设计** — 换测法：拉起浏览器后多等 45 秒（让存着的旧标签页恢复完）再打开 facebook.com，一次就通，主页身份=身体塑形主页；以后验 Cora 就按 45 秒这个等法来。
5. **边界** — 6 个号全部确认后才可进轮换；Cora 的失败是启动等待不足，不是号坏了。猎手任务正文的轮换更新这次先没改，须另行核对任务原文后再动手——轮换概念已定、任务文本更新仍待办，不要把两者混为已完成。
6. **验收** — 6 个环境全部确认：Fowler、Emerson、Jioklm、Jusa、Simon、Cora 都是已登录、主页身份正确。下午 15:45 养号轮仍只成 3 个（Jioklm、Jusa、Simon），Cora 仍因等的时间不够而超时、Fowler/Emerson 共用 20004 线瞬时抖动，但复测线通，结论仍是"没有一个真出问题"，与登录态结论一致。

教学价值：核验步骤本身要有超时参数；把"等的时间"写进核验方法，下一次同样环境就不再被误判为故障。

附带实例（同一窗口的工具决策）：Codex 已装 0.164.0-alpha.9 但 `~/.codex` 只有空 tmp 目录、未登录；登录需用户自己的 OpenAI/ChatGPT 账号授权，主代理替登不了；当前运营工作（浏览器、文档、定时任务、CLI）没有一项非 Codex 不可，其价值只在未来纯写代码的大活上。结论是"不缺能力，先不启用"，不是"不能用"。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25**: 例15 的批准门是同一条线的下一环；缺料不可用别的料顶替仍成立。
2. **autoclip 接入 clipdraft Skill（候选，未采纳）** — transfer 的下一环是"AI 选段"，不是整条替换；实测等用户点头；FB 每日线明确排除。
3. 私信首接的事件驱动升级 — done as 例8; 2026-10-25 的新候选面：猎手任务正文的轮换更新（待核对原文后动手）。
4. 海外6组每周数据汇总/周报 — 仍是未知面，等用户提团队汇报摩擦时再问。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-10-26T19:13:27Z (24h, per study task plan). By then: autoclip 实测是否获批并跑出 JSON/耗时结果；猎手任务正文轮换更新是否完成；例10 的 3 秒触发任务正文补写是否完成；X p6 当晚是否再次出现 twitter-cli 初始化故障（2026-10-25 10:45 Beijing 已发出一次，不等于根治）；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: three new same-day worked examples (15–17) observed and preserved; the publish gate and the external-tool evaluation framework are now written as task-text conditions, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, plus 例15 的批准门与例16 的用户自带候选)， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: 例10 的任务正文补写在 2026-10-24 当天因安全检查未完成，2026-10-25 的四任务改动是否包含 3 秒触发口径未在窗口内确认；例5 串行锁的下轮验证结果仍未知；X p6 工具故障的根治方案未知；autoclip 的 CLI/MCP 细节以 README 为准，尚未在本机实测。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and candidate):
- "我觉得可以" (2026-10-25 Beijing afternoon, approving only the seven-part strategy, not v1/v2, material timing, or animation length)
- "dulaautoclip 这个 github 的自动剪辑工具我们的项目能用吗？" (2026-10-26 00:26 Beijing, user raising the candidate)
- "自动剪辑，不是自己剪辑" (2026-10-26 00:26 Beijing, user correcting the term)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/16 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- Autoclip 实测：用户点头后，跑一条带字幕素材的 produce，记录 JSON 结构与耗时，再定接不接。
- 猎手任务正文轮换更新：核对原文后动手，完成后回读核验。
- 例5 串行锁的下轮验证是否通过；例10 任务正文补写是否完成；X p6 工具故障是否根治。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate now touches the same pipeline, so ask in that context, not as a separate item.)

## Research Trajectory

- **External sources viewed**: zhouxiaoka/autoclip, GitHub repository page, https://github.com/zhouxiaoka/autoclip — opened and read 2026-10-26 in this study; added MIT licence, 9,716 stars at read time, CLI/MCP availability, `produce --srt --json` usage, local CLI needing only Python + FFmpeg without Redis, brand outro default-on and closable, and the 1h43m/10-clip/¥0.09 cost example, all consistent with the main agent's 2026-10-26 00:31 Beijing assessment.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-20/goal.md`, `.../2026-10-21/goal.md`, `.../2026-10-22/goal.md`, `.../2026-10-23/goal.md`, `.../2026-10-24/goal.md`, `.../2026-10-25/goal.md` (2026-10-25 and 2026-10-24 read in full, earlier ones carried via the 10-25 note's review; carried forward the goal snapshot, standing constraints, worked examples 1–14, the teach-plan structure, and the 10-25 note's open questions on 例5, 例10, the checklist re-ask, and formalizing cards).
- **Repetition search**: keyword variants {autoclip, dulaautoclip, 自动剪辑, clipdraft} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` (filenames included; briefs dir lists exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡， `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单）. All four variants: **zero hits in any prior note or brief filename** — the autoclip/Dula candidate is new to the goal's written record. A second grep {用户已批准, 发布门, 先审, 轮换} hits only the 10-25 note's 先审后排 rule and the 10-24 note's 轮换 concept, not the 2026-10-25 task-text gate or the Cora 45-second verification method. Every one of today's instances was raised by the user or narrated to him live in main chat, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-24T19:09:07Z → 2026-10-25T19:13:37Z. The goal-relevant turns: seven-part strategy approval and its limits, publish-task gate hardening and the three skipped evening rounds, six-environment login verification and the deferred hunter-text update, the autoclip/Dula evaluation thread (user questions at 2026-10-26 00:26/00:28/00:32/00:39 Beijing, assistant evaluations at 00:27/00:31/00:36/00:46 Beijing), the Codex question, and X p6 sent plus the renewed 344 limit.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md and memory search on autoclip / 重复工作自动化 / dulaautoclip confirming the Dula/autoclip resolution, the superseded 10-19 draft, and the pending autoclip live test; the 2026-10-25 STUDYING.md projection (mode teach, novice, next review 2026-10-25T19:12:23Z) as the selection signal.
- **Searches skipped or unavailable**: web search beyond the autoclip repository page skipped (the remaining topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract. Dula Clip AI has no GitHub/官网 URL to open — the main agent's finding (GitHub search 0 results, distribution only via a file-pack route) is recorded as an unavailable-source finding, not as a verified link.
