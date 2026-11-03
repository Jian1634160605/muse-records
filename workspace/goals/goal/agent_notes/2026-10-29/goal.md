# Study Notes - 2026-10-29 - 重复工作自动化
<!-- studying-run-start: 2026-10-28T20:37:28Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now seven days since the 2026-10-22 delivery.
- Prior notes read in full: `2026-10-28/goal.md` and `2026-10-27/goal.md`; earlier notes carried via the 10-28 note's review (`2026-10-20` through `2026-10-26`).
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated.

## Already Covered in Main Chat

- 2026-10-28 Beijing morning: user corrected the single-account target — 200 qualified leads for one account, execution from 2026-10-28 itself, not from 2026-11-01 and not a preparation period.
- 2026-10-28 Beijing morning: user changed the material-intake rule — Muse no longer tells him what material is needed or searches the library case by case; all material is supplied directly by the user, with a separate, narrow exception for generic surgery reference footage.
- 2026-10-28 Beijing daytime: user confirmed case 1's stage dates (v58 = Day 7, v76 = Day 30) and chose version A (result-first) from the three v6 versions; which account it posts to and whether the current no-fabrication cover is used were left undecided.
- 2026-10-28 Beijing 17:07: user ordered X promo, interaction, and daily-report traffic to move to the side chat 「X 运营报告」, with main chat reserved for FB content communication and urgent matters via side chat plus WeChat.
- 2026-10-28 Beijing daytime through 2026-10-29 Beijing early morning: X promo and interaction rounds were narrated live round by round (p56 onward, commented count rising past 250), including repeated short-interval skip notices and repeated schedule-overlap notices, all asking the user to decide the interval rule.
- 2026-10-28 Beijing daytime: FB hunter and DM-watch rounds were narrated live — Mellissa Gerow Russell's B-19 closing follow-up sent and CLI-verified, Anne Riches and Sarah Jane re-asks sent, no new client replies, 0 new qualified leads.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Six new worked automation instances (例30–35), all from 2026-10-28 lived operations and the 2026-10-29 early-morning X rounds. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: 2026-10-28 is the day the automation pattern's weak point moved from "no stop condition" to "a stop condition exists but its rule is disputed." The X promo line finally got a working pre-check (例30) and ran all day, while the X interaction line kept executing two different rules in the same day — platform-signal-only in its task text, short-interval skip in practice — and asked the user to decide, repeatedly, without a decision landing (例31). A disputed rule that keeps running is worse than a missing rule: it produces inconsistent execution and a log full of overlap warnings, and each round re-asks the same question instead of banking the answer.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, seventh day.
2. Standing constraints — **present, expanded by three in this window**:
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
   o. **NEW**: report routing is by topic, not by channel default — X promo, interaction, and daily reports go to the side chat 「X 运营报告」; main chat is FB content only; urgent matters go side chat plus WeChat (2026-10-28 17:07 Beijing; see 例31, routing note).
   p. **NEW**: material intake is user-supplied by default — Muse no longer specifies what material is needed or hunts the library case by case; the only exception in this window is a separately ordered generic surgery reference download, split by doctor, never mixed, and never passing another doctor's face or voice off as Qin Hao's (2026-10-28 09:47 Beijing).
   q. **NEW**: a target change takes effect on the corrected date, not the planned date — the single-account 200 target runs from 2026-10-28 itself, after the user corrected the "preparation period until 2026-11-01" reading the same morning (2026-10-28 11:14 Beijing; see 例34).
3. Low-risk pilots demonstrated — **now thirty-five worked examples** (例1–35 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–29 carried from the 10-28 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24), 发布任务的"用户已批准"硬门槛 (10-25), autoclip / Dula Clip AI 的接入评估 (10-26 00:26–00:46 Beijing, candidate, not adopted), 六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法 (10-25), 内容为主 70/30 + 每号每天 1 条 + 成品直发门 (10-26 afternoon), 明天 18 条秦浩成品的排期、计数与来源澄清 (10-26 evening), 已发视频的水印审计与"只隐藏、不删除" (10-26 evening), 18:45 失败后的恢复路径选择 A 与 19:45 v2 成功 (10-26 evening), autoclip 实测闭环 (10-26 17:18 Beijing), X p20 的无限重试与 226 新限 (10-26 afternoon to 10-27 early morning), 修好的 X CLI 线成为默认路线 + 280 字精简规则 (10-27 18:04 Beijing), 被截断的报错掩盖了真因 186 (10-27 evening), FB 19:45 一次性任务绕开旧格式轮次 + 代理断线的显式留仓 (10-27 evening), 秦浩素材分类法 + 只下确认项的下载口径 (10-27 afternoon–evening), 内容池算术 + 每周补料节奏 (10-27 afternoon), X p56 的熔断落地 (10-28 00:03–02:53 Beijing).

