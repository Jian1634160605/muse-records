---
name: employee-agent-install
description: 把员工电脑接进老板的 ixBrowser 远程操作：员工版受限小程序 v7 的安装部署指南。给其他电脑部署安装时用。
---

# 员工电脑接入 · 安装部署

把一台员工电脑接进老板的 ixBrowser 远程操作，让老板能远程操作这台电脑上 ixBrowser 里的 FB / IG 账号。按下面步骤装，全部装完才算接通。

**给谁用**：少婷、辰昊、蔡蔡、小徐、尹卓（每人一份以自己名字命名的包）。

**先确认**：员工收到的是写着自己名字的那份包（比如“少婷-agent-v7-restricted.zip”），不要用别人的包，也不要用老板那台的包。每人的令牌都不一样，用错了连不上。

## 什么时候用这个 skill

- 给一台新员工电脑部署安装受限版小程序时用。
- 员工装机出问题、要排查时用。
- 核对一台员工电脑是否接通时用。

## 第一步：ixBrowser 用自己的员工号登录，开 Local API 开关

1. 打开 ixBrowser，确认右上角登录的是自己的员工号（少婷、辰昊、蔡蔡、小徐、尹卓其中一个）。
2. **不要用管理员账号 liveon01 登录自己的电脑**，只能看到自己分组的账号。
3. 在 ixBrowser 设置里找到 Local API，把开关打开。
   - Local API 是付费功能，由老板那边统一开通；如果客户端里找不到这个开关，先问老板。
4. 确认能看到自己分组的 profile 列表，账号是登录着的。

## 第二步：装 Tailscale，登进老板那个网络

1. 去 Tailscale 官网下载安装包，装到电脑上，一路点下一步。
2. 装完在右下角找到 Tailscale 图标，点登录，用老板给的那个账号登进去。
3. 登好后，把 Tailscale 显示的那个 100 开头的地址（比如 100.78.x.x）发给老板。
   - 老板那边要按这个地址登记电脑，没这个地址他连不到你。

## 第三步：装 Python

1. 去 Python 官网下载安装包（或者用 python-manager，选一个最新的 Python 版本装上）。
2. 安装时注意勾上“Add Python to PATH”（加到系统路径）。
3. 装完关掉黑窗口再重开一个，按 Win+R，输入 cmd 回车，输入 `python --version` 回车，能打出版本号（比如 Python 3.12.x）就说明装好了。打不出来就重装一遍，记得勾 PATH。

## 第四步：装 ixBrowser 小程序（员工受限版 v7）

1. 把以自己名字命名的 zip 解压到一个固定文件夹：`D:\ixbrowser-agent`，以后别挪地方。
2. 进这个文件夹，双击 `install.bat`。
3. 它会做三件事：桌面建一个快捷方式“ixBrowser Agent”、加到开机自启、立即在后台启动（没有黑窗口）。
4. 看到“Done”就好了，以后开机自动跑，不用再管。
5. 第一次运行会下载安装依赖（ixbrowser-local-api、playwright），需要几分钟，耐心等它跑完。

**验证装没装好**：
- 打开任务管理器，看有没有 pythonw.exe 在跑；或者
- 打开 `D:\ixbrowser-agent\agent.log`，看最后一行是不是显示已启动、版本号是 v7。
- 两个都没看到，就把 agent.log 最后几行截图发给老板。

**平时不用管它**：
- 想停：双击 `stop.bat`。
- 想手动在前台跑（看日志）：双击 `start.bat`，会弹出黑窗口显示日志。
- 桌面快捷方式丢了：再双击一次 `install.bat` 就重建。

## 第五步（可选，第二阶段）：装 Concat 剪辑桥

这一步可以先不做，等老板说要剪视频了再装。

1. 把 Concat 装到 `D:\Concat\concat.exe`（老板会给安装包或下载地址）。
2. 在 `D:\ixbrowser-agent` 里已经有 `concat_bridge.py` 和 `concat_bridge_startup.bat`，双击 `concat_bridge_startup.bat` 就能启动桥接服务；想开机自启，把它也放到开机启动文件夹里。
3. 桥接服务和 ixBrowser 小程序用同一个令牌，不用另外配。

## 这个受限版能做什么、不能做什么

| 能做 | 不能做 |
|---|---|
| 列出 ixBrowser 里的 profile、打开 / 关闭指定的号 | 不能在电脑上跑任何命令 |
| 打开 Facebook / Instagram 核对当前登录的是哪个账号，并截图 | 不能读电脑上任意文件夹和文件 |
| 在 Facebook、Instagram、Messenger 里点按钮、打字、发评论、回私信 | 不能在页面里执行 JS |
| 收视频 / 图片文件（只收 .mp4、.mov、.jpg、.jpeg、.png、.webp），存在 uploads/ 里再经浏览器发出去 | 不能远程更新代码，更新须老板重新发包重装 |
| 打开的网站只限 facebook.com、instagram.com、messenger.com | 其他网站一律打不开 |
| 挂文件只允许 uploads/ 目录下的文件 | 其他路径的文件挂不上 |

一句话：这个小程序只能帮老板远程操作 ixBrowser 里的 FB / IG 账号，碰不到电脑上别的文件，也跑不了命令。

## 装完后要发给老板的东西

1. Tailscale 地址（100 开头的那个）。
2. agent.log 最后一行截图，或者一句话“我装好了，任务管理器里有 pythonw.exe”。
3. 老板那边登记后会逐台验：列出 profile、核对登录账号，验通了才算接通。

## 出问题怎么办

- 打开 `D:\ixbrowser-agent\agent.log` 看最后几行，把截图发给老板，不要只发一句话。
- 提示连不上 ixBrowser：先确认 ixBrowser 客户端开着，并且设置里已开启 Local API 开关。
- 提示 `profile_id 必须是数字`：这是老板那边传参的问题，告诉老板就行。
- 令牌在 `D:\ixbrowser-agent\config.json` 里，**不要发给别人，也不要贴到群里**。

## 老板侧登记（给 Muse 的提醒）

- 每台员工电脑一个独立令牌，**谁的包只发给谁、绝不群发混发、令牌绝不在聊天或记忆里复述**。
- 员工装好回传 Tailscale 地址后，逐台登记 IP 加令牌、验 `/health`（须是 v7）、列 profile、核对登录，验通一台算一台。
- 员工电脑只看自己授权分组，不动老板的默认分组，不核验老板的账号。
