# ixBrowser 常驻小程序 v6（跑在你的 Windows 电脑上）

## 这是什么

一个很小的本地服务，装一次就不用管了。Muse 在另一台电脑上发指令过来，它在本机帮你：

- 列出 ixBrowser 里的全部 profile（账号），打开 / 关闭指定的 profile
- 打开 Facebook / Instagram 核对当前登录的是哪个账号，并截图保存
- 让浏览器做动作：点按钮、打字、发评论、回私信、发视频
- 读写你电脑上的文件、执行命令（视频要经这台电脑的浏览器发出去，文件须先到这台电脑上）

它必须跑在你的电脑上，因为 ixBrowser 的接口和浏览器调试端口只听本机，
Muse 从外面够不着。只有这个小程序在，你电脑上的浏览器才能被远程操作。

它不会把你的密码、cookie 发出去，只回传操作结果（比如账号名、截图）。
所有接口都要带令牌才能调（令牌在 config.json 里，只有 Muse 知道）。

## 安装（只装一次）

1. 把压缩包解压到一个固定文件夹（比如 `D:\ixbrowser-agent`，以后别挪地方）。
2. 双击 `install.bat`。
3. 它会做三件事：桌面建一个快捷方式“ixBrowser Agent”、加到开机自启、立即在后台启动（没有黑窗口）。
4. 看到“Done”就好了，以后开机自动跑，不用再管。

第一次运行会下载安装依赖（ixbrowser-local-api、playwright），需要几分钟。

## 平时

- 什么都不用做。开机自动启动，后台一直跑着。
- 想确认它在不在跑：看任务管理器里有没有 pythonw.exe，或打开 `agent.log` 看最后一行。
- 想停：双击 `stop.bat`。
- 想手动在前台跑（看日志）：双击 `start.bat`，会弹出黑窗口显示日志。

## 更新

不用你管。Muse 发新版时直接远程给你装好（自己下载、校验、替换、重启，
失败自动滚回旧版）。你会在 `update_result.txt` 里看到 update ok。

v6 修了 v5 的更新毛病：以前更新时旧进程可能没退干净、一直占着端口，
新版起不来还误报成功。现在更新前会先清掉所有旧进程，验活时核对版本号，
以后再也不用你手动点 stop.bat、再点快捷方式。

## 出问题怎么办

- 打开 `agent.log` 看最后几行，把截图发回来，不要只发一句话。
- 提示连不上 ixBrowser：先确认 ixBrowser 客户端开着，
  并且设置里已开启 Local API 开关。
- 提示 `profile_id 必须是数字`：profile_id 要传数字，不能带引号。
- 桌面快捷方式丢了：再双击一次 `install.bat` 就重建。

## 文件说明

- `ixbrowser_agent.py`：服务主程序
- `ixbrowser_driver.py`：ixBrowser API 驱动（不要改）
- `config.json`：调用令牌（不要发给别人）
- `requirements.txt`：依赖清单
- `install.bat`：装一次（桌面快捷方式 + 开机自启 + 启动）
- `stop.bat`：停用
- `start.bat`：前台手动启动（看日志用）
- `agent.log`：运行日志
- `agent.pid`：运行中的进程号
- `shots/`：核对账号时保存的截图
- `uploads/`：Muse 推过来的视频等文件
- `backup_prev/`：上次更新前的旧版备份（更新失败自动回滚用）
