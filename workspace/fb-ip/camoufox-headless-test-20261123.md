# Camoufox 无窗口实测报告

> **2026-11-24 13:42 成安决定删掉 Camoufox，不再用。**已从他电脑上完全卸载：pip 包 camoufox 0.5.6 已卸、浏览器本体缓存 `C:\Users\Administrator\AppData\Local\camoufox` 已删、`D:\camoufox-profiles`（含 p108 常驻 profile）已删、uploads 里所有 Camoufox 相关脚本/日志/截图/cookie 文件已删，三项核验全是 gone。ixBrowser 不受影响，照常跑。以下为删除前的实测记录，留作备查。

日期：2026-11-23 18:2x
测试：Camoufox 指纹浏览器 headless=True 能否在不弹可见窗口的情况下打开 facebook.com、读页面、关掉

## 结论：通过 ✅

Camoufox 真正无窗口可用。全程成安电脑上没有出现浏览器窗口。

## 实测过程

1. **发现 Camoufox 并没装**：成安电脑上 Python 3.15.2，没有 camoufox 包、没有浏览器本体（之前说的“已装”是指 cookie 备份的目录格式，不是浏览器本身）。
2. **安装**：`pip install --only-binary=:all: camoufox` 成功装上 0.5.6（注意：0.5.9 需要 zstandard，而 Python 3.15 没有 zstandard 的预编译包、且电脑缺 MSVC 编译器编不出来；0.5.6 用 browserforge 不依赖 zstandard，所以能装）。顺带把 Playwright 从 1.65.2 降到了 1.62.0（camoufox 0.5.6 要求 <1.63）。
3. **下载浏览器本体**：`python -m camoufox fetch`，v159.0-beta.43，约 1.27GB，下载完成。路径：`C:\Users\Administrator\AppData\Local\camoufox\camoufox\Cache\browsers\official\159.0-beta.43-e9bba4a1\camoufox.exe`
4. **无窗口测试**：`Camoufox(headless=True)` 启动，打开 https://www.facebook.com，读标题，等 20 秒，关掉。

## 实测证据

- facebook.com 正常打开，页面标题读到 "Facebook"
- `navigator.webdriver: False`（反检测生效）
- 测试运行期间查可见窗口：7 个 camoufox 进程，全部 `MainWindowTitle=''`、`HasMainWindow=False`，可见窗口列表里没有 Camoufox，只有成安平时开的应用（微信、飞书、剪映、Chrome 等）
- 测试结束：浏览器正常关闭，无残留 camoufox 进程

## p108 真号登录完成（2026-11-24 11:05–11:22，成安给密码后跑通）

**结论：p108 已在 Camoufox 无窗口里完整登录，信息流直进，两次重启都稳。✅**

- 过程：成安给了 10 个候选密码让挨个试。**10 个在 Camoufox 里全被 FB 拒**（有的显示 "The login information you entered is incorrect"；第一个曾有一次跳到 2FA 页但显示 "Invalid request"）。最后用 **ixBrowser profile 108 里存的密码**（9 位，与给的 10 个都不同）才通过：输密码 →  proper 2FA 页（`two_step_verification/two_factor/?flow=two_factor_login`）→ 用 profile 里存的 TOTP 密钥（32 位）现算 6 位码填入 → 通过 → 到 "You're logged in. Trust this device?" 页（显示 Firefox on Windows）。
- **关键教训：给的密码不等于 profile 里存的密码**。ixBrowser 建号时存的密码才是 FB 认的那个；以后迁号先读 profile 里存的密码和 TOTP 密钥，别只靠成安给的密码表。读 profile 用 SDK `get_profile_list(profile_id=...)`（返回是 list 不是 dict，要取 `data` 或 `list` 键；第一次写错键导致读不到密钥，已修正）。**密码和密钥只在脚本内存里用，绝不打印、不写日志、不进记忆**；含密码的脚本用完立即从成安电脑删除（已删干净）。
- **指纹稳定性已验证 ✅**：登录完成后两次重开同一 profile（11:19、11:21），**都直接进信息流**（导航 7/7，无密码、无 2FA、无 Trust 页）。说明 Camoufox 常驻 profile 的会话是稳定的，不用每次重登；"Trust this device" 那页在重开时根本没再出现（会话已有效，那页只是可选步骤）。
- 信息流截图：`~/workspace/fb-ip/p108-camoufox-feed-20261124.png`（侧栏显示 Joinul Manik，What's on your mind, Joinul?，帖子正常加载）。
- 仍未测：用 Camoufox 做账号操作（发帖/评论/私信），那是下一步；每号仍需自己的代理（本次 p108 没配代理也能打开，正式跑要配）。

