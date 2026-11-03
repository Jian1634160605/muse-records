# Study Notes - 2026-10-28 - 重复工作自动化
<!-- studying-run-start: 2026-10-27T19:17:44Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now six days since the 2026-10-22 delivery.
- Prior notes read in full: `2026-10-20/goal.md`, `2026-10-21/goal.md`, `2026-10-22/goal.md`, `2026-10-23/goal.md`, `2026-10-24/goal.md`, `2026-10-25/goal.md`, `2026-10-26/goal.md`, `2026-10-27/goal.md`.
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated.

## Already Covered in Main Chat

- 2026-10-27 Beijing afternoon: user approved the Qin Hao material-library inventory (秦浩 only; Li Feng folder skipped entirely) and the priority shortlist, then asked how long downloading would take and whether mirroring the library would be faster.
- 2026-10-27 Beijing afternoon: user proposed screen-recording selection, then ordered it stopped; selection and editing now use original films only.
- 2026-10-27 Beijing afternoon: user widened generic-material scope to all doctors, then corrected himself — other doctors' voiceovers cannot be used on Qin Hao accounts (impersonation).
- 2026-10-27 Beijing afternoon: user asked for a per-file classification taxonomy so he can build folders and upload; the assistant gave the person-then-stage folder scheme and file-naming rule.
- 2026-10-27 Beijing 18:04: user ordered the repaired X CLI line to be the permanent default route, with no switching back and forth.
- 2026-10-27 Beijing 19:35: user ordered that any FB-content approval card must summon him via WeChat; the rule was written into the 19:45 one-off task.
- 2026-10-27 Beijing evening: user chose option A (post today's 5 items at 19:45, plus the previous night's 2 items) and, when only 1 of 7 posted, ordered an immediate repost of the remaining 6, then said he would check the proxy himself and told Muse to wait for his message.
- 2026-10-28 Beijing early morning: X p56 failed 13 consecutive times on the same cookie-acquisition fault, and the 02:13 round stopped retrying and did read-only verification only.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Six new worked automation instances (例24–29), all from 2026-10-27 lived operations and the 2026-10-28 early-morning X rounds. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: 2026-10-27 is the day two of the 10-27 note's open gaps actually closed in practice. First, the repaired tool became a named default route with a length rule attached (例24), instead of another one-off workaround. Second, the missing circuit breaker from 例23 finally appeared — not as a number the user set, but as a stop-retry decision after 13 identical failures (例29). The remaining gap is symmetric: the FB proxy failure now has an explicit hold (例26), but no retry budget or re-check time was set, so "wait for the user" is the stop condition, not a timer.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, sixth day.
2. Standing constraints — **present, expanded by four in this window**:
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
   k. **NEW**: a repaired tool route becomes the default route by user decision, not by habit — no switching back and forth in the same window (2026-10-27 18:04 Beijing; see 例24).
   l. **NEW**: the 3-second WeChat escalation is now explicitly attached to FB-content approval cards, not only to DM cards (2026-10-27 19:35 Beijing; see 例26).
   m. **NEW**: a download is only what Muse itself confirmed it wants — no bulk extra downloads; chat transfer is impossible above 100 MB per file, so large material must be pulled from the library, not sent through chat (2026-10-27 18:21–18:22 Beijing; see 例27).
   n. **NEW**: a retry loop gets a stop — after 13 consecutive identical tool failures, the round stops retrying and does read-only verification only (2026-10-28 02:13 Beijing; see 例29).
3. Low-risk pilots demonstrated — **now twenty-nine worked examples** (例1–29 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–23 carried from the 10-27 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24), 发布任务的"用户已批准"硬门槛 (10-25), autoclip / Dula Clip AI 的接入评估 (10-26 00:26–00:46 Beijing, candidate, not adopted), 六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法 (10-25), 内容为主 70/30 + 每号每天 1 条 + 成品直发门 (10-26 afternoon), 明天 18 条秦浩成品的排期、计数与来源澄清 (10-26 evening), 已发视频的水印审计与"只隐藏、不删除" (10-26 evening), 18:45 失败后的恢复路径选择 A 与 19:45 v2 成功 (10-26 evening), autoclip 实测闭环 (10-26 17:18 Beijing), X p20 的无限重试与 226 新限 (10-26 afternoon to 10-27 early morning).

