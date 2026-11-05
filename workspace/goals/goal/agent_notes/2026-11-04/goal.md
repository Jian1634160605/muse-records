# Study Notes - 2026-11-04 - 重复工作自动化
<!-- studying-run-start: 2026-11-04T00:27:16Z -->

## Goal snapshot

- goal_id `goal_47ddf0ae009e` (workspace slug `goal`), category `productivity`, kind `outcome`, status `active`.
- Created 2026-10-19T04:51:26Z at the user's own request; current_state unchanged: 第一份盘点清单与第一张任务卡已交付，下一步逐个推进自动化。
- Value alignment: 把时间从重复劳动里释放出来，专注在增长和决策上。
- Learning state: mode `teach`, mastery band `novice`; mastery **not estimated** (no retrieval attempt and no five-field card yet; evidence label `tentative`).
- Goal timeline: **still zero entries** since creation, confirmed again via `user_goal.get` in this study. Brief `goal_briefing_135212c5fa67` （第一份盘点清单） delivered in main chat 2026-10-22T07:26:08Z; brief `goal_briefing_3e128ce38ec2` （第一张任务卡） delivered 2026-10-21T04:46:42Z. No user reply to either ask, and the checklist ticks are still not confirmed — now thirteen days since the 2026-10-22 delivery.
- Prior note read in full: `workspace/goals/goal/agent_notes/2026-11-03/goal.md`, which carries worked examples 例1–61 and standing constraints a–jj in full; this note does not re-copy them, it extends them with 例62–67 below.
- Time convention in this note: main-chat events are given in Beijing time (Asia/Shanghai, UTC+8), as the schedules and the assistant's own phrasing in the window use it; packet timestamps are UTC, converted by +8 hours where a Beijing time is stated. This run started 2026-11-04T00:27:16Z, i.e. 2026-11-04 Beijing 08:27.

## Already Covered in Main Chat

- 2026-11-03 Beijing 11:40–11:49: user asked about X progress, FB progress and overall data, then approved the breakthrough order — content first, overdue warm batches second, account expansion third.
- 2026-11-03 Beijing 12:15: assistant reported p634 finally sent after trimming, and the X 2026-11-03 daily report at 21:45 stated the morning failure was weighted-length 186, not a cookie-fetch fault.
- 2026-11-03 Beijing 17:37–17:47: user approved the boss–manager–employee org chart, added reviewer E07 with a 90-point gate, extended it to a dual gate for long content and then to a universal gate for all content, and set English external copy with bilingual video text.
- 2026-11-03 Beijing 17:49–17:58: user ordered Emerson personal-account cleanup and avatar/bio matching to the Xiaohongshu second account, set the Singapore/Shanghai persona and daily 09:00–11:00 posting, then said Dr.qh666 was deleted and persona content goes to the personal account only.
- 2026-11-03 Beijing 18:01–18:08: user gave the Dr.qh88 link as the unified funnel, authorised Muse to scrape the Xiaohongshu second note itself, and ordered only the 9 low-traffic Dr.qh88 Reels hidden, leaving the 5 high-traffic ones untouched.
- 2026-11-03 Beijing 18:11–18:16: assistant reported the 9 Reels could not be hidden — no Hide option in the Reels menu or in Meta Business Suite — and that Expire now was not clicked because it is not hiding.
- 2026-11-03 Beijing 18:20: assistant flagged the Chen Jie pre-op science item in the nose-matrix document against the 2026-10-27 non-Qin-Hao-voiceover red line and held Chen Jie content out of both Emerson personal and Dr.qh88 transition batches pending the user's sentence.
- 2026-11-04 Beijing 05:36–06:40: assistant reported two new duplicate-comment accidents (JustLikeBit triple, heitieya double) caused by checking a non-existent `id` field instead of `tweet_id`, with both delete attempts timing out and the duplicates still online.
- None found in this window about the goal itself: no reply to the 7-item checklist, no retrieval-prompt attempt, and no five-field task card from the user.

## What this study adds

Six new worked automation instances (例62–67), all from 2026-11-03 Beijing daytime through 2026-11-04 Beijing 08:27. All were set by the user or narrated to him live — they are new to the goal's written record, not new to the user, so they do not by themselves earn a new Letter (see the ruling in the finish-step output).

Key observation: today's window contains two different kinds of "fix" that must not be conflated. The p634 fix is a genuine root-cause correction (例62): a four-day misdiagnosis was replaced by a measured cause and the line resumed. The dedup fix is a fix that mutated (例63): the truncation failure was addressed, but a field-name error recreated the same visible accident twice more in one morning. A fix that changes the failure's mechanism without adding a check that would catch the new mechanism is not yet a closed loop — it is a new entry in the same lesson.