## p108 常驻 profile（2026-11-24 10:45–10:50，成安说“好”后建）

**结论：profile 建好了，但 FB 还要一次密码——cookie 只能走到选号页，进信息流要密码。**

- 常驻 profile 目录：`D:\camoufox-profiles\p108`（57 个文件，已落盘）。
- 正确调法：`Camoufox(headless=True, persistent_context=True, user_data_dir=...)`——**只传 user_data_dir 不加 persistent_context=True 会报错**（`BrowserType.launch() got an unexpected keyword argument 'user_data_dir'`），因为不加这个开关走的是 `launch()` 不是 `launch_persistent_context()`。
- 过程：cookie 导入 → 打开 facebook.com → 出现“Continue as Joinul Manik”→ 点 Continue → **弹出密码框**（Joinul Manik + Password 输入框 + Log in 按钮，见截图 `~/workspace/fb-ip/p108-camoufox-password-prompt-20261124.png`）。
- 这不是验证、不是封号，是新设备/新指纹的标准流程：会话 cookie 能认出账号，但新指纹首次进要重新输一次密码确认。**我没输密码**（没有这个号的密码，也不会在聊天里要密码）。
- 待定：要让 p108 在 Camoufox 里真正能跑，得有人（成安）在 Camoufox 的 p108 profile 里输一次密码；或者评估指纹固定方案（每次启动指纹会变的话，下次可能又要 Continue/输密码）。

**结论：通过 ✅——p108 的登录态能导进 Camoufox 无窗口跑。**

- 拿的是新号 p108（FB 账号 61575760092172，显示名 **Joinul Manik**）。
- 登录态来源：ixBrowser SDK `get_profile_cookie`（**profile_id 必须是数字 int，传字符串会报 code 1000 "profile_id must be a Number"**）；共 13 个 cookie，其中 11 个 facebook.com（含 c_user、xs、sb、datr、fr 等会话关键 cookie）。cookie 只写在成安电脑上的文件里，不打印、不进聊天。
- 做法：11 个 FB cookie 转成 Playwright 格式 → `context.add_cookies()` → `Camoufox(headless=True)` 打开 facebook.com。
- 结果：**3 次运行 URL 都留在 facebook.com/、都没有登录表单**；截图显示 FB 认出了这个号，出现“Continue as Joinul Manik”选号页（点 Continue 就进信息流）。这是新设备/新指纹的正常一步确认，不是验证、不是封号。
- 注意：前两次我的检测逻辑写错了（只查信息流侧栏和登录表单，选号页两者都没有，误报“没登录”）；第三次加截图才定论。以后判断登录态要认“选号页/Continue 按钮”这种中间态，不能只看侧栏。
- 测试期间没有出现 Camoufox 可见窗口（headless 再次确认）；中间有两扇 “Facebook - Chromium” 的 Chrome 窗口短暂出现又消失，10:38 再查已没有，无法确定归属，疑似成安自己在 Chrome 里打开又关了，未证实与 Camoufox 有关。

## 注意事项

- Camoufox 是代码驱动的（Playwright API），不是 ixBrowser 那种带界面的 profile 管理器。换过去要重新搭驱动，不是装上就能点着用。
- 每个号要自己管 profile 文件夹和 cookie，登录态要从 ixBrowser 那边导过来或重新登录。
- 本次只测了“打开 facebook.com 读标题”，没登录任何账号、没操作任何账号。带登录态跑账号操作还没测。
- **p108 登录态已验证可用**：cookie 导入后 FB 显示“Continue as Joinul Manik”选号页，点 Continue 即进信息流；尚未在 Camoufox 里点 Continue、尚未做任何账号操作（发帖/评论/私信均未测）。
