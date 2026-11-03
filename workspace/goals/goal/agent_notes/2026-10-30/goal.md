# Study Notes - 2026-10-30 - 重复工作自动化
<!-- studying-run-start: 2026-10-30T00:47:33Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 已定下目标，下一步先盘点现有重复工作清单.
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now eight days since the 2026-10-22 delivery.
- Prior notes read in full: `2026-10-29/goal.md` and `2026-10-28/goal.md`; earlier notes carried via the 10-29 note's review (`2026-10-20` through `2026-10-27`).
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated.

## Already Covered in Main Chat

- 2026-10-29 Beijing 16:24: user pointed out that, apart from the main account, the other FB accounts had never posted a video, and asked why no videos were posted for them.
- 2026-10-29 Beijing 16:28: user ordered all other accounts' static IP lines changed to the main account's line, to test whether that fixes publishing.
- 2026-10-29 Beijing 16:32: user said, in frustration, that no more approvals should be sent to him and the agent should pass them all itself; the assistant replied that approval cards are a system safety mechanism it cannot click or switch off.
- 2026-10-29 Beijing 16:33–16:34: user ordered one work for every account, and for every account both the Page and the personal profile to post.
- 2026-10-29 Beijing 17:42: assistant reported 9 of the 10 posts published and link-verified, with only the Fowler Page post stuck in the Reel editor at the WhatsApp-button prompt step.
- 2026-10-29 Beijing 17:46: user asked to keep publishing the one post that had not gone out.
- 2026-10-29 Beijing 18:12: assistant reported the Fowler Page post finally published on the fifth attempt, the three accounts that lost login restored, and the second round of 10 complete.
- 2026-10-29 Beijing 19:35: assistant reported the Fowler Page self-comment done, but the remaining 7 self-comments could not be done because Reel pages froze on open, and that it would retry when the line recovers.
- 2026-10-30 Beijing 07:31: assistant asked the user to decide one thing: only 3 finished items remain unposted (b4, d2新, 60, originally allocated Emerson / Jioklm / Jusa), after which directly postable finished stock hits zero and the next batch is the 5 arrived Qin Hao voiceovers needing editing plus review; no user answer to that question appears in this window.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Six new worked automation instances (例36–41), all from 2026-10-29 lived operations and the 2026-10-30 early-morning question. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: 2026-10-29 is the day the automation question stopped being "which rule is missing" and became "what breaks when a human has to carry the automation." The 10-post round finally proved the non-main accounts can publish, but only through a chain of human-ordered workarounds — a shared IP line, a main-site post flow that bypassed the stuck editor, and a cookie-backup login restore after a browser crash. Each workaround worked, and each one added a hidden debt: one shared line for five accounts, one unverified fifth attempt, and a self-comment backlog that grew instead of clearing. Automation that only works by stacking workarounds is a procedure, not yet a pipeline.

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, eighth day.
2. Standing constraints — **present, expanded by three in this window** (items a–q carried from the 10-29 note):
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
   r. **NEW**: all five FB accounts now share the main account's line by user order — the user ordered the change 2026-10-29 Beijing 16:28 to test whether it fixes publishing; the association risk of one line for many accounts was already known and accepted for the earlier Fowler/Emerson sharing, and is now extended to all five, so any future account trouble must be read against this shared-line fact first (see 例36).
   s. **NEW**: "no more approval cards, pass them all yourself" is not achievable — restated 2026-10-29 Beijing 16:32 after the user's frustrated order; the mitigations that do exist are scheduled tasks that do not pop cards, and the per-category "始终允许" choice (Messenger DM sending already set), so approval friction is a standing cost to design around, not a switch to flip (see 例40).
   t. **NEW**: cookie-backup restore is a proven recovery for browser-crash login loss — stop the browser, copy the `cookies.sqlite.bak` back over `cookies.sqlite`, delete the `-wal`/`-shm` files, relaunch — applied successfully to Fowler, Jioklm, and Jusa 2026-10-29 Beijing evening (see 例37); it restores login without asking the user to re-login or hand over credentials.
