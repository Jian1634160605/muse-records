# AGENTS.md

Your operating manual for this workspace, written by you. Your main instructions cover how you work in general. This file is where you keep the specific, durable lessons and conventions you pick up as you work, the kind of thing you'd want a future session to know. It's not about the user (that goes in `USER.md` and your memory) or your personality (that's `SOUL.md`); it's about how you get work done here.

## Conventions
Add an entry whenever you work something out worth keeping, for example:
- a convention you've settled on ("keep data exports in `workspace/exports/` and clean them up monthly")
- a tool or site quirk worth remembering ("site X hides its form behind a cookie banner; dismiss it first")
- a workflow that worked, or a mistake not to repeat

It starts empty and is meant to grow slowly. Don't pad it; a short, accurate file beats a long, stale one.

- **浏览器活绝不派给子代理**（2026-10-22 实证）：子代理没有实时浏览器控制权限，browser.browse 必须由我本人直接派发；派 subagent 做只读复查会原样返工（它只能 CLI/文本抓取，浏览器部分交白卷）。

## 站点经验
- **凭据绝不上终端输出（2026-10-22 实证）**：`~/.agent-reach/proxy-*.txt` 只用于 `export HTTPS_PROXY="$(cat ...)"` 形式，**绝不** `cat`/echo/head 打印到 stdout 检查连通性——输出会进日志与上下文。连通性用带代理的实际 API 调用验证。
- Instagram 网页版（桌面）无法编辑主页链接：编辑资料页的"网站"栏是禁用的，IG 原文提示"只能在移动设备上编辑你的链接"——与账号类型无关（专业号也一样）。加/改 IG 主页链接只能让用户在手机 IG App 里操作。IG 连接器（instagram-cli）也只能改简介文字、头像，不能改链接。christycrawford85 本身已是专业账户（创作者·个人博客类），2026-10-20 实测确认。
- **FoxProfile profiles 接口会 inline 返回代理凭据（2026-10-25 实证）**：查环境状态时绝不直接打印 `/api/v1/profiles` 原文，只取 name + is_running 两个字段；凭据值一律不进回复、不进文件、不进记忆。
- **FoxProfile 改代理无需重建（2026-10-26 实证）**：PATCH /api/v1/profiles/{name} 只改 proxy 字段，不动登录态、可恢复；但 **curl 通 ≠ 浏览器代理可用**：备用线 20018/20019 在 Simon 环境换线后浏览器连报 502（格式纠正后仍 502），已恢复原代理，勿再直接拿这两条线换浏览器环境。
- **浏览器崩溃丢登录态可用 cookie 备份恢复（2026-10-29 实证）**：Camoufox 崩溃/重启后环境打开变登录页时，先停浏览器，把 `camoufox_data/<env>/cookies.sqlite.bak` 拷回 `cookies.sqlite` 并删掉 `-wal`/`-shm`，再拉起即恢复登录（Fowler/Jioklm/Jusa 三号同法全恢复）；操作前先把当前 cookies.sqlite 备份到一边，勿在浏览器运行时拷。
- **FB 公共主页 Reels 没有隐藏选项（2026-11-03 实证，Dr.qh88）**：Reels 视频菜单只有保存/复制链接/删除等，无 Hide；Meta Business Suite 内容 > Posts & reels 的 Manage post 子菜单也只有 Edit、Delete、Expire now、禁止嵌入、改日期、改混剪音频等，无 Hide/Archive。Expire now 不等于隐藏、会改发布状态，未经用户决定不得擅自点。
