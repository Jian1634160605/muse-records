# 私信盯守台账 — gaga5456（IG 鼻子线，ixBrowser profile 65）

## 2026-11-17 19:47（首轮，job fb-dm-p65）

- **身份核验通过**：instagram.com 首页标题「秦昊博士 (@gaga5456) • Instagram 照片和视频」，og:title「Dr. Qin Hao (@gaga5456)」，未跳登录页。主页数据：12 帖子、0 追随者、47 下列的。
- **Direct 收件箱读不到（被 IG 每日限额页挡住）**：两次打开 `instagram.com/direct/inbox/`，页面标题为「Instagram • Messages」但正文只有 54 字：「您已达到每日限额 / 你今天使用 Instagram 的时间已经达到了9 小时37分钟。现在是关闭应用的好时机。」DOM 里无可点的关闭/稍后按钮（仅翻译反馈按钮）。重试一次，结果相同。
- **通知页读不到**：打开 `instagram.com/notifications/` 被重定向回个人主页 `instagram.com/gaga5456/`，无通知列表。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：收件箱不可见，无法判断有无新私信/新关注；不编结果。
- **判定**：不是 226/344、不是登录失效（登录正常、主页正常）。是 IG「使用时间每日限额」拦截（账号在「你的动态」里设了每日使用上限或 IG 默认提醒），今日已用 9 小时 37 分钟。按手册「打不开先记日志，不硬闯」，未尝试绕过/改设置（改账号限额设置须用户决定）。
- **待办**：用户需在 IG App「你的动态 → 每日使用上限」里调高或关闭该号限额，或等明日限额重置；下轮再试收件箱。
- 轮次结束已 `close(65)` 关掉 profile。

## 2026-11-19 21:12（本轮，job fb-dm-p65）

- **身份核验通过**：instagram.com 首页正常加载（未跳登录页）；Direct 收件箱页眉显示用户名 `gaga5456`，即本号。**11-17 的 IG 每日使用限额问题已解决**：本轮收件箱正常打开，未再出现限额页（用户 11-19 已在手机时间管理里关掉限额）。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程；**Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）；**无新关注、无新评论、无新私信通知**。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile（两次打开均已关闭）。

## 2026-11-19 22:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号；通知内容与 21:12 轮次完全一致（rezazes 5 赞、eleanore.meyer.58 1 赞），为同一登录态。注意：首轮 identity eval 因传输截断（curl 18）失败，未直接读到用户名；重试轮收件箱正文首行即 `gaga5456`，以此核验。
- **Direct 收件箱为空（重试轮确认）**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。首轮 inbox eval 同样因 curl 18 失败，未当作“为空”上报；重试后读回确认。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：无新关注、无新评论、无新私信通知。与 21:12 轮次相同：本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输故障记录**：① 首次执行误用 `~/.agent-reach/proxy-acct2.txt` 覆盖 HTTPS_PROXY，全部调用 curl 56 连接被重置；改回默认环境代理后 agent（v10）正常——该 proxy-acct2.txt 文件疑似过期/错线，以后本轮只用默认环境代理，不再覆盖。② 轮中出现零星 curl 18（传输截断）与 curl 52（agent 空回复），属瞬时故障，重试后通过；③ close 第一次因 curl 52 空回复未生效，复核 opened 列表发现 65 仍开着，第二次 close 返回 closed:true，再查 opened 列表确认 65 已不在。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（在开的 5、32、38、67 为其他并行轮次的号）。

## 2026-11-19 23:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 21:12、22:12 两轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输故障记录**：首轮中 requests 页 eval 与 notifications 页 goto 各遇一次 curl 52（agent 空回复），属瞬时故障；重试轮（重开 profile）通知页正常读回，内容与前两轮一致。两次 close 均返回 closed:true，opened 列表复核确认 65 已关（在开的 5、32、38 为其他并行轮次的号）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关。

## 2026-11-20 00:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（在开的 63 为其他并行轮次的号）。

## 2026-11-17 20:17（本轮，job fb-dm-p65）

