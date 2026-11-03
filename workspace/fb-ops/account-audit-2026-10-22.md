# FB 矩阵账号盘点报告 — 2026-10-22

- 盘点时间：2026-10-22 10:19–10:21（CST）
- 方式：只读盘点，未发帖、未评论、未改任何设置。
- 通道：facebook-cli（Victoria 会话，走 FB 静态代理）+ FoxProfile profiles 列表（仅列表，未启动新号浏览器）。
- 说明：标注"未读到"的均为本次工具实际返回失败/无该字段，不做推测；标注"历史记录"的数字来自 2026-10-21 接入/运营记录，非今日实测。

## 1. Victoria Maizie（个人号 61590577106578）— 主页 Dr.qh88

### 登录健康
- `facebook-cli me` 正常返回：Victoria Maizie，fb_user_id=61590577106578，与目标一致。CLI 会话健康。
- FoxProfile 环境 fb-victoria 存在（代理端口 20002），当前未运行（该号日常走 CLI+托管浏览器，不依赖此环境）。

### 个人号最近帖子（timeline 最新 10 条，还有更多未拉）
| 时间（CST） | 类型 | 内容 | 链接 |
|---|---|---|---|
| 2026-10-21 23:03 | Reel | V3 西语男修复旅程（Day 1→拆线） | https://facebook.com/reel/2567000590471792/ |
| 2026-10-21 19:50 | Reel | V2 Deep Sculpt 白人男前后对比 | https://facebook.com/reel/1123541476924976/ |
| 2026-10-21 17:47 | Reel | V1 黑人男全脸改造·术后1个月 | https://facebook.com/reel/1646748630341954/ |
| 2026-10-20 22:52 | Reel | Day 3 → Day 30 | https://facebook.com/reel/873312822537059/ |
| 2026-10-20 19:50 | Reel | Day 3 → Day 15 | https://facebook.com/reel/1591515982775545/ |
| 2026-10-20 15:53 | Reel | Day 30 男案例 | https://facebook.com/reel/1439061491530501/ |
| 2026-10-20 10:54 | 图文 | Natural lift / Dr. Qin Hao 介绍 | 见 timeline |
| 2026-10-20 09:39 | 文字 | 拉皮恢复期问答长帖 | 见下方异常 #1 |
| 2026-10-18 19:47 ×2 | 工作经历更新 | 非内容帖 | — |

### 个人号互动（抽样实测：10-21 三条 Reel + 10-20 Day3→30 Reel + 恢复期文字帖，共 5 条）
- 评论：全部 0（comments read 返回空）。
- 表情反应：全部 0（reactions read 返回空）。
- 可见性：抽样 4 条 Reel 均为 public（已核验）；文字帖为 private（见异常 #1）。

### 主页 Dr.qh88（profile 61595415571609）数据（account-insights，as_of 2026-10-22 10:19，窗口 2026-09-24 至 10-21，last_28d）
- 粉丝 follower_count：**0**
- views（窗口）：12（上一周期 0）
- unique_viewers（窗口）：2（上一周期 0）
- profile_visits（窗口）：4（上一周期 0）
- engagement_including_clicks（窗口）：0
- new_followers（窗口）：0；unfollowers：0

### 主页最近帖子（窗口内共 3 条，列表已拉完）
| 发布时间 | 可见性 | 播放 views（lifetime） | engagements | 点赞 | 评论 | 分享 |
|---|---|---|---|---|---|---|
| 2026-10-18 20:06 | Public | 3 | 0 | 0 | 0 | 0 |
| 2026-10-16 11:04 | Public | 0 | 0 | 0 | 0 | 0 |
| 2026-10-16 11:03 | Public | 0 | 0 | 0 | 0 | 0 |

- 帖子类型/文案：本次 Page posts 返回未带 caption/type 字段，**未读到**。
- 注意：10-20、10-21 的 6 条 Reel 都发在个人号上，主页 Dr.qh88 自 10-18 后没有新帖。

## 2. Fowler Ariana（FoxProfile 环境 fb-3651）— 主页 dr.qh（61595431556915）

- FoxProfile 环境 fb-3651：存在，代理端口 20003，当前未运行。
- 今日 CLI 实测（以 Victoria 会话读该主页）：
  - profile info → HTTP 403 "Profile Not Accessible"（仅本人/好友可读）；
  - timeline fetch → 同样失败。
  - 结论：**粉丝数、最近帖子、互动今日全部未读到**（CLI 通道读不了非本会话账号的主页对象）。