**例24：修好的 X CLI 线成为默认路线 + 280 字精简规则（2026-10-27 Beijing 18:04，用户定）**
1. **盘点** — X 大号 @TheEasySale1 的 twitter-cli 从 2026-10-26 16:53 Beijing 起连续报 `Failed to init ClientTransaction`，p20–p24 卡住；p20–p23 已靠浏览器路线发出，工具线本身仍未恢复。
2. **拆解** — 补丁修的是签名获取：带登录 cookie 取首页、适配新版 webpack ondemand 映射，warm_ct 输出 WARMED。修好后用户 18:04 Beijing 定："修补好了就一直用修好的线"，不再来回切换。
3. **量化** — 例外只有一条：p24 原文加权约 287，超 API 280 上限，CLI 撞 186，故 18:04 Beijing 仍走浏览器原样发出（tweet_id 2115021837948363128，推文数 317→318）。p25 已按此精简到加权约 276，原文记在 post-log.md。
4. **自动化设计** — 默认规则分两条门：280 字以内走修好的 CLI 线；超 280 的先精简到 280 内再走 CLI，精简版发、原文留档备查。蓝 V 长帖特权只在 X 网页和 App 编辑器里生效，第三方公开接口一律按 280 卡 — 用户 18:06 Beijing 问"我不是蓝V吗"时主代理就是这样解释的，不是蓝 V 失效，是两条门规则不同。
5. **边界** — 用户若觉得精简亏了，可改口让超限的一律走浏览器原样发、不改文案；窗口内用户未改口，默认仍是先精简再走 CLI。
6. **验收** — 2026-10-27 当天 X 共发出 25 条（p20–p44，日报 21:45 Beijing），推文数 313→338；此后 p33、p35、p36、p40、p43、p44 等多轮均按精简规则走 CLI 一次发出，未撞 186。

教学价值：工具修复的终点不是"能发了"，而是用户亲口把"用哪条线"定为默认，并把例外（超限）写成规则；没有这句定性，下一次故障又会回到"浏览器还是 CLI"的摇摆。

**例25：被截断的报错掩盖了真因 186（2026-10-27 Beijing evening，多轮）**
1. **盘点** — p33、p35、p45 等轮次的脚本报错只显示 `Getting Twitter cookies...` 前缀，表面看像 cookie 获取故障。
2. **拆解** — `~/workspace/x-ops/post_next_acct2.py` 把 stderr 截断到 200 字以内，真报错被盖住。详细模式复跑才露出完整返回：`Twitter API error (HTTP 0): Twitter API returned errors: Authorization: Tweet needs to be a bit shorter. (186)`。
3. **量化** — p33 在 19:33、19:43、19:53 三轮同错后，删两处赘述（`，别留弱口令裸奔` 和 `，少一个入口少一分风险`）精简发出；p35 删一处（`，全车资料和对话记录说没就没`）发出；p45 在 21:53、22:03、22:13 三轮同错后，再精简到 107 字发出（tweet_id 2115084940312514856）。cookie 本身已加载、CT 缓存正常，故障不在取 cookie 那一步。
4. **自动化设计** — 诊断规则：凡是只剩前缀的报错，先用详细模式复跑一次再定性，不凭前缀归因；发帖前的时间线核实（最新帖、推文数、会话 authenticated/verified）仍要做，但它只能排除平台信号，不能证明超长与否。
5. **边界** — 2026-10-28 凌晨 p56 的同类前缀后来被证明确实是 cookie 环节故障（见例29），所以"前缀 = 超长"也不是通解 — 前缀只说明信息不足，不说明原因。
6. **验收** — p33、p35、p45 均在精简后走 CLI 发出，原文留在 promo-queue.json 的 original_text 字段；post-log.md 补记了 p33 的 19:57 成功条目，避免后续轮次误判 p33 仍待发。

教学价值：日志截断本身就是一个故障模式；自动化系统的可观测性（完整报错）比重试次数更重要 — 截断的日志会让正确归因晚三轮。