3. Low-risk pilots demonstrated — **now forty-one worked examples** (例1–41 below).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–35 carried from the 10-29 note: 团队周报 (10-19), FB 去重台账 (10-20), FoxProfile 免扫码登录 (10-21, still the only completed card, still unlogged to the goal timeline), 评论单出口拆分 (10-22), 评论计数串行锁 (10-22), 私信服务器端核验 (10-22), 删自设限额/平台信号唯一标准 (10-23), 30 秒实时监控 hook (10-23), 微信求助通道 (10-23), 审批卡 3 秒微信触发 (10-24), 有问题第一时间讲 (10-24), 发布流水线的两道门 (10-24), FoxProfile 链路抖动与重启补发 (10-24), X p6 归因纠错 (10-24), 发布任务的"用户已批准"硬门槛 (10-25), autoclip / Dula Clip AI 的接入评估 (10-26 00:26–00:46 Beijing, candidate, not adopted), 六个 FoxProfile 环境的登录态核验与 Cora 的 45 秒等法 (10-25), 内容为主 70/30 + 每号每天 1 条 + 成品直发门 (10-26 afternoon), 明天 18 条秦浩成品的排期、计数与来源澄清 (10-26 evening), 已发视频的水印审计与"只隐藏、不删除" (10-26 evening), 18:45 失败后的恢复路径选择 A 与 19:45 v2 成功 (10-26 evening), autoclip 实测闭环 (10-26 17:18 Beijing), X p20 的无限重试与 226 新限 (10-26 afternoon to 10-27 early morning), 修好的 X CLI 线成为默认路线 + 280 字精简规则 (10-27 18:04 Beijing), 被截断的报错掩盖了真因 186 (10-27 evening), FB 19:45 一次性任务绕开旧格式轮次 + 代理断线的显式留仓 (10-27 evening), 秦浩素材分类法 + 只下确认项的下载口径 (10-27 afternoon–evening), 内容池算术 + 每周补料节奏 (10-27 afternoon), X p56 的熔断落地 (10-28 00:03–02:53 Beijing), X 推广线的发前加权复核 + 逐轮补草稿 (10-28 Beijing 05:23 to 10-29 Beijing 03:09), X 互动线的规则冲突 — 短间隔跳过 vs 平台信号-only，全天未决 (10-28 Beijing), FB 内容线的"已选版、未定号" — 内容批准 ≠ 发布批准 (10-28 Beijing daytime), 一案多版 + 批量成片 + 哈希去重 (10-28 Beijing daytime), 单号 200 目标 — 目标变了，度量还没跟上 (10-28 Beijing 11:08–11:14), 私信跟进梯队的服务器端核验 (10-28 Beijing daytime to 10-29 Beijing 00:38).