- **本轮未执行：外部连接审批未通过，IxAgent 调不通**。执行脚本时到用户电脑的隧道连接（lhus1.sitenn.org）触发审批卡（approval_id ac8fb970-ffd8-42c0-9ce3-ad7e804613e3，12:19 UTC 请求），后台模式、无人点批，调用卡在 pending_user_confirmation，已终止，未重试。
- **后果**：profile 65 未打开、身份未核验、收件箱/通知均未读到；本轮未发任何私信、未通过任何好友、未筛查到新线程。**不编结果**：无法判断有无新私信/新关注。
- **注意**：上一轮（19:47）的 IG 每日使用限额（9 小时 37 分钟）问题仍未解决——即使连接恢复，收件箱仍可能被限额页挡住，需用户在 IG App「你的动态 → 每日使用上限」里调高/关闭，或等明日重置。
- **判定**：不是 226/344、不是登录失效（未验证到登录态）。是运行环境审批阻塞 + 上轮限额问题待用户处理。下轮需先确认审批已点、再试收件箱。

## 2026-11-20 01:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 00:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 为空列表，0 个在开）。

## 2026-11-20 03:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12、01:12、02:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 5、32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 5、32，为其他并行轮次的号）。

## 2026-11-20 02:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 00:12、01:12 两轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 5 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。


## 2026-11-20 04:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12、01:12、02:12、03:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 5、32 为其他并行轮次的号（5 在本轮进行中由其所属轮次自行关闭）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-20 07:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12、01:12、02:12、03:12、04:12、05:12、06:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12、01:12、02:12、03:12、04:12、05:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 5、32 为其他并行轮次的号（5 在本轮进行中由其所属轮次自行关闭）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。


- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12、01:12、02:12、03:12、04:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-20 08:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12、01:12、02:12、03:12、04:12、05:12、06:12、07:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，6d 前）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-20 10:12（本轮，job fb-dm-p65）

- **本轮未执行：ixBrowser Local API 连不上（用户电脑端）**。agent 本身正常——`health` 返回 ok、ixbrowser-agent v10（两次 health 均一次通过）。但 `opened`、`open(65)`、`close(65)` 全部失败，报错一致：「连不上 ixBrowser Local API（http://127.0.0.1:53200/api/v2/）。请确认 ixBrowser 客户端已打开，且设置里已开启 Local API 开关。」原始错误为 ConnectTimeoutError（2 秒超时）。三次 open 尝试 + 两次 close 均同错；60 秒后复核，`opened` 仍同错——**持续性故障，非瞬时波动**。
- **与 09:12 轮不同**：09:12 时 opened/health 均正常，只是 profile 65 启动报 code 1004；本轮是 ixBrowser 客户端本身不可达（Local API 无响应），**所有 profile 操作都被挡住，不只 65 号**。疑似用户电脑上 ixBrowser 客户端已关闭/崩溃，或 Local API 开关被关。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：profile 65 未打开，身份未核验，收件箱/Requests/通知均未读到，无法判断有无新私信/新关注；上一轮 08:12 收件箱与 Requests 均为空、通知无新增。**不编结果**。
- **判定**：不是 226/344、不是已确认的登录失效（未验证到登录态）。是运行环境阻塞——用户电脑端 ixBrowser 客户端不可达，需用户侧处理（重新打开 ixBrowser 客户端并确认 Local API 开关已开启，或重启 ixBrowser agent）。**属致命问题（全部账号操作被挡），需报总管/用户。**下轮先看 Local API 是否恢复再跑。
- **轮次结束 profile 65 未开着**（opened 列表读不到，但 open 从未成功、无残留进程可关），无需 close。

## 2026-11-20 09:12（本轮，job fb-dm-p65）

- **本轮未执行：profile 65 打不开（ixBrowser agent code 1004）**。三次 `open(65)` 均失败：`打开 profile 65失败：code=1004 message=Unknown internal error`（首轮、close 后重试、health 检查后 60 秒再试均同错）。`check(65)` 同样失败。`close(65)` 返回 code 1009 Process not found（本来就没开起来）。
- **环境核查**：agent 本身正常——`health` 返回 ok、ixbrowser-agent v10；`profiles` 列表共 46 个，gaga5456（profile 65）在列；`opened` 列表全程为空（0 个在开），无残留进程。故障只针对 65 号启动这一步，不是 agent 宕机、不是隧道断连（opened/health 均一次通过，默认环境代理，未覆盖 proxy-acct2.txt）。
- **与 11-19 Bertie（profile 35）残留状态不同**：Bertie 当时 close 再 open 即恢复；本轮 65 号 close 后重开仍 1004，三次均失败，未再硬闯。登录态未验证到（没打开就无法判断），**不是 226/344、不是已确认的登录失效**——不编结果。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：收件箱/Requests/通知均未读到，无法判断有无新私信/新关注；上一轮 08:12 收件箱与 Requests 均为空、通知无新增。
- **判定**：运行环境阻塞（ixBrowser 启动 65 号失败），需总管/用户侧处理——可能需在用户电脑上重启 ixBrowser agent 或检查 65 号浏览器进程/配置。下轮先看本问题是否已恢复再跑；若持续 1004，考虑重启 agent 后重试。
- **轮次结束 profile 65 未开着**（opened-after 为空列表，0 个在开），无需 close。