**例26：FB 19:45 一次性任务绕开旧格式轮次 + 代理断线的显式留仓（2026-10-27 Beijing evening）**
1. **盘点** — 17:45 和 18:45 轮次已按无答复跳过；旧轮次格式仍按 v1/v2 找料，18:45 轮仍按旧格式、还列着已删的 Simon、Cora，只会跳过或找错料。用户 19:19 Beijing 选 A：今晚 19:45 直接按今日 5 条发（Victoria b0、Fowler a3、Emerson 17、Jioklm 3e、Jusa 03），昨晚 Jioklm 视频 + Jusa 拉皮文字帖一起处理；Simon 的 05 留仓等新号，不改派。
2. **拆解** — 动手前先核查：Jioklm 主页现可见的不是昨晚那条 "Thirty days" 视频，10-26 的 posted 记录里也没有 Jioklm、Jusa，昨晚两条按未发处理；19:45 任务发之前还会再查一次，万一已发只跳过已发那条。
3. **量化** — 19:45 一次性任务只发出 1 条：Victoria 主页 Dr.qh88，今日 b0，https://www.facebook.com/reel/2736884813380236，自评已留。未发出 6 条：Fowler a3、Emerson 17、Jioklm 3e、Jusa 03、Jioklm 昨晚视频、Jusa 昨晚文字帖。19:45 轮本身是绕开旧轮次直接发，不改常规定时任务的定义。
4. **自动化设计** — 失败分两层：第一层是浏览器窗口打不开 FoxProfile 面板（127.0.0.1:8000 和 localhost:8000 报 invalid_request）；用户 20:47 Beijing 下令"现在就重发剩下6条"后，第二层是更底层的 ProxyUnreachable — Fowler fb-3651（20004 线）、Jioklm fb-73057（20010 线）、Jusa fb-91565（20011 线）、Victoria fb-victoria（20002 线，顺手测的）全报代理那端连不上，浏览器根本起不来。19 点多 Jioklm 环境还正常打开过主页，线是 19 点多到 20:33 之间断的；X 那条线是另一条，20:43 还正常发了 p38，不是整台机器断网。
5. **边界** — 没有跨号登录、没有输密码、没有绕验证；环境都是干净停下的。这次没有弹出审批卡，所以按用户 19:35 定下的那条，没有需要他点的卡 — 但 19:35 的规则本身已写进任务：发 FB 内容时一弹出审批卡就微信喊他，卡出来 3 秒未点立即喊，不等超时，主聊天同步说明。用户 21:02 Beijing 说"我先查代理，你等我消息"，6 条原样留仓、不自动重发。
6. **验收** — 未验收：1/7 已发，6 条待补发，重发时机取决于用户查代理的结果，不能默认已补发；Simon 05 仍留仓。

教学价值：例21 的 A 路径在这里复用了一次 — 绕开旧格式、显式带入、按条报结果；但新教训是，失败原因会换层（面板打不开 → 代理连不上），同一批料的两次失败报告不能互相沿用，必须逐层重测。

**例27：秦浩素材分类法 + 只下确认项的下载口径（2026-10-27 Beijing afternoon–evening）**
1. **盘点** — 素材库盘点（只读、未下原片）：顶层文件夹 15 个，实际拆分 21 个单位 — 患者 19 个（含待确认"小鱼临时"）、模特 2 个单独列；口播 3 批 40 条视频 + 1 图约 8.3 GB；日常 0。缺口：患者长期恢复期（2 天 / 7 天 / 30 天 / 3 个月）几乎全缺、独立划线文件夹 0、日常 0；仅有的 7 天 / 3 个月在模特文件夹内。
2. **拆解** — 用户 15:35 Beijing 问"患者文件里的分类标记"，并贴了一张库内截图；主代理给的方案核心是三句话：先按人拆，再按阶段分，一个文件只进一个阶段文件夹。顶层：秦浩 / 患者（一个患者一个文件夹）/ 模特（单独，不算患者）/ 口播 / 日常。
3. **量化** — 单个患者文件夹固定 14 个子文件夹，只建已有阶段的，缺的别建、别拿别人顶：01_术前 / 02_术前划线 / 03_面诊 / 04_手术中 / 05_术后即刻 / 06_查房 / 07_拆线 / 08_恢复2天 / 09_恢复7天 / 10_恢复30天 / 11_恢复3个月 / 12_对比图 / 13_人文跟进 / 00_待分拣 / 99_排除。文件名改成"患者代号_项目_阶段_日期_序号"，如"案例01_鼻子_术前划线_2026-07-09_01.mp4"。每个患者文件夹根目录配一张信息表，写清 7 样：患者代号（不用真名）、年龄段和项目、已有和缺的阶段、记忆点一句话、患者原话一句（没逐字听清写"未确认"、不编）、可发确认、打码要求、水印归属。截图那批的拆法也逐条给了：2026-8-3 的 2 位客户拆成 2 个患者文件夹，2026-8-4 的 5 位拆成 5 个，看不出阶段的先进待分拣。
4. **自动化设计** — 两条复用规则写进了分类法：通用医护空镜（消毒、戴手套、器械台、手术灯、洗手、换药，无患者辨识度）1 秒左右当过渡可跨视频、跨账号重复，单独建通用库；患者专属画面（脸、划线特写、切口缝合特写、前后对比、查房送花）哪怕 1 秒也不复用到别的患者身上。通用范围放宽只限真正不带医生身份的片段：李峰和其他医生的口播带本人脸和声音，一律停下、不下载、不当通用素材（用户 15:30 Beijing 自纠："不是秦浩的口播还能用吗？怕是不行哦"）；李峰日常里只列了一份疑似不带医生身份的空镜清单（15 条微信小视频），只记清单、没下载、没确认为可用。
5. **边界** — 录屏选片已停用：绿联云实时推流转码常黑屏 / 无声，正式录屏没做成，试点 8 条全部受限用待复核；此后选片 / 剪辑走原片路线。下载口径收窄到只下确认项：秦浩口播 8.20 批里已确认可用的 5 条（104058、104331、104506、104927、105202），不下 8.20 剩下 3 条、不下 8.26、9.8 批；聊天窗口单文件上限 100 MB，口播单条 150–700 MB，根本传不了，大素材一律由 Muse 直接从素材库下载。
6. **验收** — 5 条全部已下齐并核对大小 / 时长，存 ~/workspace/your_files/秦浩口播-确认5条-20261027/，合计 896.8 MB：104058 157.5 MB 41.5 秒、104331 183.3 MB 48.4 秒、104506 213.7 MB 56.4 秒、104927 195.6 MB 51.7 秒、105202 146.7 MB 38.8 秒。之前那 8 条的浏览器下载因看不到下载管理器、无法核实落盘，状态只能写"未核实"，用户 15:37 Beijing 说自己去素材库下那 8 条、放进他建的文件夹，浏览器任务已关闭，不再由它核对。