**例36：五号共用主号线 + 主页与个人主页双发的第一轮（2026-10-29 Beijing 16:24–17:42）**
1. **盘点** — 用户 16:24 Beijing 当面指出：除主号外，其他账号都没发过视频。主代理当场认了三点原因：以前把 Victoria 当主转化号、其他号只做养号和截流，视频料先给 Victoria；料不够时轮次缺料就跳过，其他号最先被跳；当天本来要补发的轮次先把 Fowler 的 3 条发错到 Victoria，后来其他号的代理线死了、上传也卡住，助理在等用户选方案、没继续硬发。
2. **拆解** — 用户 16:28 Beijing 下令把其他账号的静态 IP 都改成和主号一样的线、试试能不能解决问题；16:33 Beijing 下令给所有账号都发一个作品；16:34 Beijing 追加主页和个人主页都要发。合计 10 条：5 个号 ×（主页 1 条 + 个人主页 1 条）。
3. **量化** — 17:42 Beijing 报 9/10 已发且链接核验：Victoria 主页 0b、Victoria 个人 87、Fowler 个人 a3、Emerson 个人 17、Emerson 主页 05新、Jioklm 主页 3e、Jioklm 个人 p73057、Jusa 个人 f2、Jusa 主页 03。唯一未发：Fowler 主页 dr.qh。改线后 Jioklm、Fowler 已能打开 Facebook，Emerson 刚拉起、Jusa 当时未测 — 改线至少恢复了打开，不等于恢复了全部发布。
4. **自动化设计** — 可复用点有二：一是"缺料跳过"必须按号记账，不能只记总数 — 总数发了、某号 0 发时，总数会掩盖缺口，用户正是从"今天才知道"这一点发现问题的；二是用户指令本身就是一次自动化校准：从"主号优先"改成"每号每面各 1 条"，把分配规则写进了当轮的执行口径，而不是留在"主转化号"的旧心智里。
5. **边界** — 五号共用一线是用户为排障下的临时指令，不是已证明安全的长期配置；此前 Fowler/Emerson 共用的关联风险已知并被接受，这次是把同一风险扩展到全部五号。后续任何一号出现验证、限流或关联信号时，先查这条共用线，再查内容本身。
6. **验收** — 部分验收：9/10 当时已核验；Fowler 主页 1 条未验收，见例37。

教学价值：自动化系统里最难发现的故障是"某一路从未执行" — 没有按号的执行计数，系统会一直报告"今天发了 N 条"而无人知道某一号永远是 0；按号、按面的计数表是这类故障唯一的早期信号。

**例37：Fowler 主页的四次失败、一次未核验关闭、一次 cookie 备份恢复后成功（2026-10-29 Beijing 17:42–18:12）**
1. **盘点** — Fowler 主页 dr.qh 的 4a 试了两次、换 b4 又试了一次，走 Reel 编辑器点发布后都卡在同一个地方：弹出加 WhatsApp 按钮的提示，点了暂不后编辑器一直停在编辑页，主页动态和 Reels 列表里都没有新帖。
2. **拆解** — 第四次情况不同：上传完成再点发布，WhatsApp 提示点了暂不，等了 90 秒后编辑器已经关闭了 — 但这一步没有核验就不能算发出。随后 Fowler、Jioklm、Jusa 三台浏览器在打开 Fowler 主页时相继崩溃，新浏览器也拉不起来，报临时目录错误；系统重启后临时目录问题自愈、服务重新拉起，但三号登录态已丢、打开变登录页，Emerson 登录还在。
3. **量化** — 核验结果是实锤未发：Fowler 主页 Reels 列表仍只有 2 条旧帖，时间线最新仍是 10 月 22 号那条，当天无新帖 — "编辑器关了"不等于"发出去了"。第五次重发 4a 在 Fowler 登录用浏览器自己的 cookie 备份恢复后发出并核验作者与文案无误：https://www.facebook.com/reel/3817497068402843/ ；Jioklm、Jusa 也用同一办法恢复，5 号登录态全在。
4. **自动化设计** — 三条可复用规则：一是发布流程必须以"主站发帖流程"为备选路线 — Jioklm 主页那条正是用主站发帖流程（不是之前卡住的 Business Suite 路线）走通的，其他号随后按同样流程发；二是任何"编辑器已关闭"都必须以主页已发布列表核验为准，关闭只是过程信号，不是结果证据；三是浏览器崩溃后的登录恢复有现成手順（约束 t），应写进故障手册的第一步，而不是先向用户要重新登录。
5. **边界** — 第五次成功前，助理曾向用户要过"在自己指纹浏览器里把三号重新登录一遍、导新鲜 cookie"；该请求在 cookie 备份恢复成功后已不需要 — 但记录它很重要：向用户要登录动作是最后手段，不是第一步。
6. **验收** — 已验收：第二轮 10 条至此全部发完；Fowler 主页 4a 链接已核验。未验收：自评，见例38。

