# Study Notes - 2026-11-01 - 重复工作自动化
<!-- studying-run-start: 2026-11-01T00:57:38Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now ten days since the 2026-10-22 delivery.
- Prior notes read in full: `2026-10-31/goal.md` and `2026-10-30/goal.md`; earlier notes carried via the 10-31 note's review (`2026-10-20` through `2026-10-29`).
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated. This run started 2026-11-01T00:57:38Z, i.e. 2026-11-01 Beijing 08:57.

## Already Covered in Main Chat

- 2026-10-31 Beijing 12:10: user approved all four voiceover cuts with "4条全过，今晚手动发" — the cut-4 order from 2026-10-31 Beijing 07:33 was not itself the approval; this message was.
- 2026-10-31 Beijing daytime: the four approved cuts were published and verified, one per account — Victoria 104058, Fowler 104331, Jioklm 104506, Jusa 104927 — with Emerson empty, as confirmed on 2026-10-30.
- 2026-10-31 Beijing 13:06: user asked "今天作品发完了吗" and the assistant confirmed all four were out.
- 2026-10-31 Beijing 14:37: user said "你帮我发布 / 快去"; the assistant replied nothing else was in hand — the four approved cuts were already out and backup 105202 was still uncut and unreviewed — and the user accepted that.
- 2026-10-31 Beijing 14:38–14:57: user shared a four-cell content framework (daily-life implant 20%, pre-op anxiety 20%, careful-choice + comparison 20%, recovery serial 40%) and two Xiaohongshu pitfall-complaint examples, then asked whether FB and IG could run素人号 and whether to make one or several.
- 2026-10-31 Beijing 14:43–14:57: the assistant answered that a real-patient diary account is workable and a fake-persona account is not, recommended one FB pilot rather than several at once, and was asked to draft a plan; the user then rejected PDF/PPT form ("直接发文字给我就行了，不用给我去做PDF，不用做PPT") and redefined the calculation to all accounts restarted from zero.
- 2026-11-01 Beijing 07:36 (2026-10-31T23:36Z): the assistant told the user the morning接档 reminder was already set for about 2026-11-01 Beijing 09:05 and would not disturb him early in the morning.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Six new worked automation instances (例46–51), all from 2026-10-31 lived operations and the 2026-11-01 early-morning window. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: 2026-10-31 is the day the automation question became "which approval, which count, and which decision is still owed." The four evening posts look like a routine publish round, but their automation content is in the approval boundary (a cut order is not a publish approval; a single "全过" message is), in the counting boundary (manually published posts must not be double-counted in the hunter/DM daily table), and in the decision boundary (a serial/素人 plan that is still unapproved must not be written as started, and a morning decision must not be forced at midnight — it gets a 09:05 slot instead). The X line sharpens the same point from the other side: a failure that is correctly handled every single round can still be a system failure when the rounds never stop and the failure report itself cannot be delivered.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, tenth day.
2. Standing constraints — **present, expanded by three in this window** (items a–x carried from the 10-31 note):
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
   y. **NEW**: a cut order is not a publish approval — the 2026-10-31 Beijing 07:33 cut-4 proposal was explicitly not approval, and only the user's 2026-10-31 Beijing 12:10 "4条全过，今晚手动发" converted the four cuts into publishable items; per-clip account assignment was assistant-assigned, not user-assigned, and must be recorded as such (see 例46).
   z. **NEW**: a daily operations table must not double-count manually published posts — the 2026-10-31 Beijing 13:35 hunter/DM table (Victoria 发帖1、评论13、私信3、回复0、客资0; other four accounts paused) correctly excluded the three manually published Fowler/Jioklm/Jusa cuts, so the table stays a hunter/DM-line table, not a whole-day publish count (see 例47).
   aa. **NEW**: an unapproved plan stays unapproved across form changes — rejecting PDF/PPT and asking for text plus an all-new-accounts recalculation changes the deliverable, not the decision status; the素人/serial pilot (patient candidate, written authorization, follow-up material) remains undecided, and IG remains not started (see 例49).
