# 工具链状态 — haze_lferrier（ig-02）

核查时间：2026-11-10 16:32–16:35（CST）。只读核查，未发任何评论/私信/帖子。

## 逐项结论

| 项目 | 结论 | 证据 / 卡点 |
|---|---|---|
| CLI 可用 | 通 | `/opt/hatch/bin/instagram-cli` 存在可执行 |
| CLI 登录态（本号） | **不通** | `instagram-cli accounts` 返回 `{"accounts":[]}`——本机未通过 Meta Accounts Center 链接任何 IG 账号，无本号的 `user_fbid`，无法区分会话 |
| 读主页/帖子 | **不通（CLI）** | 所有读命令（`profile`/`posts`/`user-profile`/`fetch-post-comments`/`account-search`）都强制要求 `--account-id`，无账号则无法调用 |
| 搜同行帖子 | **通（公开发现层，不经本号登录）** | `social.search`（platform=instagram，rhinoplasty / facelift 查询）返回 IG reels 与同行账号结果；但它只做发现，不能代本号读评论区、不能发评论 |
| 评论功能 | **不通（CLI 设计上就不支持）** | 连接器文档明确：`instagram-cli` 不能创建顶层评论，只能在自家帖子上 `comment-reply` 回复已有评论；同行帖子评论区发评论只能走浏览器（FoxProfile ig-02 环境） |
| 私信收发 | **不通（CLI）** | `instagram-messages-cli accounts` 同样返回 `{"accounts":[]}`；`inbox`/`send` 都需已链接账号的 `--account-id`。DM 连接器与内容连接器是两套独立授权，都未接 |
| FoxProfile 环境 | 存在，未运行 | `127.0.0.1:8000/api/v1/profiles` 查到 `ig-02`，`is_running: False`；服务本身正常。登录态需浏览器核查（本任务无浏览器权限，未启动环境、未验证） |

## 修复路径（二选一）
1. **接 CLI（推荐用于读 + 回复自家评论 + 私信）**：在 Meta Accounts Center 链接本号。内容侧链接：https://agent.meta.ai/foa_ac_link/instagram ；私信侧链接：https://agent.meta.ai/connect/instagram_messages 。接通后 `accounts` 应返回本号 `user_fbid`，再逐项复核。
2. **走浏览器（评论同行帖子唯一路径）**：由有浏览器权限的代理启动 ig-02 环境核查登录态，评论/私信走浏览器操作；CLI 接通前不要用 CLI 发任何动作。

## 注意
- gaga5456（ig-03）不在本次范围，未动。
- 本文件不含任何凭据值。

## 2026-11-10 16:54 首轮私信盯守核查（ig-haze-dm-watch）
- **账号锁定**：浏览器打开 instagram.com/direct/inbox/ 后跳转至 auth_platform/challengepicker/，提示 "Choose a way to recover — We locked your account to protect you from a possible hack"，恢复方式为邮箱验证码（页面显示的两个邮箱均已打码），Continue 未点。按规则立即停工，未尝试登录、未发任何消息/评论。
- 后果：登录态、收件箱、Message requests、关注者基线（预期约 8 人）均未核实；三表（dm-threads / dedup / leads）仍全空；基线文件未建。
- 待用户在他自己指纹浏览器里过验证（静态 IP 相同），过完重导 cookie 导入；切勿在挑战页点 Continue（页面提示所选联系方式会替换全部现有登录与联系信息）。ig-02 环境未关闭，挑战页标签已保留。