教学价值：发布自动化的验收标准只能有一个 — 发布列表里出现、作者与文案对得上；编辑器状态、上传完成、按钮点击都是过程信号，拿过程信号当结果是 10-22 私信气泡教训（例6）在发布侧的翻版。

**例38：自评欠账 7 条变 10 条的可能 + 11:00 定时重试（2026-10-29 Beijing 19:35 至 2026-10-30 Beijing 07:31）**
1. **盘点** — 除 Victoria 两条已留自评外，其余 7 条的自评未补；Fowler 主页 4a 的自评随后留好并核验，剩下 7 条在当晚补不成了：浏览器打不开 Reel 页面和主页视频列表，标签页一开就卡死，首页能加载、登录没掉，助理停手没再硬刷。
2. **拆解** — 欠账是会增长的：2026-10-30 Beijing 07:31 的晨间提问里写明，昨晚欠 7 条自评，11 点会重试补，线路还卡就停手；如果当天再发 3 条（见例41），欠账变 10 条，等线路恢复再一并补。定时任务 `fb-selfcomment-retry-1030`（runonce，2026-10-30 11:00 Beijing）就是这笔欠账的显式载体。
3. **量化** — 欠账数：7（当晚）→ 可能 10（再发 3 条后）；重试时点：2026-10-30 11:00 Beijing；停手条件：线路还卡就停，不硬刷。
4. **自动化设计** — 可复用规则：任何"发完再补"的后置动作（自评、转发、记账）都必须有独立的欠账计数和重试时点，不能只记在发帖成功的同一条目里 — 否则发帖成功会掩盖后置动作未完成，正如例36 里总数掩盖了某号 0 发。
5. **边界** — 自评重试不承诺"今天一定补成"；补完逐条核验、不重复留。
6. **验收** — 未验收：7 条自评在窗口结束时仍欠；11:00 重试结果不在本窗口内。

教学价值：发布流水线的"两道门"（例12）其实是三道：发、核验、自评 — 第三道没有独立计数时，它会悄悄成为永远的尾巴。

**例39：X 队列与去重台账的同日两次截断 + 备份恢复（2026-10-29 Beijing 18:01–18:02 及全天互动轮次）**
1. **盘点** — X 推广 p273 发出后，脚本写回队列时终端写入报 EPERM，promo-queue.json 被截断为 0 字节，原待发 p274–p535 全文丢失；同日互动侧 commented.json 也曾在写入时被截断为 0 字节。
2. **拆解** — 恢复路径是同一套：推广队列重建为最小队列（p273 已发 + p536、p537 待发），发帖日志补记，记忆日志补记，并立下"下轮发帖前必须先验证终端写入恢复，否则会再次截断"的门；去重台账则用备份副本恢复、按日志补齐 15:27–17:42 的 32 条再加本轮 1 条，之后记账改用文件工具（muse.edit / muse.write）完成，不再走被拒的 exec 写入。
3. **量化** — 推广侧损失：p274–p535 的全文（262 条草稿）丢失，只剩最小队列；互动侧 commented.json 在恢复后从 392 条起步，到窗口结束时已回到 580 条以上（2026-10-30 Beijing 07:49 轮次记 580 条），说明恢复后的记账仍在连续追加。
4. **自动化设计** — 两条可复用规则：一是任何队列/台账文件在写回前必须有备份副本 — 备份是恢复的前提，不是事后补救；二是写入通道本身要可切换：exec 写入被拒时，文件工具是备用通道，通道切换应写进轮次手順，而不是每次现场发明。
5. **边界** — 丢失的 p274–p535 全文无法从截断后的文件里找回；重建的只是"能继续发"的最小队列，不是原队列 — 两者不能混称为"已恢复"。
6. **验收** — 部分验收：推广线在 p536、p537 后继续发出（p538 起全天连续），互动记账恢复连续；未验收：原 262 条草稿全文的补回（若用户要补，需另行重建草稿，不是自动恢复）。

教学价值：台账文件的写坏比读坏更贵 — 读坏只会让一轮误判（见例40 的重复评论），写坏会让一整段未来消失；写前备份 + 写后校验是任何"队列"类自动化的底线，不是可选项。