3. Low-risk pilots demonstrated — **now fifty-one worked examples** (例1–51 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–45 carried from the 10-31 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24), 发布任务的"用户已批准"硬门槛 (10-25), autoclip / Dula Clip AI 的接入评估 (10-26 00:26–00:46 Beijing, candidate, not adopted), 六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法 (10-25), 内容为主 70/30 + 每号每天 1 条 + 成品直发门 (10-26 afternoon), 明天 18 条秦浩成品的排期、计数与来源澄清 (10-26 evening), 已发视频的水印审计与"只隐藏、不删除" (10-26 evening), 18:45 失败后的恢复路径选择 A 与 19:45 v2 成功 (10-26 evening), autoclip 实测闭环 (10-26 17:18 Beijing), X p20 的无限重试与 226 新限 (10-26 afternoon to 10-27 early morning), 修好的 X CLI 线成为默认路线 + 280 字精简规则 (10-27 18:04 Beijing), 被截断的报错掩盖了真因 186 (10-27 evening), FB 19:45 一次性任务绕开旧格式轮次 + 代理断线的显式留仓 (10-27 evening), 秦浩素材分类法 + 只下确认项的下载口径 (10-27 afternoon–evening), 内容池算术 + 每周补料节奏 (10-27 afternoon), X p56 的熔断落地 (10-28 00:03–02:53 Beijing), X 推广线的发前加权复核 + 逐轮补草稿 (10-28 Beijing 05:23 to 10-29 Beijing 03:09), X 互动线的规则冲突 — 短间隔跳过 vs 平台信号-only，全天未决 (10-28 Beijing), FB 内容线的"已选版、未定号" — 内容批准 ≠ 发布批准 (10-28 Beijing daytime), 一案多版 + 批量成片 + 哈希去重 (10-28 Beijing daytime), 单号 200 目标 — 目标变了，度量还没跟上 (10-28 Beijing 11:08–11:14), 私信跟进梯队的服务器端核验 (10-28 Beijing daytime to 10-29 Beijing 00:38), 五号共用主号线 + 主页与个人主页双发的第一轮 (10-29 Beijing 16:24–17:42), Fowler 主页的四次失败、一次未核验关闭、一次 cookie 备份恢复后成功 (10-29 Beijing 17:42–18:12), 自评欠账 7 条变 10 条的可能 + 11:00 定时重试 (10-29 Beijing 19:35 to 10-30 Beijing 07:31), X 队列与去重台账的同日两次截断 + 备份恢复 (10-29 Beijing 18:01–18:02), 去重台账读截断导致的重复评论 + 删除不可靠 (10-29 Beijing), 私信哨兵断线 + 15 分钟兜底的双层设计 (10-29 Beijing 17:48–18:12), 五号轮换写好又在当日退回单线 (10-30 Beijing 10:35 → 16:52), 五条补发冲刺与 Jioklm 身份切换正解 (10-30 Beijing daytime), X p634 的全天同故障重试 + 旁聊转交死循环 (10-30 Beijing 10:43起，贯穿 10-31 Beijing 08:13), 2026-10-31 Beijing 07:33 的接档提问 — 库存清零后"直接做"与"直接发"仍是两回事 (undecided at the 10-31 note's close).

**例46：四条口播"全过"才是发布批准 — 剪四条的指令不是批准，分配也不是用户定的（2026-10-31 Beijing 07:33 → 12:10 → evening）**
1. **盘点** — 晨间提问（例45）先报库存事实：昨天五条已全部发齐，能直接发的成品库存清零；现成料是五条秦浩口播原片；方案是剪四条送用户过目（104058 松弛程度、104331 小拉皮恢复时间、104506 35 岁后松弛自测、104927 小拉皮全流程），105202 留作备用；剪辑口径不变：只留医生讲话主体，剪掉开头结尾非讲话段和摄影师出境段，原声不另嵌音乐，英文字幕。
2. **拆解** — 关键区分在本窗口内由助理自己先讲清、再由用户动作坐实：2026-10-31 Beijing 11:38 的提问里明确写了"14:39 切四条的指令不等于批准，每条发哪个号也还没定，Emerson 空着"；用户 12:10 的"4条全过，今晚手动发"才是批准。发布时按号分配是助理定的：Victoria 104058、Fowler 104331、Jioklm 104506、Jusa 104927，Emerson 空着 — 这与 10-30 确认的"Emerson 不能发口播"一致，但分配本身不是用户逐条指定的。
3. **量化** — 四条全部发布并核验：作者、文案、自评三重核验过的链接为 Victoria https://www.facebook.com/reel/2509916446084765/ 、Fowler https://www.facebook.com/reel/1444880133846056/ 、Jioklm https://www.facebook.com/reel/1355372076510583/ 、Jusa https://www.facebook.com/reel/1472612874833671/ 。用户 13:06 问"今天作品发完了吗"，助理确认四条已出；用户 14:37 再说"你帮我发布 / 快去"时，助理答手里已无可发项，四条已出、备用 105202 未剪未过目，用户接受 — 没有把备用条当作可直发的库存。
4. **自动化设计** — 可复用规则有二：一是料单上必须分开三栏 — 剪辑指令 / 过目批准 / 逐条分配，缺一栏就不进发布队列（例32 的内容批准 ≠ 发布批准，在这里细化为"切" ≠ "过" ≠ "分号"）；二是"手动发"这个词在本轮里是用户批准的发布方式，不是绕过核验 — 四条仍走了作者、文案、自评的核验，核验栏不能因"手动"而省略。
5. **边界** — 10-30 的五条冲刺与 10-31 的四条不是同一模式：10-30 是单线暂停下的补发冲刺，10-31 是用户逐条批准的当晚四号发布；两者都不能读成轮换、截流、养号已恢复。11-01 接档仍未定（见例51）。
6. **验收** — 已验收：四条链接；未验收：备用 105202 的剪辑与过目、四条的自评是否逐条补齐（例38 的欠账逻辑仍适用）。

教学价值：自动化料单里最容易偷换的一步，是把"开始做"当成"已经批准发" — 剪、过、分号是三道不同的门，任何一道门的通过都不能替另外两道门签字。

**例47：猎手日表不重复计手动发帖 — 一张表只算一条线（2026-10-31 Beijing 13:35）**
1. **盘点** — 当日猎手/私信线日表：Victoria 发帖1、评论13、私信3、回复0、客资0；Emerson、Fowler、Jioklm、Jusa 猎手/私信线暂停中。
2. **拆解** — 表里 Victoria 的"发帖1"与当晚手动发布的四条是两笔不同的账：日表统计的是猎手/私信线当天的动作，手动发布的 Fowler、Jioklm、Jusa 三条没有被重复计入该表。10-30 的教训（例36：总数掩盖某号 0 发）在这里反向成立 — 如果把手动发帖也塞进猎手表，Victoria 的单线表会被四条手动帖撑大，读表的人会误以为猎手线已经恢复四号。
3. **量化** — 猎手当日采集：收藏 155–161 号陆续增长（土耳其群组、休斯顿拉皮医生、阿尔伯克基眼睑、俄亥俄、土耳其内窥镜深层拉皮、眼袋类型等帖），每条 Victoria 评论均核验落地；全天 DM 0 新回复、客资 0、Victoria 无受限。
4. **自动化设计** — 可复用规则：多条业务线共用"发帖"这个词时，日表必须在表头写清它算哪条线；手动发布、猎手评论、私信跟进是三条线，三条线的计数表不能互相借数。
5. **边界** — 本例不改变任何一号的暂停状态；四号的手动发帖是发布动作，不是猎手/私信线恢复。
6. **验收** — 已验收：日表口径在当轮交代清楚；未验收：四条手动帖的自评补齐情况。

教学价值：计数自动化最常见的失真，不是少计，而是把不同线的数加进同一张表 — 表头不写清口径，数字越大误导越大。

**例48：去重台账再一次读不全 — 20:41 重复评论与删不掉的教训重演（2026-10-31 Beijing 20:41）**
1. **盘点** — X 互动轮 20:41 在 EvanLeeCQ 的家宽帖（2116507154509119518）上重复评论，与 20:40 轮次的合法评论撞车；重复评论 id 为 2116510995510423881。
2. **拆解** — 原因与例40 同构：起轮时 commented.json 读取被截断，没看到尾部、漏看了上一轮记账，于是对同一帖又发一次。补救同样失败：两次 tw2.py 删除尝试分别超时 180 秒与 170 秒，重复评论仍在线于原帖线程；台账侧已订正为只保留合法的 20:40 评论 2116510410027483587，commented.json 清理后记为 890 条。
3. **量化** — 20:40 与 20:41 两轮相隔约 1 分钟 — 短间隔本身就是高危窗口；例31 的短间隔跳过 vs 平台信号-only 规则冲突至此仍未由用户关闭，而本例证明短间隔轮次叠加截断读取时，重复几乎不可避免。
4. **自动化设计** — 可复用规则已在当轮记为教训：去重判定必须 grep tweet_id 或读 commented.json 尾部，不能只依赖整文件读取；删除不是可靠补救，超时两次即停手、记账订正，不追删到底；台账干净与帖子重复仍在必须分开写，不能写成"已处理"。
5. **边界** — 本例不改变例40 的结论，只证明例40 的规则没有被写进执行条件 — 规则写在复盘里、没写进选帖手順时，同一故障会在新的一天重演。
6. **验收** — 部分验收：台账已订正；未验收：帖子里的重复评论仍在线，删除未生效。

教学价值：去重规则的验收标准不是"复盘里写过"，而是"下一轮选帖前是否真的 grep 了 tweet_id 或读了尾部" — 写进复盘的规则若不进手順，等于没写。

**例49：素人/连载方案仍未批 — 方向可借、方法不可抄、形式被否、测算被重算（2026-10-31 Beijing 14:38–14:57）**
1. **盘点** — 用户框架：日常生活植入 20%、术前焦虑 20%、谨慎选择 + 对比 20%、恢复连载 40%；论点是每个病例阶段都是内容，恢复连载拉回访，一个病例的价值可以放大。用户另发两张小红书截图（杭州隆鼻失败点名店铺、上海隆鼻歪斜维权投诉），属"踩坑投诉种草"。
2. **拆解** — 助理的区分是本例的核心自动化资产：方向可借 — 恐惧/搜索动机 + 证据链 + 评论区生长解释了帖子为什么有人看，医生主导的踩坑教育（选医生前要问什么、面诊流程信号）不需要新患者素材，适配口播；方法不可抄 — 点名同行/店铺（不贬低同行红线 + 法律/平台风险）、在医生号上伪造患者投诉（身份混淆）、复用他人面孔/收据，三条全禁。两张截图帖本身只有个位数点赞（上海帖 3 赞 / 15 评论，评论区才是价值），所以它们不是连载系统本身，只落在 20% 选择 + 对比格里的"踩坑教育"子类型，外加一条小改：自家帖结尾留一个引回复的问题。
3. **量化** — 用户追问"FB 和 IG 能做这种素人号吗，我们自己做一个这种素人 / 或者多做几个 / 素人来种草"时，助理的答案是分层的：真人日记号可行（真实患者、自愿、授权、真实时间线、身份干净；医生号背书、日记号讲人讲过程、双号收口到 WhatsApp/面诊钩子），假扮陌生患者的假素人号不可行（虚构身份 + 误导营销，封号风险与海外医疗合规风险更大，曝光后秦浩信任崩塌）；FB 比 IG 更直接（群组里已有现成的推荐/恢复需求），IG 自 2026-10-20 弃用后重启需新号、养号、分流，性价比低于先在 FB 验证；数量上不是一次做几个，而是 1 个 FB 真人日记试点、恢复连载节奏、医生号转发背书、测 2 周（播放 vs 客资），有效才扩。
4. **自动化设计** — 可复用规则有三：一是"方案被否的是形式，不是方向" — 用户 14:56 否了 PDF/PPT（"没用了，我看不懂，直接发文字给我就行了，不用给我去做PDF，不用做PPT"），助理 14:53 自称的 11 页可执行版因此不算已交付形式，文字版仍欠着；二是"测算被重定义，不等于被批准" — 用户把测算基准从现有号改为全部新号从 0 粉丝/0 播放重算，助理给出的文字测算（新号每天 1 帖、冷启动约 100 播放/帖、互动 1–3%、互动到私信 10%、私信到留号 20%；单号首月约 3000 播放、1–2 个客资，5 号约 5–10 个/月；即使成熟到 1000 播放/帖，5 号约 90 个/月，仍低于 200）只是测算假设，不是启动决定，助理同时建议不废 Victoria、老号加新号做增量；三是试点三项待拍板至今未变 — 患者人选、书面授权、随访素材，缺一项都不能开拍。
5. **边界** — 用户 14:45 的"我想想，你结合这个内容给我出一版方案"是"出方案"，不是"批准试点"；ainotes.coloros.com 的《矩阵账号 SOP 与五系列内容收割链》被合并时，助理没有照抄大号每天 3 帖（与每号每天 1 条高质量规则冲突），只保留了 1 大 + 3–4 小交叉分发、生活/工作/客户系列种草、讲解/服务系列收割的骨架。漏斗公式（客资 = 曝光 × 互动率 × 私信转化率 × 留号率 × 合格率）已给出，但助理同时承认真实分段率不可测（客资仍为 0、漏斗从未按段记账），所以试点计划只能带一张实测表，不能带编造的百分比。
6. **验收** — 未验收：文字版方案仍欠；患者人选、书面授权、随访素材三项未定；IG 未启动；试点未启动。本 note 不把其中任何一项写成已定或已启动。

教学价值：方案自动化最容易错的一步，是把"用户让出方案"读成"用户批准执行"，把"测算被重算"读成"目标被改小" — 出方案、改测算、批执行是三道不同的门，门与门之间不能互相顶替。

**例50：X p634 续入 2026-11-01 凌晨 — 单轮正确、系统仍在重复失败（2026-10-31 Beijing 10:43起，贯穿 2026-11-01 Beijing 08:13）**
1. **盘点** — 推广草稿 p634（出海账号换绑后旧登录设备二次确认，146 字，未超 280）自 2026-10-30 Beijing 10:43 起每一轮都发不出去：post_next_acct2.py 在 "Getting Twitter cookies…" 处中断，返回 rc=1，还没走到 X 发帖接口；2026-11-01 Beijing 00:03 至 08:13 的每 10 分钟一轮延续同一故障，07:03 实跑仍是同一故障，后续轮次按停手口径只做只读核验、不盲目重试。
2. **拆解** — 每轮只读核验结论稳定：tw2.py 显示 @TheEasySale1 authenticated=true、verified=true；最新自有帖始终是 2026-10-30 的 p633（2115995832076181821）；时间线前列无 p634 文本、无 2026-11-01 新帖、无用户手动新帖；无 226/344 平台限制证据；p634 始终 pending，队列待发约 100 条，草稿内容无变动、无后备草稿增补。推文数漂移（10-31 日报记 1545，11-01 凌晨轮次记 1599、1607、1609）经时间线核实均不计为成功。
3. **量化** — 互动线同期正常：commented.json 从 2026-10-31 Beijing 08:12 的约 803 条一路记到 2026-11-01 Beijing 05:53 前后的约 950 条、08:13 前后的 954 条，每轮典型 1 评论 1 点赞、自引指纹浏览器防关联帖或 eSIM 踩坑帖，无 226/344 信号，engage-state.json 的 restricted_date 仍为 2026-10-27（已过期） — 故障定位在发帖工具取 cookie 一步，不在账号受限。X 2026-10-31 日报（21:45）：粉丝 1490（较 10-30 日报 1445 增加 45），关注 1946 不变，当日推广成功 0，p634 全天 pending，互动当日 commented +158（含自引 155）、点赞约 228。
4. **自动化设计** — 例44 的三条规则至此仍未落地：重试任务没有全天累计同故障熔断（"每轮不盲重试"被每 10 分钟的调度本身架空）；失败上报仍走不可用通道（每轮旁聊转交请求仍被 "this scheduled job has no chat to message from" 拒绝，需主 agent 转交）；计数漂移仍靠每轮人工核实而非明文规则。2026-11-01 Beijing 09:10 的 x-p634-pause-decision 定时任务正是为"暂停还是再试"设的决策点（见例51），在此之前，任何一轮都不应把"又失败一次"写成新结论。
5. **边界** — 故障定性仍是工具端故障，不是平台限额；根因（取 cookie 一步为何中断）未查明；CLI 修好线（2026-10-27 定的默认发帖线）与 post_next_acct2.py 的关系仍未澄清 — 本 note 不把"换 CLI 线"写成已定方案。
6. **验收** — 未验收：p634 仍 pending；转交死循环未解；熔断是否写进重试任务未由用户定。

教学价值：一个失败若每 10 分钟被"正确处理"一次，它的正确处理本身就成了新的重复劳动 — 熔断不是事后统计，而是要写进调度条件的停表。

**例51：11-01 上午三个决策点排进定时任务 — 深夜不问、上午定点问（2026-11-01 Beijing 09:05 / 09:10 / 09:20）**
1. **盘点** — 三个未决项各自已有定时任务：fb-nov1-morning-decisions（runonce，2026-11-01 Beijing 09:05）问 11-01 接档 — 继续 Victoria 单线还是延续 10-31 当晚的全号做法；x-p634-pause-decision（runonce，2026-11-01 Beijing 09:10）问 p634 是暂停还是再试；fb-seeding-plan-text（runonce，2026-11-01 Beijing 09:20）交素人/连载方案的文字版。
2. **拆解** — 助理 2026-11-01 Beijing 07:36 先向用户交代了节奏："今天上午的接档提醒已约好，约 09:05 发你，不会在大清早打扰你" — 决策提醒本身被当作一项需要排期的动作，而不是在 08:57 的本轮里提前追问。三个决策点分开排（09:05、09:10、09:20），而不是并成一个问题，呼应例49 的"三道门分开"：接档、p634、方案文字版是三个独立决定，一个的答案不能替另外两个签字。
3. **量化** — 本轮开始时（Beijing 08:57）三个决策点均未到时，结论一律是"未决"，不能默认单线或全号中的任何一种；10-30 的五条与 10-31 的四条都是一次性当晚发布冲刺，不能读成轮换、截流、养号已恢复。
4. **自动化设计** — 可复用规则：未决事项的自动化形态是"定时提醒 + 待定清单"，不是"默认执行" — 提醒时间本身要向用户明说（几点发、不打扰的承诺），提醒到了才问，问之前不擅自补发、不擅自扩号。
5. **边界** — 本例记录的是"提醒已约好"，不是"决定已做出"；09:05、09:10、09:20 三个任务的结果均不在本轮窗口内。
6. **验收** — 未验收：三项决定全部待 09:05 之后。

教学价值：决策自动化常常不是"自动决定"，而是"自动在对的时间把问题摆到用户面前" — 摆问题的时间点本身，就是对用户节奏的尊重。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, tenth day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.
Step 3 (from 例27, still open): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.
Step 4 (from 例31, still open): pick ONE disputed rule in current operations (short-interval skip is the live one, re-proven by 例48) and write its two candidate wordings side by side — platform-signal-only vs short-interval skip — so the user can close it with one choice instead of re-answering it every round.
Step 5 (from 例36–38, still open): pick ONE owed follow-up action (self-comments are the live one: 7 owed, possibly 10 if 3 more post today) and write its count, its retry time (2026-10-30 11:00 Beijing), and its stop condition (line still stuck → stop, do not force-refresh) — so a "posted" success never again hides an unfinished follow-up.
Step 6 (from 例42–45, still open): pick ONE automation mode decision that is still open (today's接档: Victoria single-line 1 voiceover vs yesterday's five-account 4 voiceovers) and write it as one line — 模式 / 条数 / 例外号（Emerson 空着）/ 过目门 — before any cutting starts, so the day's料单 never again has to be re-cut after the mode is settled.
Step 7 (NEW, from 例46–51): pick ONE of the three 2026-11-01 morning decision slots (09:05 接档 / 09:10 p634 暂停与否 / 09:20 方案文字版) and write it as one line — 决定项 / 选项 / 默认项（无默认，须用户定）/ 到时提醒 — so an undecided item is carried as a timed reminder, not as a silent default.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28, page-plus-profile round completed 2026-10-29, rotation written and reverted same day 2026-10-30**: 例46–47 是同一条线的下一环 — 批准栏、分配栏、计数口径栏必须分开，手动发布不能混进猎手日表。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发；单号 200 目标下，面诊名额数本身也待用户定，见例34）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — 测定窗已到 2026-11-01；例34 的单号 200 目标可能改变测定的意义：测定原是"单号安全量"，现在单号本身成了 200 目标的载体；测定口径（内容量 vs 私信量）与 200 目标的度量（英雄号、爬坡、单号累计表）须在下一轮合并说明，不能各说各话。
6. **秦浩素材库的分类与补料闭环** — 例27 的分类法 + 例28 的每周补料节奏 + 例33 的一案多版与哈希去重是同一条线：用户按分类法建文件夹、直接供料，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数换掉平均估算；通用空镜库单独建，与案例料分开标；新套 03–01 的合并决定是这条线的下一个待确认项。
7. **X 互动规则冲突的关闭** — 例31 的短间隔跳过 vs 平台信号-only 必须由用户一句话关闭，并把结论写进任务正文、从执行条件里删掉被废的一条；例48 证明不关闭的代价是重复评论重演，否则下一轮仍会重复上报同一问题。
8. **欠账计数与写前备份** — 例38 的自评欠账与例39 的队列截断是同一类缺口：任何后置动作与任何队列文件都需要独立计数 / 备份 + 写后校验；下一轮要把"欠账表"和"写前备份"写进发布与发帖轮次的手顺，而不是靠事后从日志里重建。
9. **失败上报的熔断与可用通道** — 例44 与例50 的 p634 转交死循环是同一类缺口的另一面：重试任务须自带全天累计同故障熔断，失败上报须走调度任务实际能用的通道或合并为一次性汇总，否则上报本身会成为新的重复劳动。
10. **未批方案的待定清单（NEW）** — 例49 的素人/连载试点是同一类缺口的决策面：患者人选、书面授权、随访素材三项待拍板必须以待定清单形态存在，文字版方案是欠件，不是已批；下一轮须先核对 09:20 文字版是否交付，再问试点是否批准，不能把交付当批准。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-11-02T00:57:38Z (24h, per study task plan). By then: 2026-11-01 Beijing 09:05 接档是单线还是全号，用户是否答复、剪了几条、过了目没有、当晚窗口是否赶上；09:10 p634 是暂停还是再试、取 cookie 故障根因是否查明、熔断是否写进重试任务、旁聊转交通道是否换成可用方式；09:20 素人/连载文字版是否交付、试点三项（患者人选、书面授权、随访素材）是否拍板；20:41 重复评论是否仍在线；7 条（或 10 条）自评在 2026-10-30 11:00 Beijing 重试后是否补齐；X 互动短间隔规则与调度重叠是否由用户关闭；五号共用一线后有无验证或限流信号；单号 200 的英雄号、爬坡、面诊名额、单号累计表是否落定；单号安全量测定（窗至 2026-11-01）是否与 200 度量合并说明；音乐池隔离新规则是否获批；新套 03–01 是否合并、02 的水印与天数、04 的启用、05 的齐全性是否确认；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: six new same-day worked examples (46–51) observed and preserved; the cut-vs-approval-vs-assignment distinction, the single-line daily-table counting rule, the repeated truncated-read duplicate, the borrowable-direction vs non-copyable-method distinction with its still-unapproved pilot, the p634 failure loop carried into a second day, and the timed morning decision slots are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例31 尚未由用户定数，例32 的 A 版选择，例34 的单号 200 与当日生效纠正，例36 的改线与双发决定，例40 尚未由用户定数，例42 的轮换批准与当日回退决定，例44 尚未由用户定数，例46 的四条全过批准，例49 尚未由用户定数）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: 2026-11-01 接档（单线 vs 全号）未定；09:10 p634 暂停与否未定；09:20 文字版未交付；试点三项未定；20:41 重复评论仍在线；7 条自评的 2026-10-30 11:00 Beijing 重试结果不在本窗口内；p634 取 cookie 故障的根因未查明；X 短间隔规则与调度重叠未决；五号共用一线后的长期关联风险未验证；X 原 262 条草稿全文丢失后是否补回未定；Dreamofkang 与 andynotbot 的重复评论仍在线；私信哨兵状态文件写失败的根因未深究（重启自愈）；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；音乐池隔离规则未获批；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "4条全过，今晚手动发" (2026-10-31 Beijing 12:10, the four-cut publish approval)
- "今天作品发完了吗" (2026-10-31 Beijing 13:06, the user's completion check)
- "你帮我发布 / 快去" (2026-10-31 Beijing 14:37, the user's second publish push, answered as nothing left in hand)
- "没用了，我看不懂，直接发文字给我就行了，不用给我去做PDF，不用做PPT" (2026-10-31 Beijing 14:56, the PDF/PPT form rejection)
- "我发现一个问题哈，你管理的这些账号，除开那个主号其他账号你都没发过视频，我今天才知道" (2026-10-29 Beijing 16:24, the per-account zero-post discovery; carried from the 10-30 note)
- "你把其他账号的静态IP都改成和主号一样 的你试试能不能解决问题！" (2026-10-29 Beijing 16:28, shared-line order; carried from the 10-30 note)
- "修补好了就一直用修好的线，OK" (2026-10-27 18:04 Beijing, repaired-line default; carried from the 10-28 note)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27/30/32/34/36/42/46 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计；单号 200 目标的度量是否与测定口径合并。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)
- 五号共用一线是长期配置还是排障临时态：若是临时态，恢复一号一线的时点与判据是什么，须用户定；若是长期态，关联风险的接受要显式记下来，不能只留在当轮口头。
- p634 重试任务的熔断数与上报通道：全天累计同故障几次后降级为只读核验、失败汇总走哪条调度任务实际能用的通道，须用户定；在此之前，每轮仍会产生新的转交请求。
- 素人/连载试点是否批准：患者人选、书面授权、随访素材三项须先拍板；文字版方案交付不等于试点批准，下一轮须分开核对。

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-31/goal.md` and `2026-10-30/goal.md` read in full; earlier notes (`2026-10-20` through `2026-10-29`) carried via the 10-31 note's review; carried forward the goal snapshot, standing constraints a–x, worked examples 1–45, the teach-plan structure, and the 10-31 note's open questions on 例31, 例32, the checklist re-ask, formalizing cards, the FB 6-item hold, the X p67 trim, the 15-case arrival, and the single-account measurement.
- **Repetition search**: keyword variants {104058, 素人, 串联, 恢复连载, 坑位, 四条全过, 接档, 全号, 2116510995510423881} grep-searched over `workspace/goals/goal/agent_notes/` and the brief filenames in `workspace/goals/goal/briefs/` (exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: 素人 / 串联 / 恢复连载 / 坑位 / 四条全过 / 2116510995510423881: **zero hits** in any prior note or brief filename — today's instances are new to the written record. 104058: hits only in the 10-28 note (as inventory) and the 10-31 note (as the undecided cut-4 proposal) — not as a published approval. 接档 / 全号: hits only in the 10-31 note (the undecided 2026-10-31 接档 question and the still-paused mode) — not today's approval, publish, or 11-01 morning decision slots. Every one of today's instances was set by the user or narrated to him live in main chat in the 2026-10-31 to 2026-11-01 Beijing window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-31T00:18:49Z → 2026-11-01T01:05:49Z, plus the run's chunked conversation handoff covering 2026-10-31 Beijing daytime through 2026-11-01 Beijing 08:13, including the 2026-10-31 Beijing 12:10 four-cut approval, the four verified publish links, the 14:38–14:57 素人/serial discussion and PDF/PPT rejection, the 20:41 duplicate-comment incident, the 2026-11-01 Beijing 07:36 morning-reminder message, and the 09:05 / 09:10 / 09:20 decision slots. The fetch's own visible window ends at 2026-10-31 Beijing 10:28; the later turns are carried by the run handoff, which this study trusts as its own earlier work. The goal-relevant turns: the four-cut approval and publish, the completion check and second publish push, the framework and pitfall examples, the real-diary vs fake-persona answer, the form rejection and all-new-accounts recalculation, the duplicate comment and failed deletions, the p634 tool-fault rounds carried into 2026-11-01, and the undecided 2026-11-01 morning decisions.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first 70/30, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, 5-voiceover arrival, single-account 200 from 2026-10-28, X reports to side chat, main chat FB only, Victoria single-line revert 2026-10-30) as background only — every dated claim in this note is sourced to the conversation window, the run handoff, or a prior note above, not to memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract, and was restricted to Markdown to avoid matching base64 image data inside brief HTML files. No credentials, cookie values, or proxy secrets were reproduced in this note; only file names, counts, and link URLs already reported to the user are referenced.