## 2026-11-20 14:13（窗口外跳过，job fb-dm-p65）

- 北京时间 14:13 不在夜里窗口（22:00–次日 06:00）内，按规定直接结束：未开浏览器、未发任何内容、未碰账号（profile 65 未打开）。
- 未读收件箱/通知，未发私信，无新回复可回，无客资，无致命问题。例行轮次，只写日志，不报用户。

## 2026-11-20 15:12（窗口外跳过，job fb-dm-p65）

- 北京时间 15:12 不在夜里窗口（22:00–次日 06:00）内，按规定直接结束：未开浏览器、未发任何内容、未碰账号（profile 65 未打开）。
- 未读收件箱/通知，未发私信，无新回复可回，无客资，无致命问题。例行轮次，只写日志，不报用户。

## 2026-11-20 16:12（窗口外跳过，job fb-dm-p65）

- 北京时间 16:12 不在夜里窗口（22:00–次日 06:00）内，按规定直接结束：未开浏览器、未发任何内容、未碰账号（profile 65 未打开）。
- 未读收件箱/通知，未发私信，无新回复可回，无客资，无致命问题。例行轮次，只写日志，不报用户。
2026-11-20 17:12 CST fb-dm-p65 gaga5456（profile 65）IG 私信盯守：窗口外（北京时间 22:00–次日 06:00）跳过，未开浏览器、未发内容、未碰账号。
## 2026-11-20 19:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12–08:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。**环境已恢复**：09:12 的 profile 65 启动 code 1004 与 10:12 的 ixBrowser Local API 不可达均已消失，open(65) 一次成功；轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-20 20:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12–19:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-20 18:12（窗口外跳过，job fb-dm-p65）

- 北京时间 18:12 不在夜里窗口（18:30–次日 06:00）内，按规定直接结束：未开浏览器、未发任何内容、未碰账号（profile 65 未打开）。
- 未读收件箱/通知，未发私信，无新回复可回，无客资，无致命问题。例行轮次，只写日志，不报用户。


## 2026-11-20 21:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12–20:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-20 22:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12–21:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。注：首轮脚本输出被 tail 截断头部，为补全核验证据又重跑一次只读核验，两次结果完全一致；两次均为只读检查，未发任何内容。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有其他并行轮次的号：首轮为 profile 32，复核轮为 profile 38）。

## 2026-11-20 23:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号（首轮与重试轮两次确认）。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 00:12–22:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输故障记录**：首轮通知页 eval 遇一次 curl 52（agent 空回复），属瞬时故障；重试轮（重开 profile）通知页正常读回，内容与前几轮一致。两次 close 均返回 closed:true，opened 列表复核确认 65 已关（opened-after 只有 profile 5、32，为其他并行轮次的号）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关。

## 2026-11-21 00:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 2、5、32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 2、5、32，为其他并行轮次的号）。

## 2026-11-21 01:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 5、44 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 5、32、44，为其他并行轮次的号）。

## 2026-11-21 03:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12、01:12、02:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 32、44 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-21 02:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12、01:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时在开的 profile 5、32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 5、32，为其他并行轮次的号）。

