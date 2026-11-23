# agent-desktop：直接操作桌面软件

> 来源：Vercel Labs 开源项目 vercel-labs/agent-desktop（Apache 2.0，视频里十大项目之一）。原文是给 AI agent 的 skill，这里按 Muse 的用法改写。核心理念：**不靠截图猜像素，直接读操作系统的无障碍树（accessibility tree），按元素编号点**。

## 这是什么

agent-desktop 是一个 CLI，读操作系统的无障碍树，把桌面应用的界面转成 JSON，每个可操作的元素带一个编号（ref）。agent 按编号点按/打字，再读一遍界面确认结果，循环操作。它本身没有模型，观察-行动-验证的循环由你来跑。

**用在哪**：在用户电脑上操作桌面软件——点按钮、填表、读界面状态、切菜单、打勾、滚动、拖拽、打字、按快捷键、截图、管理窗口、用剪贴板、开/关应用。咱们的场景：操作 Concat、剪映、微信电脑版这类桌面软件，不用再靠截图猜坐标。

**重要**：这个 CLI 要装在**用户电脑（Windows）**上才能操作那台电脑的软件，不是在我云端装。调用方式是经 ixBrowser agent 的 /exec 在用户电脑上跑命令。

## 已装好（2026-11-19 23:08 实测）

- 位置：`D:\ixbrowser-agent\tools\agent-desktop\agent-desktop.exe`，版本 v1.3.1。
- 实测 `agent-desktop status` 返回 ok：平台 Windows，无障碍权限已授予（accessibility: granted），支持 window / focused / sheet / menu / start-menu / taskbar / system-tray 等界面。
- 用户电脑上没有 Node.js，所以装的是 GitHub Releases 的原生包（`agent-desktop-v1.3.1-x86_64-pc-windows-msvc.tar.gz`），不用 npm。
- 调用时用完整路径：`"D:\ixbrowser-agent\tools\agent-desktop\agent-desktop.exe" status`。

## 安装

在用户电脑上（二选一）：

```powershell
npm install -g agent-desktop
```

或直接从 GitHub Releases 下对应平台的原生包（不用 Node）。

装完先跑：

```powershell
agent-desktop status                # 看平台、权限、支持的界面
agent-desktop skills get platform   # 加载当前操作系统的 skill（Windows 版）
```

## 用法循环

```powershell
agent-desktop snapshot --skeleton --app "Notes" -i --compact   # 先浅画一张图
agent-desktop snapshot --root @s8f3k2p9:e3 -i --compact        # 钻进一个区域
agent-desktop click '@s8f3k2p9:e12'                            # 按编号操作
agent-desktop snapshot --root @s8f3k2p9:e3 -i --compact        # 再读一遍验证
```

- PowerShell 里编号必须加引号（`'@s8f3k2p9:e12'`），因为裸 `@token` 是 splatting 操作符。
- 编号属于它那次快照：`@<snapshot_id>:e<N>`，比如 `@s8f3k2p9:e1`。界面一变就失效（`STALE_REF`），要重新快照拿新编号。
- 小应用不用画骨架，直接 `snapshot -i` 全量读。
- 每次操作完必须重新读一遍验证，不要假设成功了。

## 重试规则

- 只有 `disposition.retry` 是 `safe` 时才能重试或换个办法。只 `not_delivered` 是安全的。
- 其他 delivery 值表示动作可能已经生效了，再点一次会点两下、打字打两遍、开关会自己弹回去。
- 不安全的结果先读当前状态（`get`、`is` 或新快照）再决定，不要直接重试。
- `details.retryable: false` 表示等也没用，换个办法。

## Headless 与 headed

- 默认无头（headless）：用无障碍语义调用，不抢焦点、不动鼠标、不模拟按键、不动剪贴板。没有语义路径就直接失败，不硬来。
- 只有用户明确允许物理输入（双击、悬停、拖拽、抢焦点）时才用 `--headed`。绝不要因为无头失败就切 headed 去补救。

## 隐私

快照、剪贴板、截图、命令输出可能含用户桌面上的隐私内容，不要写进公开日志、不要上传。