教学价值：分类法本身就是自动化 — 文件夹结构 + 命名规则 + 信息表 7 字段 = 以后剪辑时不用每次翻库、不用猜阶段、不用编天数；"只下确认项"则是下载自动化的反向规则：不下 = 不制造新的待核对库存。

**例28：内容池算术 + 每周补料节奏（2026-10-27 Beijing afternoon，用户问、主代理算）**
1. **盘点** — 用户连问三件事：一个患者能剪几次、多久更新一次素材、15 个案例 + 10 条口播能做多少内容。
2. **拆解** — 一个患者能剪几条取决于素材量，不是固定数：素材薄的只有 1 条操作过程，只能出 1 条；素材全的（术前、面诊、手术、查房、拆线、恢复 7 天、30 天、3 个月 + 患者自述 + 医生讲解）拆出 8–10 条是天花板，不是平均数。10 条成立的前提是 10 条都不一样（画面和钩子都不同），同一段 10 秒换音乐、换文案在 10 个号上发 10 遍不算 10 条内容，是重复。
3. **量化** — 按平均 3–4 条算：库里 19 个患者约 50 条可用量级（打完折）；30 个案例约 90–120 条患者视频；口播按 10 条新 + 库里挑出能用的算约 20–30 条；内容池合计约 110–150 条，不算图文和日常。按现行每号每天 1 条、5 个号每天 5 条算：现手头 18 条成品 + 库里约 50 条约撑 13 天；15 + 10 那批单独约 55–70 条，约撑 11–14 天；30 案例池约撑 22–30 天。若改回每号每天 3 条：每天 15 条，50 条只够 3–4 天，90 条只够 6 天；每周需约 30 个新患者，基本续不上。
4. **自动化设计** — 更新节奏定为每周固定补一次，每次给三样：本周新患者（目标 7 个左右）、老患者的恢复跟进（7 天、30 天、3 个月到了就补，一个老患者又能多出 1–2 条）、口播 2–3 条。库存红线：手里随时留够至少 7 天的量（35 条），低于这个数就加急补，别等到 0；第一次补料最好在 7 天内给，不要拖到第 13 天。用户 14:47 Beijing 问"目前你说你要15个案例和10个口播，但是内容你能做多少个呢，还有后续我多久给你更新一次你知道吗"，主代理的回答就是上面这套算法，用户回 "ok"。
5. **边界** — 15 个是新案例的补量（顶层 15 个补到 30 个），秦浩口播另算、不包含在 15 个里；按实际患者算，库里已有 19 个，新 15 个到了约 34 个，多出来的是缓冲。排计划按平均 3–4 条算保底，好案例按 8–10 条算上限红利，不把薄案例也按 10 条算。
6. **验收** — 未验收：用户 18:07 Beijing 说正在准备 15 个新案例素材 + 另算的秦浩口播，到货后按清单核对阶段、记忆点、原话、授权 / 打码；一周新增几个可拍、可发患者这个数用户尚未回答，补料节奏的最终版仍取决于它。

