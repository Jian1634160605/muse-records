# AGENTS.md

Your operating manual for this workspace, written by you. Your main instructions cover how you work in general. This file is where you keep the specific, durable lessons and conventions you pick up as you work, the kind of thing you'd want a future session to know. It's not about the user (that goes in `USER.md` and your memory) or your personality (that's `SOUL.md`); it's about how you get work done here.

## Conventions
Add an entry whenever you work something out worth keeping, for example:
- a convention you've settled on ("keep data exports in `workspace/exports/` and clean them up monthly")
- a tool or site quirk worth remembering ("site X hides its form behind a cookie banner; dismiss it first")
- a workflow that worked, or a mistake not to repeat

It starts empty and is meant to grow slowly. Don't pad it; a short, accurate file beats a long, stale one.

- **浏览器活绝不派给子代理**（2026-10-22 实证）：子代理没有实时浏览器控制权限，browser.browse 必须由我本人直接派发；派 subagent 做只读复查会原样返工（它只能 CLI/文本抓取，浏览器部分交白卷）。
- **Bertie 绝不走 browser.browse（2026-11-10 实证）**：browser.browse 默认身份是 Victoria Maizie（默认浏览器 profile 的 FB 登录态），会把 Bertie 的活做到 Victoria 号上；Bertie 的浏览器操作必须走 `~/workspace/goals/x/hidden_files/bertie-fox.py`（FoxProfile API 直驱 fb-1030 环境），每次先核验好友页显示 Bertie Harmony 再动手。

## 站点经验
- **凭据绝不上终端输出（2026-10-22 实证）**：`~/.agent-reach/proxy-*.txt` 只用于 `export HTTPS_PROXY="$(cat ...)"` 形式，**绝不** `cat`/echo/head 打印到 stdout 检查连通性——输出会进日志与上下文。连通性用带代理的实际 API 调用验证。
- Instagram 网页版（桌面）无法编辑主页链接：编辑资料页的"网站"栏是禁用的，IG 原文提示"只能在移动设备上编辑你的链接"——与账号类型无关（专业号也一样）。加/改 IG 主页链接只能让用户在手机 IG App 里操作。IG 连接器（instagram-cli）也只能改简介文字、头像，不能改链接。christycrawford85 本身已是专业账户（创作者·个人博客类），2026-10-20 实测确认。
- **FoxProfile profiles 接口会 inline 返回代理凭据（2026-10-25 实证）**：查环境状态时绝不直接打印 `/api/v1/profiles` 原文，只取 name + is_running 两个字段；凭据值一律不进回复、不进文件、不进记忆。
- **FoxProfile 改代理无需重建（2026-10-26 实证）**：PATCH /api/v1/profiles/{name} 只改 proxy 字段，不动登录态、可恢复；但 **curl 通 ≠ 浏览器代理可用**：备用线 20018/20019 在 Simon 环境换线后浏览器连报 502（格式纠正后仍 502），已恢复原代理，勿再直接拿这两条线换浏览器环境。
- **ixBrowser agent 上跑 PowerShell 脚本：复杂脚本会空输出（2026-11-16 实证）**：经 /exec 调 `powershell -File uploads\*.ps1` 时，只含 where/Test-Path/Write-Output/Get-ChildItem 的小脚本正常回显；一旦包含 Get-CimInstance 带 or 的 -Filter、VersionInfo、注册表 Get-ItemProperty 等段落，整个脚本返回空 stdout、returncode 0、无报错（原因未明）。对策：拆成小脚本逐段跑，只保留简单结构；中文注释也曾怀疑过，已排除（纯 ASCII 版同样空输出）。
- **ixBrowser agent v10：10 号并行开得动（2026-11-19 14:14 实测）**：默认分组 10 个号（FB 7 + IG 3）同时打开，agent 保持响应，10 个号逐个 eval 全部返回、均已登录。旧结论「同时开 ≥7 个 profile 会拖垮 agent」是 v9 时期的，v10 上已不成立（至少开 + 轻量 eval 这层）。注意：此次只测了「同时打开 + 轻量读取」，没测 10 号同时跑评论/私信/发布等重负载，正式并行跑活仍要看实战。另：profile 35（Bertie）首开失败，报错「显示已开、但本机已开列表里找不到调试地址，可能在别的 ixBrowser 登录下开的」；经 agent close 再 open 即恢复，属残留状态问题。
- **IxAgent check() 会拉起已关的 profile（2026-11-17 实证，p43）**：对已关的 profile 调 `check()` 会重新启动它（新 pid/调试端口）；确认 profile 是否已关只用 `opened()` 列表核对，勿对已关的号调 check；关完务必用 opened() 复核。
- **浏览器崩溃丢登录态可用 cookie 备份恢复（2026-10-29 实证）**：Camoufox 崩溃/重启后环境打开变登录页时，先停浏览器，把 `camoufox_data/<env>/cookies.sqlite.bak` 拷回 `cookies.sqlite` 并删掉 `-wal`/`-shm`，再拉起即恢复登录（Fowler/Jioklm/Jusa 三号同法全恢复）；操作前先把当前 cookies.sqlite 备份到一边，勿在浏览器运行时拷。
- **Codex 商店版没有命令行可调（2026-11-20 实测）**：电脑上装的是 Microsoft Store 版 OpenAI.Codex，`where codex` 查不到；`codex-core-command-runner.exe` 存在但要 pipe-in 输入，不是给人用的 CLI；想用 GPT 生图没有无窗口入口，要么走 ChatGPT App，要么 Muse 自己生成。**ixBrowser agent /exec 的 dir 回显对中文路径和盘符根目录不可靠（2026-11-20 实测）**：`dir D:\ /b`、中文文件夹 `dir /b` 会返回空，`cd /d` 进目录后再 `dir`、或直接列到底层子文件夹才能看到文件，核查时别只凭上层列表为空就断定没有。
- **FB Reels 标签页核查不可靠（2026-11-19 实证，重大纠正）**：`fb_list_reels.py` 读 Reels 标签页返回 [] 时，时间线上可能明明有 Reel——Victoria 01 的 9 次“失败”发布其实全发成了（CLI `timeline fetch` 查实）。FB 发没发成一律以 CLI `timeline fetch` / `post read` 为准，不许只凭 Reels 标签页为空就断言失败、更不许直接重试（会刷出重复帖）。
- **FB 公共主页 Reels 没有隐藏选项（2026-11-03 实证，Dr.qh88）**：Reels 视频菜单只有保存/复制链接/删除等，无 Hide；Meta Business Suite 内容 > Posts & reels 的 Manage post 子菜单也只有 Edit、Delete、Expire now、禁止嵌入、改日期、改混剪音频等，无 Hide/Archive。Expire now 不等于隐藏、会改发布状态，未经用户决定不得擅自点。