**例62：p634 四天误诊被纠正 — 真因是加权超长 186，不是取 cookie（2026-11-03 Beijing 12:15 前后）**
1. **盘点** — 自 2026-10-30 Beijing 10:43 起，推广线每轮都在 "Getting Twitter cookies…" 处中断、返回 rc=1，助理连续四天把它报成工具端取 cookie 故障；互动线（走存好 token 的 tw2.py 线）同期正常，账号 authenticated=true、verified=true，无 226/344 信号。
2. **拆解** — 纠正来自两处证据的合流：发帖脚本当时丢了 stdout，只凭 stderr 前段横幅定因；按严格口径重算后，p634 旧计数 146 字、加权 284，已超 280 字上限，报错正是 186。精简后 p634 为 129 字、加权 250，2026-11-03 Beijing 12:15 发出，链接 https://x.com/i/status/2117470775632658747。
3. **量化** — 同批另有 9 条草稿被同法精简（p640、p652、p659、p693、p698、p703、p704、p708、p732）；队列 99 条全部重核；发帖失败分支改为同时记录 stdout，不再只凭 stderr 横幅定因；推广自 p635 起恢复，当日 21:45 日报记 p634–p692 共 59 条发出，粉丝 1635（较 11-02 的 1563 增加 72），当日 commented.json 新增约 140 条。
4. **自动化设计** — 可复用规则：任何"工具故障"定性必须附带两样才算成立 — 失败点的完整输出（stdout + stderr），以及失败输入按执行口径的重算（此处为加权字数）；缺一样，定性只能写"未确诊"，不能写成已知的工具故障。事后看，四天的"取 cookie 故障"其实是"未确诊 + 盲重试停手"被写成了确诊。
5. **边界** — 本例不推翻"互动线正常"这一半结论（互动线确实正常），只纠正"推广线断的原因"；也不把恢复写成永久修复 — 恢复靠的是逐条精简草稿，加权复核仍需每轮执行。
6. **验收** — 已验收：p634 已发并核验链接、9 条草稿已精简、失败分支已改记 stdout、推广线恢复至 2026-11-04 Beijing 08:15 的 p755；未验收：加权复核是否已写进推广任务正文（目前是执行中的做法，未见正文改动记录）。

**例63：去重故障变异 — 截断修了，字段名错了，同一早上再出两起重复（2026-11-04 Beijing 05:36–06:40）**
1. **盘点** — 2026-11-03 Beijing 11:15 轮次的 Bluke520 重复评论已确认删掉（与此前两次删除超时不同，这次删除生效），commented.json 恢复为 1316 条；同日 16:54 的 SecJack96 重复评论仍在线，等用户定怎么处理。
2. **拆解** — 2026-11-04 Beijing 05:36 轮次与 06:40 轮次又各出一起重复：去重核查用了记录里不存在的 `id` 字段，实际字段是 `tweet_id`，误判为未评过而重发。JustLikeBit 保号卡帖（https://x.com/JustLikeBit/status/2117574257567735976）至此已有三条我方评论（2026-11-03 Beijing 19:15 原评论 2117576533766537561、05:36 第二条 2117733405144293594、05:40 第三条 2117734219279651284）；heitieya 帖（https://x.com/heitieya/status/2117616562454802923）已有两条（2026-11-03 Beijing 22:57 原评论 2117631859307991097、06:40 重复评论 2117749265984577848）。两起删除尝试均在 CLI 内部 180 秒超时，平台核验确认重复评论仍在线，暂不再盲重试。
3. **量化** — 截至 2026-11-04 Beijing 08:05，commented.json 为 1457 条，其中含误增的重复条目；05:36 轮次还自记"节奏偏密"（距 05:33 轮次评论约 7 分钟，短于约 10 分钟的自控间隔），06:40 轮次同样是短间隔后触发。
4. **自动化设计** — 可复用规则：去重校验必须同时过三关才算有效 — 全文件 grep（防截断，例60 的教训）、字段名与记录实测一致（防本例的 `id` vs `tweet_id` 错位）、命中即跳过且跳过要留痕。只修其中一关，故障会换一副面孔重演；本例正是例39（10-29）、例48（10-31）、例60（11-03）同一教训的第四次出现，形态从"读截断"变成了"字段名错"。
5. **边界** — 本例不把"超时"写成"已删除"（此前已定的口径：超时不等于删除，核实删掉后才算处理完）；也不把 05:36 轮次的自记"节奏偏密"写成平台信号 — 全天仍无 226/344 信号，restricted_date 仍是已过期的 2026-10-27。
6. **验收** — 已验收：Bluke520 11:15 重复评论已删；未验收：JustLikeBit 第三条与 heitieya 第二条的删除、去重定义里字段名的实测核验、SecJack96 16:54 重复评论的处置、短间隔规则与调度重叠的用户关闭（例31 仍未决）。