**例40：去重台账读截断导致的重复评论 + 删除不可靠（2026-10-29 Beijing 全天互动轮次）**
1. **盘点** — 全天至少三次同帖重复评论：Dreamofkang 帖（19:26 轮次在已有 19:26 评论后又评一次）、lovejing0306 新版政策帖（19:48 已评、19:53 又评）、andynotbot 月神卡帖（22:05 已评、22:07 又评）。
2. **拆解** — 共同原因都是起轮时 commented.json 读取被截断（文件过长、100KB 上限），没看到尾部、漏看了上一轮记账，于是对同一帖又发一次。补救各不相同：lovejing 的重复用 delete 加 --yes 第三次才删掉、线程核验已无该评论；Dreamofkang 与 andynotbot 的两次 CLI 删除都 180 秒超时、重复评论仍在线，助理停手不再盲试。
3. **量化** — 互动侧当日新增评论在 X 日报里记为 220 条（含重复与删除），去重台账数从早上的约 258 条一路记到 2026-10-30 Beijing 07:49 的 580 条；重复数本身不大，但每一次重复都是一次"已评论"信号被台账读失败的证据。
4. **自动化设计** — 可复用规则已在当晚轮次里成文：选帖前必须先看 commented.json 尾部最新条目，避免截断导致误判；删除不是可靠的补救 — 超时两次即停手、记账订正，不追删到底。
5. **边界** — 台账里剔掉重复条目不等于帖子里的重复评论已删除；两者要分开记 — 台账干净、帖子仍有重复时，结论只能是"台账已订正、帖子重复仍在"，不能写成"已处理"。
6. **验收** — 部分验收：lovejing 重复已删；未验收：Dreamofkang、andynotbot 的重复评论仍在线，删除未生效。

教学价值：去重自动化的薄弱点不在"有没有台账"，而在"读台账读全了没有" — 读不全的台账比没有台账更危险，因为它会给重复动作发一张"未评论"的假通行证。

**例41：私信哨兵断线 + 15 分钟兜底的双层设计（2026-10-29 Beijing 17:48–18:12）**
1. **盘点** — 实时盯守（30 秒轮询 Messenger 线程列表、新入站即唤醒接手）从 17:48 起连续轮询失败，到 18:00 已失败 6 次，原因是写不了自己的状态文件，实时提醒断了。
2. **拆解** — 兜底在跑：15 分钟一轮的 CLI 直查仍在，刚查过 13 个线程都是我方消息在最后、没有漏接；用户 17:58 Beijing 追问"私信那个什么情况你说人话"后，助理用人话重讲了一遍：秒回断了、最晚 15 分钟内还是能知道、等哨兵修好秒回恢复。
3. **量化** — 断线时长：17:48 至重启恢复后实测正常（18:12 前后报修好）；兜底覆盖：13 线程、0 新回复、0 漏接；系统重启后哨兵自己恢复，实测一遍正常轮询、无新私信。
4. **自动化设计** — 双层监控是正确的自动化结构：快层（30 秒 hook）负责时效，慢层（15 分钟 CLI）负责不漏；快层断时，慢层把"秒回"降级为"15 分钟内知道"，而不是"不知道"。用户追问后的人话重讲本身也是设计的一部分：故障说明必须先讲"对客户意味着什么"（最晚多久知道），再讲技术原因。
5. **边界** — 哨兵的状态文件写失败是它自己的故障，不是 Messenger 或账号故障；修好后要实测一遍轮询，不能只看"服务起来了"。
6. **验收** — 已验收：哨兵恢复、实测正常、兜底期间 0 漏接。未验收：状态文件写失败的根因（重启自愈，未深究）。

教学价值：事件驱动自动化的验收要分两层 — 快层在、慢层在，缺一层时系统仍可用但时效降级；降级本身要向用户明说，不能等用户从"怎么还没回"里自己发现。