教学价值：库存算术要把"平均"和"天花板"分开记 — 按天花板排计划会高估库存、按平均排计划不会断档；补料节奏（每周一次 + 7 天红线）是消耗速度的函数，不是日历习惯。

**例29：X p56 的熔断终于落地（2026-10-28 Beijing 00:03–02:53）**
1. **盘点** — 队列首条 p56（账号频繁掉线排查体，加权约 267，未超限）从 00:03 Beijing 起连续失败，`post_next_acct2.py` 返回 rc=1，stderr 仅见 "Getting Twitter cookies..." 前缀。
2. **拆解** — 与例25 不同，这次不是超长：warm_ct 复测 WARMED，CT 缓存正常，故障在发帖时 cookie 获取环节；会话 authenticated=true、verified=true，最新帖仍是 2026-10-27 23:53 Beijing 的 p55（2115109768197263482），p56 未发出、仍 pending；今日用户无手动新帖、无重复。status 推文数在轮次间漂移（370→371→373→374→377→380→382→390→393→395），但时间线前列无新自有帖，漂移不计为已发 — 计数与时间线不一致时以时间线为准。
3. **量化** — 连续同类失败计数：00:03、00:13、00:23、00:33、00:43、00:53、01:03、01:13、01:23、01:33、01:43、01:53、02:03，共 13 次，已远超 x_cli_init_failure_triage 技能"三次同类失败即停重试"的阈值。
4. **自动化设计** — 02:13 Beijing 轮次起停重试：不再运行 post_next_acct2.py，只做只读核实（会话、时间线、队列状态），队列 p56–p101 共 46 条原序保留，未追加后备草稿。02:23、02:33、02:43、02:53 轮次沿用同一决定。
5. **边界** — 正式暂停 10 分钟重试节奏、cookie 获取环节下一步诊断由谁动手，仍待主代理定；本 note 不擅自定数、不改定时任务定义。
6. **验收** — 部分验收：熔断动作本身已执行（停重试 + 只读核实 + 记账），但根因未出、正式暂停未定、队列未推进 — 例23 的"重试预算"从建议变成了实践，数字（13 次）仍是事后计数，不是事前阈值。

教学价值：熔断的价值不在停的那一刻，而在停之后不再产出同样的失败汇报；事前阈值（3 次）与事后计数（13 次）之间的差，就是下一次要补的规则 — 阈值必须写进任务正文，否则每一次熔断都要靠人工在第 13 次才喊停。