**例30：X 推广线的发前加权复核 + 逐轮补草稿（2026-10-28 Beijing 05:23 至 2026-10-29 Beijing 03:09）**
1. **盘点** — 凌晨的熔断（例29）之后，队列首条 p56 在 05:23 Beijing 精简后发出；此后推广线全天按 10 分钟一轮运行，到 2026-10-29 03:09 Beijing 已发到 p185。
2. **拆解** — 例24–25 的教训被写成了发前动作，不是事后诊断：每条发帖前核时间线最新帖、确认用户当日无手动新帖、无重复，再按 URL 权重规则验算（chuhai.wiki 计 23 字、CJK 计 2 字），加权未超 280 才走修好的 CLI 线一次发出；发后时间线核实最新帖即本条、推文数与实发一致。
3. **量化** — 05:23 的 p56 精简版发出后，队列不再卡在首条；全天补草稿成例行动作（p102–p103 起，每轮发后补 2 条后备，如 p106–p121），到 02:23 Beijing 的受阻轮次时队列记为 posted 181、pending 172；02:43 Beijing 的 p182 随后发出，03:09 Beijing 的 p185 发出。pending 数没有归零，因为补草稿的速度与消耗速度相当 — 队列健康看的是"首条是否在动"，不是 pending 总数。
4. **自动化设计** — 两个可复用点：一是超限不发、只精简，原文留 original_text 备查；二是 02:23 Beijing 的 fail-closed 受阻轮次（工具输出后收到安全提示即停住，未运行发帖脚本、未做时间线核实）也被记账为"未完成、待下一轮"，而不是事后补写成已发 — 未核实就不认定无重复。
5. **边界** — 仍有超限项在队列里待精简（p67 加权约 289–292，全天多次提醒"到 p67 前须先精简"），说明发前复核是逐条生效的，不是队列级的一次性清理；到 p67 那轮若仍未精简，正确动作仍是停住精简，不是绕过。
6. **验收** — 已验收：p56 的卡点解除后，推广线从停滞恢复为连续发帖，全天无 226/344 平台信号；未验收：p67 的精简仍待那轮到来时执行。

教学价值：熔断（例29）解决的是"失败时停下"，发前复核解决的是"失败前拦下" — 两者合起来才是一条能自己跑的线；只写熔断不写复核，下一条超限草稿还会再撞一次 186。