## 2026-11-21 04:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12、01:12、02:12、03:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-21 05:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12、01:12、02:12、03:12、04:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。轮开始时 opened 列表为空（0 个在开）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。
- 06:13 fb-dm-p65（gaga5456，profile 65）跳过：已过夜里窗口 18:30–06:00（当前 06:13 CST），未开浏览器、未发任何内容、未碰账号。
- 07:13 fb-dm-p65（gaga5456，profile 65）跳过：已过夜里窗口 18:30–06:00（当前 07:13 CST），未开浏览器、未发任何内容、未碰账号。
- 2026-11-21 08:13 CST fb-dm-p65（gaga5456 / profile 65）：窗口外跳过——当前 08:13 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。
- 2026-11-21 09:12 CST fb-dm-p65（gaga5456 / profile 65）：窗口外跳过——当前 09:12 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 05:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时 opened 列表为空（0 个在开）；轮末 profile 32 为其他并行轮次的号（05:13:30 打开），未碰。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。
--- fb-dm-p65 (gaga5456, IG p65) 2026-11-21 10:12 窗口外跳过：当前北京时间 10:12，不在 18:30–次日 06:00 窗口内，未开浏览器、未发内容、未碰账号。
2026-11-21 11:12 CST fb-dm-p65：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
2026-11-21 12:13 CST fb-dm-p65：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
2026-11-21 13:12 窗口外跳过（窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
## 2026-11-21 14:12 fb-dm-p65 跳过：当前时间在夜里窗口（18:30–次日 06:00）之外，本轮直接结束，未开浏览器、未发任何内容、未碰账号。
- 2026-11-21 15:12 CST fb-dm-p65（gaga5456，profile 65）轮次：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。

## 2026-11-21 17:12 CST — 跳过（窗口外）
- 本轮定时 17:12，夜里窗口为 18:30–次日 06:00，窗口外。未开浏览器、未发任何内容、未碰账号。

## 2026-11-21 18:12 CST — 跳过（窗口外）
- 本轮定时 18:12，夜里窗口为 18:30–次日 06:00，窗口外。未开浏览器、未发任何内容、未碰账号。

## 2026-11-21 19:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12–05:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-21 20:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12–19:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-21 21:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12–20:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时 opened 列表为空（0 个在开）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 00:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。注：首轮脚本输出被 tail 截断头部，为补全核验证据又重跑一次只读核验，两次结果完全一致；两次均为只读检查，未发任何内容。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（首轮 opened-after 为空；复核轮 opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-21 22:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20 各轮、11-21 00:12–21:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 2 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-21 23:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知页本轮未读到（不谎报“无新增”）**：`goto(notifications/)` 成功（title「Instagram」），但随后 eval 失败——`Page.evaluate: TypeError: Cannot read properties of null (reading 'innerText')`，系页面未加载完/瞬时故障。之后两次等待复核（约 23:18、23:21）均发现 profile 65 正被其他并行轮次占用（先后于 23:15:34、23:18:09、23:20:53 重新打开），为避免抢占他人标签页导航，未再重试读通知。`check(65)` 只读确认对方当前停在 facebook.com 默认登录页，未做任何导航或点击。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：收件箱与 Requests 均为空，无新回复可回；通知未读到，故新关注/新评论是否新增**无法判断**，不编结果。下轮优先补读通知页。
- **并行占用记录**：轮开始时 65 号已开着（23:13:26 打开，pid 42664，疑似另一并行轮次）；本轮 open 复用同一实例、close 后复核 opened-after 只剩 profile 32；随后 65 号于 23:15:34、23:18:09、23:20:53 三次被重新打开（不同 pid），并行工作自行恢复、未见中断报错。轮次结束时 65 号正由其他并行轮次使用（23:20:53 打开，pid 30392），**本次未再 close**，以免关掉他人实例。
- **传输**：本轮除通知页 eval 一次失败外未遇 curl 18/52/56（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。

## 2026-11-22 01:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 5、32 为其他并行轮次的号（5 在本轮进行中由其所属轮次自行关闭）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 02:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号（未动）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 03:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载，首页 feed 正常。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮、11-22 00:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时 65 未开（was_open False），本轮自开自关。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 04:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。
## 2026-11-22 06:13（窗口外跳过）
- 本轮定时触发于 06:12，已超出夜里窗口（18:30–次日 06:00），按任务要求直接结束：未开浏览器、未发任何内容、未碰账号。
- 无需核对身份/通知/收件箱；无新客资、无致命问题，例行跳过不报用户。
- 2026-11-22 08:13 CST fb-dm-p65：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-22 09:13 CST fb-dm-p65（gaga5456，profile 65）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-22 10:12 CST fb-dm-p65（gaga5456，profile 65）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-22 11:12 fb-dm-p65（gaga5456，IG profile 65）：窗口外（夜里窗口 18:30–次日 06:00），本轮跳过，未开浏览器、未发内容、未碰账号。
- 2026-11-22 12:12 fb-dm-p65（gaga5456，IG profile 65）：窗口外（夜里窗口 18:30–次日 06:00），本轮跳过，未开浏览器、未发内容、未碰账号。
- 2026-11-22 14:12 fb-dm-p65（gaga5456，IG profile 65）：窗口外（夜里窗口 18:30–次日 06:00），本轮跳过，未开浏览器、未发内容、未碰账号。

