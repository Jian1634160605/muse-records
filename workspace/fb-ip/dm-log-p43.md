# DM 盯守台账 — pokkhusadedere（IG 鼻子线，ixBrowser profile 43）

## 2026-11-17 19:38 轮次（IG 首轮）

- 身份核验：通过。Direct 收件箱顶栏显示用户名 pokkhusadedere；首页 feed 正常加载，已登录。
- 打开异常：首次 `open(43)` 失败，ixBrowser 侧报错 `code=1 message=The returned 'error.code' must be an integer`；重试后 `open` 成功（profile 当时已处于打开状态，debugging_address 127.0.0.1:55823）。非 429/226/344，未停号。
- 通知：最新一条为 11-02 thewanderingframe37 开始关注你；其后无新通知。无新关注需筛查（thewanderingframe37 仅关注、无医美意向信号，不联系）。
  - 注意（旧记录，非本轮新发）：10-24 有一条「We added a restriction to your account. See why.」；10-08「We updated your settings after 1 account was added to the same Accounts Center.」账号目前功能正常（feed/通知/私信均可读），仅作观察项记录，下轮留意是否出现新的限制提示。
- Direct Primary：仅 1 个线程 — pothrasevewase，最后一条是我方 8 周前发的「你」，对方无新回复。本轮无发送。
- Direct Requests：空（0 条）。
- General：未单独展开（Primary 仅 1 线程且无新消息；Requests 为空）。
- 合格客资：无。致命问题：无。
- 轮次结束已 `close(43)`，profile 已关。

## 2026-11-17 20:08 轮次（fb-dm-p43）

- 身份核验：通过。首页导航含 `/pokkhusadedere/` 个人主页链接，feed 正常加载，已登录。注意：`check()` 返回的当前标签是 facebook.com 登录页（profile 默认起始页），不代表 IG 未登录。
- 通知：最新仍为 11-02 thewanderingframe37 开始关注你，其后无新通知；无新关注需筛查。10-24「We added a restriction to your account」仍为旧记录，无新增限制提示。
- Direct Primary：**本轮两次均未成功读到线程列表**。`goto /direct/inbox/` 返回标题 "Instagram • Messages"，但数秒后 eval 显示页面已跳离（第一次跳回首页 feed，第二次跳到 /explore/ 且正文只剩页脚、threadLinks 为空）。未读到、未发送任何消息，不谎报。上一轮（19:38）Primary 仅 1 线程 pothrasevewase、最后一条为我方 8 周前消息、无新回复；本轮未能复核该线程状态，待下轮优先重读。
- Direct Requests：空（0 条），读到正常。
- 合格客资：无（未确认新私信）。致命问题：无（无 429/226/344；登录态正常）。
- 收尾异常：重试脚本末尾 `close(43)` 报 code=1009 Process not found（进程已不在）；随后一次 `check(43)` 把 profile 重新拉起（20:31:23，pid 41400）——教训：`check()` 会拉起已关的 profile，确认是否已关只用 `opened()`。已再次 `close(43)` 成功，`opened` 列表确认 43 不在其中。
- 轮次结束已 `close(43)`，profile 已关。

## 2026-11-17 20:38 轮次（fb-dm-p43）

- 身份核验：通过。首页导航含 `/pokkhusadedere/` 个人主页链接，feed 正常加载，已登录（本轮三次核验均通过）。
- 通知：最新仍为 11-02 thewanderingframe37 开始关注你，其后无新通知；无新关注需筛查。10-24「We added a restriction to your account」仍为旧记录，无新增限制提示。
- Direct Primary：**本轮第三次尝试终读到**。仅 1 个线程 — pothrasevewase，最后一条是我方 8 周前发的「你」，对方无新回复。本轮无发送、无需回复。
- Direct Requests：空（0 条），读到正常。
- 传输抖动：轮次中 ixBrowser agent 两次短暂失联（curl 52 Empty reply，约 20:41 与 20:47，各持续 2–3 分钟后自行恢复），非 429/226/344；期间一次 `open(43)` 响应被截断（curl 18）但服务端实际已打开 profile，另一次 `close(43)` 返回 ok:true 后 opened 列表仍含 43，又补关一次才真正关闭。教训：open/close 返回截断或 ok 都不能全信，必须以 `opened()` 列表核验为准。
- 合格客资：无。致命问题：无（无 429/226/344；登录态正常）。
- 轮次结束已 `close(43)`，`opened()` 列表确认 43 不在其中，profile 已关。