**例31：X 互动线的规则冲突 — 短间隔跳过 vs 平台信号-only，全天未决（2026-10-28 Beijing 全天）**
1. **盘点** — 互动轮次全天按约 1 分钟名义节奏触发，实发评论数从早上的约 89 条一路记到 03:03 Beijing 的 254 条；但大量轮次以"距上次实际互动仅 2–4 分钟，怕叠加撞 226"为由跳过，不点赞、不评论。
2. **拆解** — 跳过轮次每次都先核查了 engage-state.json：restricted_date 仍为 2026-10-27，已过期，当日未受限；Claude 防封、eSIM 保号、指纹浏览器等搜索组返回 ok:true，无 226/344 信号。也就是说，跳过的依据不是平台信号，而是自设的短间隔防叠加规则 — 与任务正文"唯一停手标准是平台信号"直接冲突，而 2026-10-23 用户定的正是后者。
3. **量化** — 冲突在同一天被反复上报：22:29、22:38、23:36、23:41 等多轮的记账里都写着"请定一下：短间隔跳过要不要保留，还是严格按平台信号-only 执行"；22:38、23:36、23:39 等时间槽还出现了同一时间槽的重叠日志（另一轮次已写入的跳过条目先于本轮出现），说明定时疑似重叠触发 — 但重叠没有造成重复互动，因为去重台账 commented.json 按 tweet_id 拦住了重复评论。
4. **自动化设计** — 可复用的反面教材有三条：一是规则冲突不能由执行轮次自行调和 — 有的轮次按正文执行（短间隔也发，如 05:15、06:23 的轮次），有的轮次按自设间隔跳过，同一任务在同一天两种行为；二是未决问题不能只靠"日报汇总"消化 — 全天多轮把同一问题推给 21:45 日报，问题本身没有在白天任何一轮被关闭；三是重叠触发需要显式去重证据 — 本窗口靠 commented.json 的 tweet_id 去重挡住了重复，但调度重叠本身（为什么同一槽出现两条日志）仍待核查，没有结论。
5. **边界** — 本 note 不擅自裁决：短间隔规则是保留还是废除、调度重叠要不要查，都须用户定；执行轮次在未决期间的"跳过并记账"至少保证了不重复、不撞限，是 fail-closed 的正确姿态，不是偷懒。
6. **验收** — 未验收：规则冲突与调度重叠两项在窗口结束时仍未决；路由变化（见约束 o）意味着这类问题此后应出现在 X 旁聊的日报里，而不是主聊 — 但路由变了不等于问题关了。

教学价值：自动化系统里最贵的不是写规则，而是关掉旧规则 — 一条被用户亲口废除过的自设数字（2026-10-23）如果还在某个轮次的"既定做法"里活着，它就会每天复活一次，直到有人把它从执行条件里删掉。

**例32：FB 内容线的"已选版、未定号" — 内容批准 ≠ 发布批准（2026-10-28 Beijing daytime）**
1. **盘点** — 案例 1 的三版 v6 已按 Day 7 / Day 30 重渲并归档：A 结果先行版 11.9 秒、B 恢复进程版 11.6 秒、C 对比冲击版 10.8 秒，封面统一 1080×1920 竖屏、主图术后最终结果、左下角小图术前、白色粗体英文文案，无真实数据不编年龄、国家、天数。
2. **拆解** — 用户 17:41 Beijing 选了 A 版，但"发哪个号、封面是否用当前无编造版"未定；17:45 与 19:54 两轮随即跳过。内容本身已批准，发布目的地与封面仍是两个独立的批准项 — 例18 的"成品直发门"在这里不适用，因为这三版是 Muse 剪辑的，不是用户发来的成品。
3. **量化** — 同一天 FB 的另一条线是反向证据：IG 队列目录 `~/workspace/ig-ops/christycrawford85/queue/2026-10-28/` 不存在、最新队列仍为 2026-10-27，22:43 Beijing 的轮次按"缺料跳过、未发"记账，未拿别的文件顶替、未向主页发 Reel — 缺料门（例15 的"用户已批准"硬门槛的另一面）仍在生效。
4. **自动化设计** — 批准要按项拆：内容版式批准、发布账号批准、封面批准是三张不同的卡；一张卡批了不能自动解锁另外两张。案例 1 的现状正好是这条规则的活例证：A 版已选，但系统没有默认账号、没有默认封面，所以正确动作是跳过并记账，不是挑一个"看起来合理"的号发出去。
5. **边界** — 昨晚留仓的 FB 6 条（Fowler a3、Emerson 17、Jioklm 3e、Jusa 03、Jioklm 昨晚视频、Jusa 昨晚文字帖）仍取决于用户查代理的结果；本窗口内没有"已补发"的证据，不能默认已补发。
6. **验收** — 部分验收：A 版选择已落定、封面模板已落定；未验收：发布账号、封面终版、留仓 6 条的补发时机。

教学价值：先审后排的"审"不是一件事 — 把批准拆成内容、账号、封面三项，系统才能在只批了一项时正确地停住，而不是在压力下把"已选版"偷换成"已批准发布"。