- 2026-11-22 15:12 CST fb-dm-p65（gaga5456，profile 65）轮次：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-22 16:12 CST fb-dm-p65（gaga5456，profile 65）轮次：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。

## 2026-11-22 17:13 跳过
窗口外跳过（夜里窗口 18:30–次日 06:00，当前 17:13），未开浏览器、未发任何内容、未碰账号。
- 2026-11-22 18:12 CST fb-dm-p65（gaga5456，profile 65）轮次：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。

## 2026-11-22 19:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21 各轮、11-22 05:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 20:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 05:12 各轮完全一致，无新关注、无新评论、无新私信通知。本月一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 21:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 05:12、19:12、20:12 各轮完全一致，无新关注、无新评论、无新私信通知。本月一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 5、32 为其他并行轮次的号（5 在本轮进行中由其所属轮次自行关闭）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32，为其他并行轮次的号）。

## 2026-11-22 22:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空（本轮读回确认）**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 本轮未读到**：两次尝试均失败——首轮 eval curl 18（transfer closed, 445 bytes remaining）、补核轮 eval 同样 curl 18（445 bytes remaining）；**不编结果**。上一轮 21:12（一小时前）读回确认 Requests 为空（Delete all 0，0 个线程）。
- **通知本轮未读到**：两次尝试均失败——首轮 goto curl 52、补核轮 goto curl 18（103 bytes remaining）；**不编结果**。上一轮 21:12 读回确认通知与此前各轮完全一致，无新关注、无新评论、无新私信通知（本周一条年龄确认提示 Nov 13；本月只有点赞——rezazes 连赞 5 条 Reel 11-08/09、eleanore.meyer.58 赞 1 条 11-07；均为纯点赞、无文字互动，不构成联系对象）。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：收件箱为空，无新回复可回；Requests/通知未读到，无法判断有无新增——下轮重读。
- **传输故障记录**：本轮 agent 间歇性无响应，curl 52（空回复）与 curl 18（传输截断）交替出现——首轮 open、requests eval、notifications goto、close、opened-after 均撞上；补核轮 requests eval、notifications goto 又撞上；第二次补核轮连 health 都 curl 52 失败；30 秒后复核 health 恢复正常（agent v10）。**不是 226/344、不是 429、不是已确认的登录失效**（登录已验证：收件箱页正常加载并显示本号用户名；agent 在故障间隙均正常响应）。属运行环境瞬时抖动，未硬闯、未盲重试超过三轮。
- **判定**：登录正常、无 226/344、无 429。例行轮次，只写日志，不报用户；Requests/通知未核验，留待下轮重读。
- 轮次结束 profile 65 已关：补核轮 close 返回 closed:true；30 秒后复核 opened 列表确认 65 不在其中（在开的 5、32、44、67 为其他并行轮次的号，未碰）。

## 2026-11-22 23:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程；首轮 eval 撞 curl 18 截断，重试后读回确认）。
- **通知本轮未读到**：三次 goto 尝试均失败——retry2 一次 curl 52、retry3 两次（curl 52、curl 18，103 bytes remaining）；**不编结果**。上次读回确认是 21:12 轮（与此前各轮完全一致，无新关注、无新评论、无新私信通知：本周一条年龄确认提示 Nov 13；本月只有点赞——rezazes 连赞 5 条 Reel 11-08/09、eleanore.meyer.58 赞 1 条 11-07；均为纯点赞、无文字互动，不构成联系对象）。通知留待下轮重读。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：收件箱与 Requests 均为空，无新回复可回；通知未读到，无法判断有无新增。
- **传输故障记录**：本轮 agent 间歇性无响应，curl 52（空回复）与 curl 18（传输截断）交替出现——首轮 health curl 52、第二轮 opened curl 18 + open curl 52（open 实际已在服务端执行，回复丢失）、retry2 三页 goto 全撞、retry3 通知 goto 两撞；间隙期 agent 均正常响应（health v10 正常、opened 列表正常）。**不是 226/344、不是 429、不是已确认的登录失效**（登录已验证：收件箱页正常加载并显示本号用户名）。属运行环境瞬时抖动，未硬闯；通知 goto 本轮共 3 次尝试后停手，未盲重试。
- **profile 65 状态说明**：65 号在本轮开始前已开着（opened 列表 open_time 22:49:04，pid 24892；22:12 轮已核验关闭，22:49 的打开者不明，疑似其他轮次/任务）。按手册「轮开始时已开的号本轮不 close」，本轮只读核查、未关闭 65（轮末 opened-after 确认 65 仍在，pid 未变）。另：retry2 中一次 close 尝试报 curl 52，经复核未生效、65 未被误关。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束 profile 65 未关闭（轮开始时已开，属其他轮次/任务的窗口，未碰）；在开的 5、35、38、44、67 为其他并行轮次的号，未碰。