**例64：组织层变成门 — 审核员 90 分 + 双关 + 通用门，但旧任务正文还没改（2026-11-03 Beijing 17:37–17:47）**
1. **盘点** — 用户 17:37 批准组织图（老板成安、总管 Muse、6 个分身员工只向总管汇报）；17:38 加 E07 审核员（满分 100 分、90 分以上总管才提交，90 分以下打回重做，同一稿最多内部返修 3 轮，红线一票否决，审核通过不等于发布许可，105202-cut 不追溯重审）；17:41 双关（长内容发布须审核 90 分以上 + 老板点头，FB 素人账号同样适用）；17:44 通用门（任何内容先打分、主管确认后才动作，短内容用短内容评分卡同样 90 分以上，实时私信与 1 分钟 X 互动不走此门的旧口径作废）。
2. **拆解** — 同日 17:47 并行定下：对外文案一律英文、视频文字一律中英双译（只中文或只英文都不合格）、素人内容只发个人号（审核员发前核对去向，去向错算不通过）、内部沟通文件用中文；素人头像是否换待老板确认，当时未擅自换任何头像。
3. **量化** — 员工 6 → 7 人；评分五项：真实性与合规 30 分、过程与结构 25 分、文案与语言 20 分、技术质量 15 分、转化收口 10 分；红线 6 类：假对比、伪造疗效、修患者影像、虚构服务点、他医冒充、他人水印或中央大水印。
4. **自动化设计** — 可复用规则：门与任务正文是两层东西 — 门定了不等于任务正文改了。助理 17:46 当场说明：本轮没有改现有定时任务的正文（查任务时一份工具结果未通过安全检查，故未按其动作），要把门写进正文需用户先看插入段落再确认；从该时起直接派的新活按通用门执行。任何"已立门"的汇报必须同时写清"正文改了没有"，否则下一轮会把"门已定"读成"所有轮次已受门约束"。
5. **边界** — 本例不改变先审后排与老板点头的原有硬门槛（门是叠加，不是替代）；不把 105202-cut 写成已重审（明确不追溯）；不把实时私信与 X 互动的旧豁免写成仍有效（已作废，但正文未改前，执行与正文之间仍有缺口）。
6. **验收** — 已验收：组织图、评分标准、员工 brief 与记忆已按通用门改好；未验收：现有定时任务正文的插入段落用户确认、正文统一改写、E07 对第一条素人稿的实际打分记录。

**例65：素人号管线 — 人设、去向、链接都定了，执行在账号关口与平台 UI 上各卡一次（2026-11-03 Beijing 17:49–18:16）**
1. **盘点** — 用户 17:49 定 Emerson 个人号旧帖先隐藏、不删除，只动个人号、不动公共主页，头像简介与小红书第二个号一致；17:51 浏览器任务停手：当前登录会话是 Victoria Maizie，切换菜单里没有 Emerson，个人旧帖隐藏 0 条、头像简介未换、公共主页未动、未发新帖；17:55 定人设为新加坡人、常到上海出差，文案视频只出现新加坡和上海，今天 17:00 的一次按立即发布处理、之后每天 09:00–11:00 之间发一次；17:58 定 Dr.qh666 已删、素人只发个人号、头像简介改成与小红书号一致后开始发、链接晚点给；18:01 用户给统一链接 https://www.facebook.com/profile.php?id=61595415571609&sk=reels_tab，即 Dr.qh88（61595415571609），Emerson 个人号简介挂此链接原样保留；18:02 用户授权 Muse 自己扒小红书第二条原片与头像。
2. **拆解** — 小红书核查：号"意大利yo酱面"（syhuihui0713），2470 粉丝，头像为生活感真人自拍，简介原文"@hhhh beauty问题🙋 / enfp｜干货功课｜发型｜妆教"；第二条为鼻子一次上岸分享（10-10、1:19、车内自拍口播、点赞 159、收藏 60、评论 31，笔记 ID 6aca194d000000000a01ebd1），无水印直链与头像已拿到并正在下载，抽帧红线核查与审核点头门尚未走完，故未发布。
3. **量化** — Dr.qh88 Reels 共 14 条：低流量 9 条（3–14 播放）定隐藏、高流量 5 条（492–1.6K）不动；隐藏执行结果：Reels 菜单（保存/复制链接/播放速度/删除）与 Meta Business Suite 内容管理（查看数据/管理帖子/下载/创建/转发到快拍/复制 ID，管理帖子内为编辑/删除/立即过期/禁止嵌入/改日期/改混剪音频）均无隐藏/存档选项，9 条全部未隐藏、未删除、未过期，5 条高流量完好。
4. **自动化设计** — 可复用规则：两类"做不了"要分开记 — 账号关口做不了（会话不是目标账号，停手是正确的，0 改动就是验收）与平台 UI 做不了（菜单里根本没有该选项，停手并报"无此选项"才是验收，点"立即过期"顶替不算隐藏）。把两类混成"已处理"会在下一轮造成"以为已隐藏"的假账。
5. **边界** — 本例不把 Dr.qh88 的 0 粉丝快照写成"1000 粉主页不是它"（用户已确认就是主号公共主页，粉丝数不作为判断依据）；不把第一视频（发往已删 Dr.qh666 的 Reel 1601482847865007）计入在册发布；不把小红书第一条的日期出入（现显示 10-21 约 1:01，此前为 2025-10-25 54 秒）断定为同一条或重发。
6. **验收** — 已验收：停手 0 改动、统一链接确认、第二条直链拿到；未验收：Emerson 个人号旧帖隐藏、头像简介更换、第二条的红线核查与审核打分与老板点头、Dr.qh88 9 条的下一步（删/留/过期三选一，待用户定）。