**例33：一案多版 + 批量成片 + 哈希去重（2026-10-28 Beijing daytime）**
1. **盘点** — 除案例 1 外的新套 01–05 陆续到货并标记在 `~/workspace/batch-20261028/new-set-0X/` 各文件夹 README.md 里；供料到一案即剪一案，不等整批。
2. **拆解** — 一个案例不只剪一条，按爆款模板出几个不同版本供用户选（案例 1 即结果先行、恢复进程、对比冲击三版）；成片按案分类归档在 `~/workspace/batch-20261028/`，封面统一模板；手术画面规则不变（非本案患者不露脸、只取切口/器械/手部近景，本案患者可露脸；裁切失败改换素材，实在无可用素材只闪过约 1–1.5 秒，也可强模糊打码保留原构图）。
3. **量化** — 新套的到货标记本身就是台账：01 只有 1 张上下对比图、案例身份未定；02 已标记齐 6 个文件，水印处理与具体天数未定前不剪不发；03 已标记齐 6 个文件，但其 06 对比图与 01 图哈希完全一致、属同一患者不应双算，是否合并待用户确认，原文件夹未删；04 已标记齐 5 个不同文件、暂时放着不用先不剪不发，视频均为横屏 10 秒转竖屏须裁切，首条视频发两次哈希相同只计 1 个，术前视频缺以对比图左图为准；05 已到 5 个、未确认是否齐，目前未见包扎段。
4. **自动化设计** — 两条可复用规则：一是"按案归档 + 按模板出多版"把剪辑从单次手工变成可重复的批量流程；二是哈希去重是计数自动化的底线 — 03 与 01 的同一图若按文件夹数双算，内容池算术（例28）就会虚增，合并决定必须由用户确认、文件夹在确认前保留。
5. **边界** — 02 的水印、04 的 HOLD 状态、05 的包扎段缺失都是"标记了就不剪"的门；标记齐全不等于可发，天数、水印、身份三项未定前，齐全的文件夹也只是库存，不是可发内容。
6. **验收** — 未验收：03–01 是否合并、02 的水印与天数、04 的启用、05 的齐全性均待用户确认；案例 1 之外其余 13 案原片本地仍无已核实落盘，需用户逐案供料。

教学价值：批量化的第一步不是剪得快，而是算得准 — 哈希去重、按案归档、未定项标记，这三样是"批量"这个词成立的前提；没有它们，批量只是把错误复制多份。

**例34：单号 200 目标 — 目标变了，度量还没跟上（2026-10-28 Beijing 11:08–11:14）**
1. **盘点** — 用户先定单号下个月 200 个合格客资（约每天 7 个，合格标准不变：海外 + 真实意向 + 带区号 WhatsApp + 国家），取代矩阵合计 100–150 的旧目标；随后纠正：执行从 2026-10-28 当天就开始，不等 2026-11-01，此前把 2026-10-28 至 31 日写成准备期是错的。
2. **拆解** — 目标变化本身是清晰的（单号、200、从今天算），但度量变化没有同步落定：英雄号是不是 Victoria、爬坡节奏（从每天几个爬到 7 个）、新号是否替代、医生每周视频面诊名额数，窗口结束时仍未获批复。
3. **量化** — 当日实数与目标的差距就是度量缺口的证据：FB 猎手轮次（round 298–306）与 DM 盯守轮次全天 0 新回复、0 新合格客资；合格客资仍是 0，多个私信线程仍无新回复（Anne、Sarah、Judi 等的再询问已发，仍在等回复）。
4. **自动化设计** — 目标自动化的一条规则：目标变了，次日复盘的口径必须当天改 — 否则复盘还会按旧矩阵合计报数，200 的单号进度永远算不出来。本窗口的复盘仍在按轮次报"评论几、私信几、客资 0"，单号累计进度表尚未出现，这是下一轮要补的台账，不是本窗口已有的成果。
5. **边界** — 不默认英雄号、不默认爬坡曲线、不默认面诊名额；用户发火后定的"只报重点和结果"口径（2026-10-28 11:17–11:18 Beijing）同样适用于 200 目标的汇报：报实际数，不报"准备中"当进度。
6. **验收** — 未验收：目标已生效（从当天算），度量（英雄号、爬坡、名额、单号累计表）未落定。

教学价值：目标自动化最容易漏的一环是度量迁移 — 目标从"矩阵合计"换成"单号"时，台账、复盘口径、汇报模板必须同一天换，否则新目标会被旧度量悄悄稀释成"还在准备"。