## 2026-11-23 00:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康。
- **注意**：轮开始时 profile 65 已开着（`was_open=True`，opened 列表含 5、32、35、44、63 等其他并行轮次的号），按手册「别的轮次正在用，本轮不 open、不 close」，本轮只读核验后即走，**未 close(65)**，未碰其他号的窗口。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。

## 2026-11-23 01:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 5、32、35、44、63 为其他并行轮次的号。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 5、32、35、44、63，为其他并行轮次的号）。
- 原始记录：`~/workspace/fb-ip/dm_p65_round_20261123_0112.json`

## 2026-11-23 02:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时在开的 profile 32、35、44、63 为其他并行轮次的号，未碰。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32、35、44、63，为其他并行轮次的号）。

## 2026-11-23 03:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 各轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时 65 未开（was_open_before=false）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32、35、44、63，为其他并行轮次的号）。核验文件：`~/workspace/fb-ip/dm_p65_round_20261123_0312.json`。

## 2026-11-23 04:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 各轮、11-23 01:12、02:12、03:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时 65 未开（was_open_before=false）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32、35、44、63，为其他并行轮次的号）。核验文件：`~/workspace/fb-ip/dm_p65_round_20261123_0412.json`。

## 2026-11-23 05:12（本轮，job fb-dm-p65）

- **身份核验通过**：Direct 收件箱页眉显示用户名 `gaga5456`，即本号。（注：open 后 check() 默认页为 facebook.com 登录页，系该 profile 默认标签页；IG 各页均已登录态正常加载。）
- **Direct 收件箱为空**：`instagram.com/direct/inbox/` 显示「Chats will appear here after you send or receive a message」，0 个线程（页眉「First note in a while... / Your note」为 Notes 功能提示，非消息线程）。
- **Message Requests 也为空**（`direct/requests/`，Delete all 0，0 个线程）。
- **通知**：与 11-19 三轮及 11-20、11-21、11-22 各轮、11-23 01:12、02:12、03:12、04:12 轮完全一致，无新关注、无新评论、无新私信通知。本周一条年龄确认提示（"We weren't able to confirm your age"，Nov 13）；本月只有点赞——rezazes 连赞 5 条 Reel（11-08/09）、eleanore.meyer.58 赞 1 条（11-07）。rezazes/eleanore 均为纯点赞、无文字互动，不构成联系对象。通知页下方的「Suggested for you」仅为 IG 推荐关注列表，非关注请求，不跟随。
- **本轮未发任何私信、未通过任何好友、未筛查到新线程**：无新回复可回，无新关注可筛。
- **传输正常**：本轮未遇 curl 18/52/56，全程一次通过（默认环境代理，未覆盖 proxy-acct2.txt）。agent v10 健康；open(65) 一次成功。轮开始时 65 未开（was_open_before=false）。
- **判定**：登录正常、无 226/344、无 429、无致命问题。例行轮次，只写日志，不报用户。
- 轮次结束已 `close(65)` 关掉 profile，并经 opened 列表复核确认已关（opened-after 只有 profile 32、35、44、63，为其他并行轮次的号）。核验文件：`~/workspace/fb-ip/dm_p65_round_20261123_0512.json`。
- 2026-11-23 06:12 CST fb-dm-p65（gaga5456，profile 65）跳过：已过夜里窗口（18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-23 07:13 CST fb-dm-p65：窗口外跳过（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
## 2026-11-23 08:12 fb-dm-p65 窗口外跳过：北京时间 08:12 不在 18:30–次日 06:00 窗口内，未开浏览器、未发内容、未碰账号。

- 2026-11-23 09:12 CST fb-dm-p65（gaga5456 / profile 65）：窗口外跳过——当前 09:12 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。