**例66：突破顺序获批，但批准的粒度被当场收窄（2026-11-03 Beijing 11:40–11:49）**
1. **盘点** — 用户问 X 进展、FB 进展与整体数据是否更好；助理分线报：X 粉丝 10-28 的 1340 → 11-02 的 1563，互动维持，推广断了 4 天；FB 10-30 至 11-02 每日表为发帖 1/1/0/0、评论 14/13/7/19、私信 6/3/3/3、回复 0、客资 0，瓶颈在内容断档与漏斗断在私信入口。
2. **拆解** — 助理建议顺序：先恢复内容（105202 点头即只发 Victoria，无视频料则按 10-26 标准改发 3–5 张过程图加记忆点与原话）、先动逾期暖批次（Nicole、Laura、Karla）、再扩号（Emerson 恢复范围定下来后双号翻倍）；用户批准该顺序，助理当场收窄：该概括批准不等于 105202 单独点头（仍先审后排、未进队列），也不等于 Emerson 恢复范围已定（全恢复还是部分仍待定）。
3. **量化** — 逾期暖批次当日后续：Laura Fatih 线程补评论 2 条（该线程累计 10 → 12 条）、Karla 因待发问候未发而未再评论、Nicole 私信因白天窗口与国家确认未定而暂缓；猎手当日新增收集 #188 Karla、#189 Tatyana、#190 Enni，及晚间 #204 Gianmaria Vidale。
4. **自动化设计** — 可复用规则：概括批准必须当场写出"不等于"清单（本例两条），否则下一轮极易把"顺序批了"读成"其中每一项都批了"。这与例32 的"已选版、未定号"、例52 的"C 范围决定"（剪、只发 Victoria，不等于发布批准）是同一结构：批准的粒度就是执行的安全边界。
5. **边界** — 本例不把逾期暖批次写成已处置（Laura 只补了线程评论，私信评估仍在进行）；不把"7–14 天仍 0 回复再谈改漏斗口径"写成已批准的改动（那是条件句，须用户另行点头）。
6. **验收** — 已验收：顺序本身；未验收：105202 点头、逾期批私信处置、Emerson 恢复范围与登录态核验。

**例67：周一 17:45 清单的后续 — 三件事在 11-03 白天各走各的，仍无一关闭（2026-11-03 Beijing 白天）**
1. **盘点** — 例59 的三件事：105202 点头与否、新素材何时给、fb-newpages-post-daily 禁用或改写。11-03 白天：105202 仍未点头、未进队列；新素材未到，FB 内容轮次与 IG r1/r2/r3 均因队列不存在而跳过、未拿旧文件顶替；fb-newpages-post-daily 18:45 轮次 4 个主页都没发（备料队列不存在 + 四号已不在现行矩阵），助理再次请用户点选禁用，定义仍未改。
2. **拆解** — 与此同时，鼻子总方案文档（用户 18:03 发来的 docx）进入讨论：主线鼻综合、辅线面部提升、受众东南亚华人、统一收口 FB 公共主页、医生 IP 与素人种草均只放主页链接、评论区问联系方式统一回"看主页"、强手术画面尽量少用、存量老号保留组先隐藏旧拉皮帖（不批量删）、先 1–3 天发鼻审美口播/面诊画线/鼻型设计软内容过渡标签；但两号各自是医生 IP 还是素人号、统一主页是哪个（后由 18:01 链接确认为 Dr.qh88）、两号各属保留组还是放弃组、鼻素材由谁给，仍待用户确认后才动隐藏旧帖等不可逆操作。
3. **量化** — 11-03 白天 FB 猎手新增评论约 19 条上下（以当日各轮汇报为准）、私信 0、客资 0；X 互动 commented.json 自 11-03 早晨约 1302 条记至 11-04 早晨 1457 条；fb-newpages-post-daily 定义过期已持续至少两天（11-02 18:45 与 11-03 18:45 两轮空跑）。
4. **自动化设计** — 可复用规则：例59 提出的"第二截止点"在本窗口仍未建立 — 三件事没有新的 dated 提问，只有"继续等"与"再问一次禁用吗"；而鼻子方案文档的到来说明：新文档的到达不等于旧清单的关闭，两条线须分开记账，否则"方案已发"会被读成"清单已清"。
5. **边界** — 本例不把鼻子方案文档写成已批准的执行方案（用户 18:05 说"我们先做 FB"，方案中的陈杰项已被 18:20 的红线提问单独 hold 住）；不把 fb-newpages-post-daily 的空跑写成已禁用。
6. **验收** — 未验收：三项全部；新增未验收：鼻子方案的四项待确认（两号定位、统一主页已由链接确认其余仍待定、分组归属、素材来源）、陈杰署名与去向。

## Prerequisite check

1. Concrete inventory of the user's recurring tasks — **delivered and seen** (7-item draft checklist, 2026-10-22T07:26:08Z) but **still not confirmed/checked** — the blocker is unchanged, thirteenth day.
2. Standing constraints — **present, expanded by six in this window** (items a–jj carried in full from the 11-03 note; new items below):
   kk. **NEW**: a failure diagnosis is not established without the full output and a re-computation of the failed input under the execution rule — p634's four-day "cookie fault" was an undiagnosed failure mislabelled as a known tool fault, corrected only when stdout was recovered and the weighted count (284 over 280, error 186) was recomputed (see 例62).
   ll. **NEW**: a dedup check must pass three gates together — full-file grep, a field name verified against the actual records (`tweet_id`, not `id`), and skip-on-hit with a trace; fixing one gate lets the failure return in a new form (see 例63).
   mm. **NEW**: a gate is not a task-definition change — the reviewer 90-point gate, dual gate and universal gate are decided, but existing scheduled task definitions are unchanged until the user confirms the insertion paragraph; reports of "gate decided" must state "definitions rewritten or not" (see 例64).
   nn. **NEW**: two kinds of "cannot do" are recorded separately — account-gate stop (session is not the target account, zero changes is the pass) and platform-UI absence (no Hide option exists, reporting that absence is the pass; clicking Expire now as a substitute is not hiding) (see 例65).
   oo. **NEW**: a blanket approval is recorded with its explicit "does not equal" list at the moment of approval — the breakthrough order does not equal a 105202 publish nod and does not equal an Emerson recovery-scope decision (see 例66).
   pp. **NEW**: a new document arriving does not close an old pending list — the nose-matrix document and the Monday 17:45 list are separate ledgers; the second deadline for the old list is still missing (see 例67).