**例35：私信跟进梯队的服务器端核验（2026-10-28 Beijing daytime 至 2026-10-29 Beijing 00:38）**
1. **盘点** — FB 私信盯守轮次覆盖 13 个进行中线程，最新均为我方消息；跟进梯队按时间触发：Mellissa Gerow Russell 的 B-19 收尾、Anne Riches 的真人式再询问、Sarah Jane 的自然再询问。
2. **拆解** — 发送判定仍用例6 的服务器端标准：浏览器气泡不算，须经 CLI 查到线程存在且 snippet 为我方消息才算送达；Mellissa 的 B-19 即按此核验（线程 `cid.g.1380794324135672`，3 条拆分，snippet 对应第 3 条），Anne、Sarah 的再询问同样经服务器端核验。
3. **量化** — 本窗口唯一行动就是 Mellissa 的 B-19；其余 13 线程无新回复，Linnie Watkins / Jenny Porter 的 B-19 时点未到，Judi / Anne / Sarah 等真人式再询问需再隔 2–3 天；猎手侧同日新增收集表 #108–#116（含 Neisha Meredith-Ponting 的韩国群新帖短评论、Aimee、Jen、Wendy、Francesca、Jesse、Teresa、Linnea 等），评论数在涨，私信转化数仍是 0。
4. **自动化设计** — 跟进梯队本身已是自动化（时间到 → 发 → 服务器端核验 → 记账），但它只保证"不漏发、不重发、不谎报送达"，不保证"客户回话" — 转化仍卡在缺一次被接住的对话和秦浩真人素材的排期上，这是梯队解决不了、也不应假装解决的问题。
5. **边界** — 明确拒绝 / 拉黑立即停；未核验真人 + 国家的收集表项不冷发；群 403 受限的项不硬发。
6. **验收** — 已验收：梯队按时执行、送达均经服务器端核验；未验收：转化（0 合格客资）与素材排期（例32）仍是瓶颈。

教学价值：跟进自动化要分清两层验收 — 执行层（按时发、核验到、记账清）与结果层（客户回、留号、成客资）；执行层全绿、结果层为零时，正确的结论是"漏斗上游（内容与素材）需要改"，不是"跟进发得不够多"。

