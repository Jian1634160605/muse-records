# ixBrowser 常驻小程序 v7 员工受限版（跑在员工 Windows 电脑上）

## 这是什么

一个很小的本地服务，装一次就不用管了。老板那边的 Muse 发指令过来，它在本机帮你：

- 列出 ixBrowser 里的全部 profile（账号），打开 / 关闭指定的 profile
- 打开 Facebook / Instagram 核对当前登录的是哪个账号，并截图保存
- 让浏览器做动作：在 Facebook、Instagram、Messenger 里点按钮、打字、发评论、回私信
- 收视频 / 图片文件（只能收 .mp4、.mov、.jpg、.jpeg、.png、.webp），存在 uploads/ 里，再经浏览器发出去

它必须跑在你的电脑上，因为 ixBrowser 的接口和浏览器调试端口只听本机，
Muse 从外面够不着。只有这个小程序在，你电脑上的浏览器才能被远程操作。

它不会把你的密码、cookie 发出去，只回传操作结果（比如账号名、截图）。
所有接口都要带令牌才能调（令牌在 config.json 里，只有老板那边的 Muse 知道，不要发给别人）。

## 员工受限版和老板那台的区别

这是受限版，只保留做 FB / IG 运营必须的接口，其他都去掉了：

**保留的接口（能做的事）：**
- GET /health、/profiles、/opened
- POST /open、/close、/check、/tabs、/goto、/click、/type、/shot、/attach、/upload

**去掉的接口（做不了的事）：**
- POST /exec —— 不能在你电脑上跑任何命令
- POST /files/list、/files/read —— 不能读你电脑上任意文件夹和文件
- POST /eval —— 不能在页面里执行 JS
- POST /update —— 不能远程更新代码，更新须老板重新发包重装

**另外三条限制：**
- /goto 只能打开 facebook.com、instagram.com、messenger.com（含 www 子域），其他网站一律拒绝
- /attach 只能挂 uploads/ 目录下的文件，其他路径一律拒绝
- /upload 只收 .mp4、.mov、.jpg、.jpeg、.png、.webp，上限 200MB

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

员工版没有远程自更新。老板发新包时，解压覆盖后重新双击 `install.bat` 即可。

## 出问题怎么办

- 打开 `agent.log` 看最后几行，把截图发给老板，不要只发一句话。
- 提示连不上 ixBrowser：先确认 ixBrowser 客户端开着，
  并且设置里已开启 Local API 开关。
- 提示 `profile_id 必须是数字`：profile_id 要传数字，不能带引号。
- 桌面快捷方式丢了：再双击一次 `install.bat` 就重建。

## 文件说明

- `ixbrowser_agent.py`：服务主程序（员工受限版 v7）
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
- `concat_bridge.py`：Concat 剪辑桥接服务（第二阶段再装，见安装说明）
- `concat_bridge_startup.bat`：Concat 桥接开机自启