附带实例（同一窗口的周报复跑收尾）：10-27 note 里蔡园庆"有效"6 vs 0 的定义冲突、单号安全量测定 Day 1 基线（Victoria 冷首条 0、跟进 3 条、其他 6 号 0）在本窗口内没有新进展；单号安全量测定的口径（内容量 vs 私信量）在内容为主改动后仍待说明 — 这两项沿用 10-27 note 的待定状态，不在本窗口内虚构进展。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, sixth day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.
Step 3 (NEW, from 例27): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27**: 例26 的一次性任务是同一条线的下一环；旧格式轮次仍未同步修订，是新缺口 — 下一次发帖前必须先对齐任务正文与今日料单，否则还会再绕一次。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 2026-10-26 的新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — Victoria 冷首条每天 3 → 5 → 7 → 9，Fowler、Emerson 2 → 3 → 4 → 5，4 个新号 1 → 2 → 3 → 4；无信号每 2 天升一档，有信号则停该号、退回上一档并报用户；Day 1 基线：Victoria 冷首条 0、跟进 3 条、其他 6 号 0 — 测定才第一天，尚不能估出天花板；例28 的内容池算术可能改变"量"的定义（内容量 vs 私信量），测定口径须在下一轮说明。
6. **秦浩素材库的分类与补料闭环（NEW）** — 例27 的分类法 + 例28 的每周补料节奏是同一条线：用户按分类法建文件夹、按清单给 15 个新案例 + 另算口播，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数（1 条 / 5 条 / 10 条）换掉平均估算；通用空镜库单独建，与案例料分开标。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-10-28T19:17:44Z (24h, per study task plan). By then: FB 剩余 6 条是否在用户查完代理后补发（Victoria b0 之外 6 条的去向）；X p56 的正式暂停决定与 cookie 环节诊断结果；15 个新案例 + 另算口播是否到货、到货后逐案实数与缺口清单；单号安全量测定 Day 2–3 的 ladder 执行与口径说明；蔡园庆"有效"定义的确认；Jioklm 主页 10 月 23 日视频的单独隐藏；Jusa 主页改名决定；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: six new same-day worked examples (24–29) observed and preserved; the repaired-line default, the truncated-log diagnostic, the format-bypass plus proxy hold, the classification taxonomy plus narrow-download rule, the content-pool arithmetic plus weekly cadence, and the stop-retry circuit breaker are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例29 尚未由用户定数）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: FB 剩余 6 条的补发时间取决于用户查代理的结果，未定；X p56 的正式暂停与诊断归属未定；15 个新案例与口播未到货；单号安全量测定口径未定；蔡园庆"有效"定义未定；Jioklm 主页视频的单独隐藏未完成；Jusa 改名未定；d1、05 的前后对比同一人疑点未单独确认；7 条首批成品的音乐版权风险未解决；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "修补好了就一直用修好的线，OK" (2026-10-27 18:04 Beijing, repaired-line default)
- "要发fb内容需要审核卡的时候叫我" / "微信叫我" (2026-10-27 19:35 Beijing, FB approval-card WeChat rule)
- "A，昨晚两条也一起处理" (2026-10-27 19:19 Beijing, 19:45 option A plus previous night's 2 items)
- "现在就重发剩下6条" (2026-10-27 20:47 Beijing, immediate repost order)
- "我先查代理，你等我消息" (2026-10-27 21:02 Beijing, proxy hold)
- "不是秦浩的口播还能用吗？" / "怕是不行哦" (2026-10-27 15:30 Beijing, non-Qin Hao voiceover self-correction)
- "你就不要录屏了" (2026-10-27 15:25 Beijing, screen-recording stop)
- "你确认你自己要的那几个就行，不要搞特别多" (2026-10-27 18:22 Beijing, narrow-download rule)
- "ok" (2026-10-27 14:52 Beijing, accepting the content-pool and weekly-cadence arithmetic)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-20/goal.md`, `2026-10-21/goal.md`, `2026-10-22/goal.md`, `2026-10-23/goal.md`, `2026-10-24/goal.md`, `2026-10-25/goal.md`, `2026-10-26/goal.md`, `2026-10-27/goal.md` (2026-10-27 and 2026-10-26 read in full, earlier ones carried via the 10-27 note's review; carried forward the goal snapshot, standing constraints, worked examples 1–23, the teach-plan structure, and the 10-27 note's open questions on 例5, 例10, the checklist re-ask, formalizing cards, the autoclip live test, the A-path repost, the 18-video count, and the p20 retry budget).
- **Repetition search**: keyword variants {修好的线, 280, 186, 一次性任务, 代理连不上, 素材分类, 通用素材, 口播5条, 录屏停用, 每周补, 空镜} grep-searched over `workspace/goals/goal/agent_notes/` and `workspace/goals/goal/briefs/` (filenames included; briefs dir lists exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: 修好的线 / 一次性任务 / 代理连不上 / 素材分类 / 通用素材 / 口播5条 / 录屏停用 / 每周补 / 空镜: **zero hits** in any prior note or brief filename — new to the written record. 280 / 186: hits only inside base64 image data in the two brief HTML files, not as content — disregarded, not a topic hit. Every one of today's instances was set by the user or narrated to him live in main chat in the 2026-10-27 window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-26T19:09:09Z → 2026-10-27T19:20:33Z, plus the run's chunked conversation handoff covering 2026-10-27 Beijing daytime through 2026-10-28 Beijing early morning. The goal-relevant turns: the material-library inventory and mirroring discussion, the screen-recording proposal and stop order, the generic-material widening and non-Qin Hao voiceover self-correction, the per-file classification taxonomy request and answer, the 5-voiceover narrow download and arrival, the X CT repair and repaired-line default, the 280-trim rule and blue-V distinction, the FB 19:45 option A decision and 1/7 result, the proxy-unreachable repost failure and user proxy check, the FB approval-card WeChat order, the content-pool arithmetic and weekly cadence, and the X p56 13-failure stop-retry decision.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first 70/30, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, 5-voiceover arrival, 15-case preparation) as background only — every dated claim in this note is sourced to the conversation window or a prior note above, not to memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract. No credentials, cookie values, or proxy secrets were reproduced in this note; only ports, file names, and counts are referenced.