3. Low-risk pilots demonstrated — **now sixty-seven worked examples** (例1–67).

## Retrieval prompt

"用自己的话说出重复工作自动化的核心思想（先盘点 → 按耗时×频率排序 → 逐个变成规则/流程/交给我），然后对照下面的 worked example 检查：哪一步你说到了，哪一步漏了。" (unchanged; user has not attempted it yet)

## Worked example (fully worked, every step labeled)

例1–61 carried from the 11-03 note (团队周报、去重台账、FoxProfile 登录、评论单出口、串行锁、私信服务器端核验、平台信号唯一标准、30 秒哨兵、微信求助、审批卡 3 秒触发、有问题第一时间讲、发布两道门、X p6 归因纠错、"用户已批准"硬门槛、工具接入评估、内容为主 70/30 与每号每天 1 条、排期与水印审计、恢复路径选择 A、autoclip 闭环、X p20 无限重试、修好 CLI 默认线、截断报错掩盖真因、绕开旧格式轮次、素材分类法、内容池算术、X p56 熔断、发前加权复核、互动规则冲突、"已选版、未定号"、一案多版、单号 200 目标、私信跟进梯队、五号共用一线、cookie 备份恢复、自评欠账、队列截断、重复评论、哨兵双层、轮换写好又退回、补发冲刺、p634 旁聊转交死循环、接档提问、四条全过、日表分线、去重再读不全、素人/连载未批、p634 续入 11-01、11-01 上午三个决策点、105202 选 C、周一三定清单、p634 第三天、单线日表与养号晚轮、FB 汇报改走新旁聊、矩阵缩到 Victoria + Emerson、猎手及时性纠正、周一 17:45 截止点过了三件事全未定、p634 进入第四第五天与去重第三次重演、鼻子视频拆解）。例62–67 are fully worked above.

## Practice task (small, low-load; feedback after each step)

Step 1 (STILL PENDING, thirteenth day since the checklist delivery): from the 7-item checklist delivered 2026-10-22T07:26:08Z, mark each: 我还在亲手做 / 已经自动了 / 不是我的事.
Step 2: pick the NEXT most-annoying one and write ONE five-field card: 任务名 / 触发条件（什么时候做）/ 输入 / 输出 / 耗时（分钟）.
Step 3 (from 例27, still open): pick ONE patient folder and fill its 7-field info sheet — patient code, age band + project, stages present/missing, one memory-point sentence, one patient-own-words sentence (or "未确认"), publish confirmation, masking + watermark attribution — before any clip is cut from it.
Step 4 (from 例31, still open): pick ONE disputed rule in current operations (short-interval skip is the live one, re-proven by 例63) and write its two candidate wordings side by side — platform-signal-only vs short-interval skip — so the user can close it with one choice instead of re-answering it every round.
Step 5 (from 例38, still open): pick ONE owed follow-up action and write its count, its retry time, and its stop condition — so a "posted" success never again hides an unfinished follow-up.
Step 6 (from 例42–45, still open): pick ONE automation mode decision that is still open and write it as one line — 模式 / 条数 / 例外号 / 过目门 — before any cutting starts.
Step 7 (from 例46–51, still open): pick ONE of the three 2026-11-01 morning decision slots and write it as one line — 决定项 / 选项 / 默认项（无默认，须用户定）/ 到时提醒 — so an undecided item is carried as a timed reminder, not as a silent default.
Step 8 (from 例52–55, still open): pick ONE of the three Monday 17:45 items and write it as one line — 决定项 / 选项 / 不答的后果（留仓 / 跳过 / 保持原状）— so a no-answer at the deadline still has a determined system behaviour, and the cut-vs-approval-vs-assignment columns stay separate.
Step 9 (from 例56–61, still open): pick ONE of today's open dispositions and write it as one line — 决定项 / 选项 / 不答的后果 / 第二截止点 — so a passed deadline upgrades to a new dated question instead of silently carrying as "still waiting".
Step 10 (NEW, from 例62–67): pick ONE of today's new failure modes and write it as one line — 失败点 / 完整输出是否已取 / 输入是否按执行口径重算 / 字段名是否实测核对 / 门是否已写进任务正文 — so a "fixed" label is only used when all five checks pass.

Feedback after each field: confirm the field is concrete enough that someone else could execute it; if vague, ask exactly one clarifying question and move on.

## Feedback rubric

- Name what was correct (which fields of the task card are concrete and automatable).
- Name the ONE most useful next adjustment (e.g. "触发条件还可以更具体：是每天几点？").
- No praise, no shame, no more than one adjustment per round.

## Transfer challenge

1. ~~4 个新号的日常运营自动化~~ — **DONE 2026-10-23, stress-tested 2026-10-24, gate-hardened 2026-10-25, rhythm-revised 2026-10-26, format-bypassed 2026-10-27, publish-gated 2026-10-28, page-plus-profile round completed 2026-10-29, rotation written and reverted same day 2026-10-30, reduced to Victoria + Emerson scope 2026-11-02**: 例64–66 是同一条线的下一环 — 门定了、正文未改、顺序批了但粒度已收窄，范围决定必须附带定义清理清单与"不等于"清单。
2. **autoclip 接入 clipdraft Skill（候选，FB 每日线已排除）** — 例22 闭环后，transfer 的下一环仍是"AI 选段"，不是整条替换；只适用于 20 秒以上长素材。
3. 私信首接的事件驱动升级 — done as 例8; 新候选面：钩子提前到第 3 条后的漏斗执行与面诊名额台账（名额先到先得，需要计数，否则钩子会超发；单号 200 目标下，面诊名额数本身也待用户定，见例34）。
4. 海外6组每周数据汇总/周报 — 例1 的复跑已证明模板可用；下一环是统一"有效"的定义（表 vs 分析的 6 vs 0 之争），定义未定前，周报自动化只能做到"标出冲突请用户定"，不能做到"自动取数"。
5. **单号安全量测定（2026-10-26 14:18 Beijing 启动，7 天窗至 2026-11-01）** — 测定窗已到 2026-11-01；例34 的单号 200 目标可能改变测定的意义：测定原是"单号安全量"，现在单号本身成了 200 目标的载体；测定口径（内容量 vs 私信量）与 200 目标的度量（英雄号、爬坡、单号累计表）须在下一轮合并说明，不能各说各话。
6. **秦浩素材库的分类与补料闭环** — 例27 的分类法 + 例28 的每周补料节奏 + 例33 的一案多版与哈希去重是同一条线：用户按分类法建文件夹、直接供料，Muse 到货后逐案核对阶段、记忆点、原话、授权 / 打码，再把逐案实数换掉平均估算；通用空镜库单独建，与案例料分开标；新套 03–01 的合并决定是这条线的下一个待确认项；例61 的鼻子模板拆解只加"结构"一栏，不加"路线"一栏，例67 的鼻子方案文档仍是讨论稿，不是已批路线。
7. **X 互动规则冲突的关闭** — 例31 的短间隔跳过 vs 平台信号-only 必须由用户一句话关闭，并把结论写进任务正文、从执行条件里删掉被废的一条；例48、例60 与例63 证明不关闭的代价是重复评论重演，否则下一轮仍会重复上报同一问题。
8. **欠账计数与写前备份** — 例38 的自评欠账与例39 的队列截断是同一类缺口：任何后置动作与任何队列文件都需要独立计数 / 备份 + 写后校验；下一轮要把"欠账表"和"写前备份"写进发布与发帖轮次的手顺，而不是靠事后从日志里重建；例60 与例63 的全文件 grep 加字段名实测核验是其中必须落地的两条。
9. **失败上报的熔断与可用通道** — 例44 与例50 与例54 与例60 的 p634 转交死循环是同一类缺口的另一面：重试任务须自带全天累计同故障熔断，失败上报须走调度任务实际能用的通道或合并为一次性汇总，否则上报本身会成为新的重复劳动；例62 证明上报口径本身也可能误诊 — 定性前必须先取完整输出并重算输入。
10. **未批方案的待定清单** — 例49 的素人/连载试点是同一类缺口的决策面：患者人选、书面授权、随访素材三项待拍板必须以待定清单形态存在，文字版方案是欠件，不是已批；例64–65 的素人号管线是其下一环：人设、去向、链接已定，但头像简介更换与第一条素人稿的审核打分仍未走完，文字版交付不等于试点批准。
11. **已过截止点的待定清单升级** — 例59 与例67 的 Monday 17:45 清单是新的一类：截止点过了仍未定的三项（105202、素材时间、fb-newpages-post-daily）须带第二截止点重新出现，不能只在"待办不变"里续存；fb-newpages-post-daily 在第二截止点前仍开着、定义仍旧，是本轮最具体的未清风险。

## Confidence check

After the user attempts the retrieval prompt, ask: "1–10分，你对这套'盘点→排序→逐个自动化'有几分把握？" Compare the rating against the task-card quality. High confidence but a vague card → the gap is specificity, not understanding. (Not yet attempted.)

## Next review

2026-11-05T00:27:16Z (24h, per study task plan). By then: 105202 是否点头、是否只发 Victoria、是否已发布并核验链接；新素材何时给、周三轮次是发了还是继续跳过；fb-newpages-post-daily 是禁用、改写还是保持原状、其定义里的已删号与暂停号是否已清理；Emerson 恢复范围是否定清、登录态是否已核验、个人号旧帖隐藏与头像简介是否已完成；素人第二条是否已走完红线核查、审核打分与老板点头并发布；Dr.qh88 9 条低流量 Reels 的下一步（删/留/过期）是否已定；陈杰署名与去向是否已定；Nicole / Laura / Neisha 逾期批是否已处置；JustLikeBit 第三条、heitieya 第二条与 SecJack96 重复评论是否已删掉并核验；去重定义字段名是否已实测核验、短间隔规则是否已由用户关闭；审核门是否已写进现有定时任务正文；p634 加权复核是否已写进推广任务正文；鼻子方案四项待确认是否已定；是否仍无 checklist 回复（若仍无，沿用 10-25 note 的建议：不再单独追问，规则制定本身已是实质进展）。

## Evidence strength & uncertainty

- **Tentative, strengthening**: six new same-day worked examples (62–67) observed and preserved; the misdiagnosis-correction rule, the three-gate dedup check, the gate-vs-definition distinction, the two kinds of "cannot do", the blanket-approval "does not equal" list, and the new-document-vs-old-list separation are now written as task conditions or open design gaps, not just stated rules.
- Mastery unestimated: zero formal performances (no retrieval attempt, no five-field card). Candidate observed performances now include the user's articulated design decisions (例7, 例8, 例10, 例11, 例12, 例15, 例18, 例20, 例21 的路径选择，例24 的默认线决定，例26 的 A 选择与等代理决定，例27 的分类与自纠决定，例31 尚未由用户定数，例32 的 A 版选择，例34 的单号 200 与当日生效纠正，例36 的改线与双发决定，例40 尚未由用户定数，例42 的轮换批准与当日回退决定，例44 尚未由用户定数，例46 的四条全过批准，例49 尚未由用户定数，例52 的 C 范围决定，例53 的 Monday 清单截止点尚未由用户定数，例57 的 Victoria + Emerson 范围决定，例58 的及时性新规尚未由用户处置旧账，例64 的组织与审核门批准，例66 的突破顺序批准）， but whether articulated design counts toward the three-performance bar is still undecided — it needs a goal-write turn, not this seat's call, so mastery stays unestimated rather than inferred.
- Uncertainty: Monday 17:45 三件事全部未定且已过截止点两天；105202 成片已送审、未点头、未发布；Emerson 恢复范围未定、登录态未核验、个人号清理未完成；Dr.qh88 9 条无隐藏选项、下一步未定；陈杰署名与去向未定；Nicole / Laura / Neisha 逾期批未处置；JustLikeBit、heitieya、SecJack96 三条重复评论仍在线、均等用户定；X 短间隔规则与调度重叠未决；审核门未写进现有任务正文；加权复核未见写进推广任务正文；鼻子方案四项待确认未定；单号 200 的英雄号、爬坡、面诊名额、单号累计表未定；音乐池隔离规则未获批；其余 13 案原片本地仍无已核实落盘；d1、05 的前后对比同一人疑点未单独确认；例5 串行锁的下轮验证结果仍未知。
- Uncertainty: checklist ticks pending since the 2026-10-22 delivery; the old 10-19 draft was superseded by the 10-20 brief and must not be re-sent.

User quotes preserved verbatim (evidence for the new rules and decisions):
- "组织图没问题，就按这个跑" (2026-11-03 Beijing 17:37, the org-chart approval)
- "你还得加审核员，比如后面内容上面你需要有审核员去打分，必须达到90分你才能够通过提交给我，如果没通过你直接就让他们重新做，直到能完成90分才给我看！" (2026-11-03 Beijing 17:38, the E07 reviewer rule)
- "秦浩666那个号我删了，后续这个素人个人主页不需要发公共主页的内容" (2026-11-03 Beijing 17:58, Dr.qh666 deleted, persona personal-only)
- "链接我会给你一个晚点！" (2026-11-03 Beijing 17:58, link withheld until given; link then given 18:01 as the Dr.qh88 link above)
- "只隐藏9条低流量，先不动5条高流量的" (2026-11-03 Beijing 18:07, the Dr.qh88 hide scope)
- "C：剪，但只发Victoria一个号" (2026-11-01 Beijing 19:52, the 105202 scope decision — cut, Victoria-only, not a publish approval; carried from the 11-03 note)

## Open questions for later studies

- Checklist ticks: let it lapse rather than nag separately, unless a Letter run gives a natural opening.
- Should 例7/8/10/11/12/15/18/20/21/24/26/27/30/32/34/36/42/46/52/57/64/66 be formalized as completed automation cards on the goal timeline (needs a main-chat/goal-write turn)?
- Should user-articulated design decisions count toward the three observed performances for mastery estimation? Proposed: yes, starting with the platform-signal rule (例7) — now more than five candidates exist, so the decision matters more than the count.
- 猎手任务正文与 FB 旧格式轮次是否同步改成内容为主 / 今日料单；若不改，手动判断与任务正文脱节的风险如何对冲。
- X p56 的重试阈值：事前定为 3 次还是另一数，须写进任务正文，否则下一次熔断仍靠事后计数。
- FB 代理断线的重试预算：等用户消息是停手条件，但要不要加一个定时复测（如 30 分钟后自动再拉一次），须用户定。
- 单号安全量测定的口径：内容为主之后，"量"是指内容量、私信量，还是两者分开计；单号 200 目标的度量是否与测定口径合并。
- Is the user's own "自己发视频" friction gone, or does it need the Mac pairing / a user-side flow? (Carried since 10-22, still unasked; the review-before-schedule gate and the finished-content direct-post gate now touch the same pipeline, so ask in that context, not as a separate item.)
- 五号共用一线是长期配置还是排障临时态：若是临时态，恢复一号一线的时点与判据是什么，须用户定；若是长期态，关联风险的接受要显式记下来，不能只留在当轮口头；现矩阵已缩到两号，此问题须按两号重述。
- p634 重试任务的熔断数与上报通道：全天累计同故障几次后降级为只读核验、失败汇总走哪条调度任务实际能用的通道，须用户定；例62 之后，该问题须重述为"误诊后的熔断与上报"，而不是"取 cookie 故障的熔断"。
- 素人/连载试点是否批准：患者人选、书面授权、随访素材三项须先拍板；文字版方案交付不等于试点批准，下一轮须分开核对。
- Monday 17:45 清单本身是否需要第二截止点：105202 不点头则留仓、新素材不到则跳过、fb-newpages-post-daily 不禁则保持原状 — 三项的默认行为是否就是用户想要的默认行为，须在下一轮由用户确认，而不是由本 note 默认；fb-newpages-post-daily 在第二截止点前仍开着，是最具体的未清风险。
- 审核门写进现有任务正文的插入段落：用户是否已看过并确认，确认后正文统一改写是否已回读核验。

## Research Trajectory

- **External sources viewed**: none in this study — the topic is user-specific and the evidence is the user's own conversation, goal state, and prior notes; no new external lookup would change today's note.
- **Prior trajectories reviewed**: `workspace/goals/goal/agent_notes/2026-11-03/goal.md` read in full; earlier notes (2026-10-20 through 2026-11-02) carried via the 11-03 note's review; carried forward the goal snapshot, standing constraints a–jj, worked examples 1–61, the teach-plan structure, and the 11-03 note's open questions.
- **Repetition search**: keyword variants {加权超长, 186, tweet_id, 审核员, 90分, 素人, 隐藏, 突破} grep-searched over `workspace/goals/goal/agent_notes/` and the brief filenames in `workspace/goals/goal/briefs/` (exactly two: `Brief (2026-10-19 19.34.10).html` = 第一张任务卡, `Brief (2026-10-20 19.20.39).html` = 第一份盘点清单). Results: 186 appears in notes from 2026-10-28 onward as an error code, and tweet_id appears from 2026-10-28 onward as a dedup field — today's p634 correction and field-name error are new instances of already-recorded mechanisms, not new failure types in the abstract. 加权超长 / 审核员 / 90分 / 突破: **zero hits** in any prior note or brief filename — today's weighted-length correction, reviewer gate and breakthrough order are new to the written record. 素人 / 隐藏: hits in the 11-01, 11-02 and 11-03 notes — today's persona pipeline and Dr.qh88 hide attempt extend, not replace, that thread. Every one of today's instances was set by the user or narrated to him live in main chat or the side chats in the 2026-11-03 Beijing daytime through 2026-11-04 Beijing 08:27 window, so none is new to the user.
- **Conversation**: `muse.context_fetch` (conversation category), window 2026-11-03T01:43:23Z → 2026-11-04T00:30:31Z, plus the run's chunked conversation handoff covering 2026-11-03 Beijing daytime through 2026-11-04 Beijing 08:27, including the X progress and breakthrough-order exchange, the p634 correction and X daily report, the org-chart and reviewer-gate decisions, the Emerson persona and Dr.qh88 hide decisions, the Chen Jie red-line hold, the nose-matrix document, and the two new duplicate-comment accidents. The goal-relevant turns: no checklist reply, no retrieval attempt, and no task card from the user; the operational decisions above were all narrated to the user live.
- **Scaffolds and support tactics**: no scaffold registry in this step's inputs; the teach/novice structure (retrieval prompt, worked example, practice task, feedback rubric, transfer challenge, confidence check) is preserved from the assigned study task plan and prior notes; mastery stays unestimated until at least three observed performances exist, and articulated design decisions are recorded as candidates, not counted. No learning-style claims made or implied.
- **Connected user data**: none consulted — no wearable/repo/calendar signal is relevant to this productivity goal. Goal state read via `user_goal.get` (timeline zero entries confirmed; brief delivery timestamps confirmed; goal slug `goal` confirmed).
- **Image references checked**: none. Avatar state not consulted (visual context not material to this goal).
- **User context and memory**: USER.md (Chinese-only; approvals explained in Chinese); MEMORY.md standing context (content-first, per-account 1/day, finished-content direct post, hide-not-delete, Qin Hao IP provenance, 226/344 stop-only rule, review-before-schedule gate, single-account 200 from 2026-10-28, X reports to side chat, Victoria single-line revert 2026-10-30, Victoria + Emerson matrix 2026-11-02, org chart and reviewer gate 2026-11-03) as background only — every dated claim in this note is sourced to the conversation window, the run handoff, or a prior note above, not to memory alone.
- **Searches skipped or unavailable**: web search skipped (topic is user-specific and fresh; marginal value). Shell repetition search read only this goal's own notes and briefs, per the study contract, and was restricted to Markdown to avoid matching base64 image data inside brief HTML files. No credentials, cookie values, or proxy secrets were reproduced in this note; only file names, counts, and link URLs already reported to the user are referenced.