附带实例（同一窗口的成品库存清零预警，未决）：2026-10-30 Beijing 07:31 的晨间提问是例41 之外的下一个待定动作 — 成品里只剩 3 条没发过（b4、d2新、60），原分配是 Emerson 发 b4、Jioklm 发 d2新、Jusa 发 60；发完这 3 条，能直接发的成品库存就清零，下一批是已到货的 5 条秦浩口播，得剪辑加用户过目才能发；昨晚浏览器 Reel 页卡死还没复测，助理不承诺今天一定发成，发成以拿到链接核对为准。该提问在窗口结束时仍无用户答复，本 note 只记为待定，不记为已定。

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, eighth day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Starter they can copy: 任务名=X 大号撞 226 后手动补发；触发=自动发帖失败那天；输入=现成文案；输出=App 里手动发出+链接发我；耗时=3分钟.
Step 3 (from 例27, still open): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.
Step 4 (from 例31, still open): pick ONE disputed rule in current operations (short-interval skip is the live one) and write its two candidate wordings side by side — platform-signal-only vs short-interval skip — so the user can close it with one choice instead of re-answering it every round.
Step 5 (NEW, from 例36–38): pick ONE owed follow-up action (self-comments are the live one: 7 owed, possibly 10 if 3 more post today) and write its count, its retry time (2026-10-30 11:00 Beijing), and its stop condition (line still stuck → stop, do not force-refresh) — so a "posted" success never again hides an unfinished follow-up.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28, page-plus-profile round completed 2026-10-29**: 例36–37 是同一条线的下一环 — 非主号第一次按"主页 + 个人主页各 1 条"发齐；旧格式轮次仍未同步修订，任务正文与今日料单的对齐仍是缺口。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发；单号 200 目标下，面诊名额数本身也待用户定，见例34）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — 例34 的单号 200 目标可能改变测定的意义：测定原是"单号安全量"，现在单号本身成了 200 目标的载体；测定口径（内容量 vs 私信量）与 200 目标的度量（英雄号、爬坡、单号累计表）须在下一轮合并说明，不能各说各话。
6. **秦浩素材库的分类与补料闭环** — 例27 的分类法 + 例28 的每周补料节奏 + 例33 的一案多版与哈希去重是同一条线：用户按分类法建文件夹、直接供料，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数换掉平均估算；通用空镜库单独建，与案例料分开标；新套 03–01 的合并决定是这条线的下一个待确认项。
7. **X 互动规则冲突的关闭** — 例31 的短间隔跳过 vs 平台信号-only 必须由用户一句话关闭，并把结论写进任务正文、从执行条件里删掉被废的一条；否则下一轮仍会重复上报同一问题。
8. **欠账计数与写前备份（NEW）** — 例38 的自评欠账与例39 的队列截断是同一类缺口：任何后置动作与任何队列文件都需要独立计数 / 备份 + 写后校验；下一轮要把"欠账表"和"写前备份"写进发布与发帖轮次的手顺，而不是靠事后从日志里重建。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-10-31T00:47:33Z (24h, per study task plan). By then: 剩余 3 条成品（b4、d2新、60）是按原分配发还是留着，用户是否答复；7 条（或 10 条）自评在 11:00 重试后是否补齐；X 互动短间隔规则与调度重叠是否由用户关闭；FB 留仓与五号共用一线后有无验证或限流信号；单号 200 的英雄号、爬坡、面诊名额、单号累计表是否落定；音乐池隔离新规则是否获批；新套 03–01 是否合并、02 的水印与天数、04 的启用、05 的齐全性是否确认；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: six new same-day worked examples (36–41) observed and preserved; the shared-line decision, the main-site bypass plus cookie-backup recovery, the self-comment backlog count, the queue-truncation backup rule, the truncated-read duplicate mechanism, and the two-layer DM monitoring design are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例31 尚未由用户定数，例32 的 A 版选择，例34 的单号 200 与当日生效纠正，例36 的改线与双发决定，例40 尚未由用户定数）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: 剩余 3 条成品的发与留未定；7 条自评的 11:00 重试结果不在本窗口内；X 短间隔规则与调度重叠未决；五号共用一线后的长期关联风险未验证；X 原 262 条草稿全文丢失后是否补回未定；Dreamofkang 与 andynotbot 的重复评论仍在线；私信哨兵状态文件写失败的根因未深究（重启自愈）；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；音乐池隔离规则未获批；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "我发现一个问题哈，你管理的这些账号，除开那个主号其他账号你都没发过视频，我今天才知道" (2026-10-29 Beijing 16:24, the per-account zero-post discovery)
- "你把其他账号的静态IP都改成和主号一样 的你试试能不能解决问题！" (2026-10-29 Beijing 16:28, shared-line order)
- "后面不用再给我发审核了全部你自己过就行了，我烦了" (2026-10-29 Beijing 16:32, approval-frustration order, answered as not achievable by the agent)
- "那你现在给所有的账号都发一个作品" / "还有所有的主页都要发，主页和个人主页都要发！" (2026-10-29 Beijing 16:33–16:34, page-plus-profile round order)
- "修补好了就一直用修好的线，OK" (2026-10-27 18:04 Beijing, repaired-line default; carried from the 10-28 note)
- "我先查代理，你等我消息" (2026-10-27 21:02 Beijing, proxy hold; carried from the 10-28 note)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27/30/32/34/36 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计；单号 200 目标的度量是否与测定口径合并。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)
- 五号共用一线是长期配置还是排障临时态：若是临时态，恢复一号一线的时点与判据是什么，须用户定；若是长期态，关联风险的接受要显式记下来，不能只留在当轮口头。

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-10-29/goal.md` and `2026-10-28/goal.md` read in full; earlier notes (`2026-10-20` through `2026-10-27`) carried via the 10-29 note's review; carried forward the goal snapshot, standing constraints, worked examples 1–35, the teach-plan structure, and the 10-29 note's open questions on 例31, 例32, the checklist re-ask, formalizing cards, the FB 6-item hold, the X p67 trim, the 15-case arrival, and the single-account measurement.
- **Repetition search**: keyword variants {主页个人主页, 静态IP改, 共用同一条线, cookie备份, 队列截断, 自评欠账, 哨兵, 审批全自动, 只剩3条, b4} grep-searched over `workspace/goals/goal/agent_notes/` (Markdown only, to avoid base64 image blobs in brief HTML) and the brief filenames in `workspace/goals/goal/briefs/` (exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: **zero hits** in any prior note or brief filename for all ten variants — today's instances are new to the written record. Every one of them was set by the user or narrated to him live in main chat in the 2026-10-29 to 2026-10-30 Beijing window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-10-28T19:09:12Z → 2026-10-30T00:55:49Z, plus the run's chunked conversation handoff covering 2026-10-29 Beijing daytime through 2026-10-30 Beijing early morning. The goal-relevant turns: the user's per-account zero-post discovery and shared-line order, the approval-frustration order and the agent's cannot-bypass answer, the page-plus-profile 10-post order and its 9/10 then 10/10 result, the Fowler Page editor block and cookie-backup recovery, the self-comment backlog and 11:00 retry schedule, the Messenger sentinel outage and 15-minute fallback, the X queue and ledger truncations with backup recovery, the truncated-read duplicate comments, and the 2026-10-30 Beijing 07:31 question about the last 3 finished items (unanswered in window).
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first 70/30, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, 5-voiceover arrival, single-account 200 from 2026-10-28, X reports to side chat, main chat FB only) as background only — every dated claim in this note is sourced to the conversation window, the run handoff, or a prior note above, not to memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract, and was restricted to Markdown to avoid matching base64 image data inside brief HTML files. No credentials, cookie values, or proxy secrets were reproduced in this note; only file names, counts, and link URLs already reported to the user are referenced.