- 历史记录（2026-10-21，非今日实测）：cookie 直登成功；名下主页 dr.qh 存在；截至 2026-10-21 晚，该号尚未发布内容（Emerson 已先行试发成功，Fowler 待照同流程发）。

## 3. Emerson Ciara（FoxProfile 环境 fb-6399）— 主页 Dr.qh666（61595249439024）

- FoxProfile 环境 fb-6399：存在，代理端口 20004，当前未运行。
- 今日 CLI 实测（以 Victoria 会话读该主页）：
  - profile info → HTTP 403 "Profile Not Accessible"；timeline fetch → 失败。
  - 结论：**粉丝数、最近帖子、互动今日全部未读到**（同 Fowler，通道限制）。
- 历史记录（2026-10-21，非今日实测）：名下主页 Dr.qh666 接入时 0 粉；2026-10-21 晚经 FoxProfile 补丁路线试发 V1 成功并核验上线，Reel：https://www.facebook.com/reel/2298761260969935 。
- 今日追加核验：以 Victoria CLI `post read --url` 读该 Reel → **HTTP 404 Post Not Found**，从外部通道无法确认其当前可见性（见异常 #4）。

## 4. 新号（FoxProfile 环境 fb-51292，用户 ID 61590573251292）

- 按要求仅查 profiles 列表：环境 fb-51292 **存在**，代理端口 20005 已绑定，当前 **未运行**。
- 本次**未启动其浏览器、未触碰其登录**（接入验证由另一流程进行中）；账号身份、主页、数据本次一律未查。

## 汇总表

| 账号 | 环境/通道 | 主页 | 粉丝（今日实测） | 最近内容 | 互动概况 | 状态 |
|---|---|---|---|---|---|---|
| Victoria Maizie | CLI 会话正常；fb-victoria 环境存在 | Dr.qh88 | 0 | 个人号 10-21 连发 3 条 Reel（均 public）；主页最新帖停留在 10-18 | 抽样 5 帖评论 0、反应 0；主页 28 天 views 12、主页访问 4 | 有异常（见 #1、#2） |
| Fowler Ariana | fb-3651 存在（端口 20003） | dr.qh | 未读到（403） | 未读到；历史记录：尚未发帖 | 未读到 | 数据盲区（见 #3） |
| Emerson Ciara | fb-6399 存在（端口 20004） | Dr.qh666 | 未读到（403）；历史：接入时 0 粉 | 历史：10-21 晚发 V1 Reel；今日外部读取 404 | 未读到 | 数据盲区 + 可见性待核（见 #3、#4） |
| 新号 61590573251292 | fb-51292 存在（端口 20005，未运行） | 未查（按要求） | 未查 | 未查 | 未查 | 接入验证由另一流程进行中 |

## 异常清单

1. **Victoria 恢复期文字帖仍是私密**：2026-10-20 09:39 的拉皮恢复期问答长帖（post 122147272131352570），今日 `post read` 核验 visibility=**private**（verified），与 10-21 晚的状态一致，仍未公开；需用户在 FB App 内手动改 Public，CLI 侧改不了。
2. **Dr.qh88 主页 0 粉、数据近零**：粉丝 0；近 28 天 views 12、独立观众 2、主页访问 4；窗口内 3 条帖最高 views 仅 3，其余全 0。且 10-20/21 的 Reel 都发在个人号，主页自 10-18 起无新内容。
3. **Fowler / Emerson 数据盲区**：两号主页经 Victoria 的 CLI 会话读取均返回 403（仅本人/好友可读），粉丝、帖子、互动今日均未读到；要拿今日数据只能分别用两号自己的 FoxProfile 会话读（本次未启动两号浏览器做深读）。
4. **Emerson 首发 Reel 外部不可见待核**：10-21 晚核验上线的 V1 Reel（2298761260969935），今日以 Victoria CLI 读取返回 404 Post Not Found；不能据此断定已删除，也可能是对非好友会话不可见——需在 Emerson 本号会话内确认其状态。
5. **Victoria 个人号互动为零**：抽样 5 条帖（含 10-21 三条新 Reel）评论与反应均为 0，与此前多轮 lead-scan 结果一致；账号本身无受限提示，CLI 与发帖通道均正常。

*本报告所有"今日实测"数字均来自 2026-10-22 10:19–10:21 的工具实际输出；历史记录已逐项标注日期。*