附带实例（同一窗口的音乐池隔离提议，未批准）：案例 1 的旧音乐池（2026-10-21 至 25 的备料）被发现混入了带人声的原曲翻录，v6 三版改用已核实干净纯音乐作基线交付；提议中的新规则是：备料步骤 4 改为隔离旧池、新增 3–4 首干净曲目轮换，旧池在逐首听过之前不再用 — 该提议在窗口结束时仍待用户批准，本 note 只记为提议，不记为已定规则。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, seventh day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.
Step 3 (from 例27, still open): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.
Step 4 (NEW, from 例31): pick ONE disputed rule in current operations (short-interval skip is the live one) and write its two candidate wordings side by side — platform-signal-only vs short-interval skip — so the user can close it with one choice instead of re-answering it every round.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28**: 例32 的"已选版、未定号"是同一条线的下一环；旧格式轮次仍未同步修订，任务正文与今日料单的对齐仍是缺口。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发；单号 200 目标下，面诊名额数本身也待用户定，见例34）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — 例34 的单号 200 目标可能改变测定的意义：测定原是"单号安全量"，现在单号本身成了 200 目标的载体；测定口径（内容量 vs 私信量）与 200 目标的度量（英雄号、爬坡、单号累计表）须在下一轮合并说明，不能各说各话。
6. **秦浩素材库的分类与补料闭环** — 例27 的分类法 + 例28 的每周补料节奏 + 例33 的一案多版与哈希去重是同一条线：用户按分类法建文件夹、直接供料，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数换掉平均估算；通用空镜库单独建，与案例料分开标；新套 03–01 的合并决定是这条线的下一个待确认项。
7. **X 互动规则冲突的关闭（NEW）** — 例31 的短间隔跳过 vs 平台信号-only 必须由用户一句话关闭，并把结论写进任务正文、从执行条件里删掉被废的一条；否则下一轮仍会重复上报同一问题。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-10-29T20:37:28Z (24h, per study task plan). By then: X 互动短间隔规则与调度重叠是否由用户关闭；X p67 的精简是否在到轮时执行；FB 留仓 6 条是否在用户查完代理后补发；案例 1 A 版的发布账号与封面终版是否落定；新套 03–01 是否合并、02 的水印与天数、04 的启用、05 的齐全性是否确认；单号 200 的英雄号、爬坡、面诊名额、单号累计表是否落定；音乐池隔离新规则是否获批；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: six new same-day worked examples (30–35) observed and preserved; the pre-post weighted check, the disputed-rule cost, the split-approval gate, the multi-template batch with hash dedup, the target-to-metric migration gap, and the server-verified follow-up ladder are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例31 尚未由用户定数，例32 的 A 版选择，例34 的单号 200 与当日生效纠正）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: X 短间隔规则与调度重叠未决；X p67 精简未执行；FB 留仓 6 条的补发时间取决于用户查代理的结果，未定；案例 1 A 版的发布账号与封面未定；新套 03–01 合并、02 水印与天数、04 启用、05 齐全性未定；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；音乐池隔离规则未获批；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "修补好了就一直用修好的线，OK" (2026-10-27 18:04 Beijing, repaired-line default; carried from the 10-28 note)
- "我先查代理，你等我消息" (2026-10-27 21:02 Beijing, proxy hold; carried from the 10-28 note)
- "你确认你自己要的那几个就行，不要搞特别多" (2026-10-27 18:22 Beijing, narrow-download rule; carried from the 10-28 note)
- Short-interval skip notices in the 2026-10-28 window are paraphrased, not quoted, because each round's wording varies; the repeated ask is consistently "短间隔跳过要不要保留，还是严格按平台信号-only 执行" in substance.

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27/30/32/34 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计；单号 200 目标的度量是否与测定口径合并。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-28/goal.md` and `2026-10-27/goal.md` read in full; `2026-10-20/goal.md` also read in full; earlier notes (`2026-10-21` through `2026-10-26`) carried via the 10-28 note's review; carried forward the goal snapshot, standing constraints, worked examples 1–29, the teach-plan structure, and the 10-28 note's open questions on 例5, 例10, the checklist re-ask, formalizing cards, the FB 6-item hold, the X p56 formal pause, the 15-case arrival, and the single-account measurement.
- **Repetition search**: keyword variants {加权, 精简, 短间隔, 多模板, A结果先行, 200个, 音乐池, 案例1} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` (filenames included; briefs dir lists exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: 短间隔 / 多模板 / A结果先行 / 200个: **zero hits** in any prior note or brief — new to the written record. 加权 / 精简: hits only inside the 10-28 note (例24–25, diagnosis and trim rule), not as today's full-day pre-check routine. 音乐池: hits only the 10-27 note's pool mention, not today's isolation proposal. 案例1: zero hits under that exact term in prior notes (earlier notes use 案例1-adjacent case wording, not this batch-20261028 pipeline). Every one of today's instances was set by the user or narrated to him live in main or side chat in the 2026-10-28 window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-27T19:09:09Z → 2026-10-28T20:49:01Z, plus the run's chunked conversation handoff covering 2026-10-28 Beijing daytime through 2026-10-29 Beijing early morning. The goal-relevant turns: the single-account 200 target and its same-day correction, the user-supplied material-intake change, the case 1 stage confirmation and A-version choice with account/cover undecided, the X-reports-to-side-chat routing order, the all-day X promo recovery (p56–p185) and interaction rounds with repeated short-interval skip and schedule-overlap notices, the FB DM-watch and hunter rounds (Mellissa B-19, Anne/Sarah re-asks, prospects #108–#116, 0 new leads), the new-set 01–05 arrival markings, and the music-pool isolation proposal.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first 70/30, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, 5-voiceover arrival, single-account 200 from 2026-10-28, X reports to side chat, main chat FB only) as background only — every dated claim in this note is sourced to the conversation window, the run handoff, or a prior note above, not to memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract. No credentials, cookie values, or proxy secrets were reproduced in this note; only ports, file names, and counts are referenced.
