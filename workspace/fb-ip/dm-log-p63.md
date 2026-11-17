# 私信盯守台账 — elainaklocko（IG 面提线，profile 63）

## 2026-11-17 19:44–20:12 CST（fb-dm-p63 首轮，IG 首轮）

- 身份核验：登录正常，feed 正常。**实测用户名为 `elainaklocko_lily.02176`**（主页 h1 与导航个人资料链接一致，9 posts / 0 followers / 3 following，可见 Edit profile，确为本号），与手册写的 `elainaklocko` 不符——请总管核对：是否为同一账号改名/带后缀的完整 handle。按实测 handle 继续本轮，未发任何内容。
- Direct 收件箱（Primary）：只有 2 年前的旧群聊，无新 1:1 私信、无未读。旧群聊里有多条 2 年前本号发出的垃圾链接消息（"Free live cam girls…" 指向 imogen-289.devyn49620.buzz 等域名）——为账号接手前的历史记录，本轮未碰、未删、未回复；该号历史上有疑似被盗/群发垃圾记录，留待总管评估。
- Requests：空（0 条）。General 标签页本次点击未找到元素，未单独读到——Primary 已覆盖新 1:1 私信入口，Requests 为空，缺口记于此。
- 通知：仅一条系统通知（"You're now using a Meta Account on Instagram. Oct 19"）+ 一批 "Suggested for you" 推荐关注（均为旧群聊圈子的人，非新关注/新互动），无新关注、无新评论/点赞通知，无需处理、未关注任何人。
- 新回复：无。本轮未发任何私信，无需 E07、无需送达核验。
- 异常：无 429、无 226/344。首轮曾遇到 `check()` 读到 facebook.com 登录页（与实际 tab 不符，疑为 check 读了另一 tab/重定向残影），后以 tabs + eval 直读 URL 确认实际在 IG 且已登录；另一次点击 Requests 标签误跳 /explore/，改用 /direct/requests/ 直达后读到空列表。均已记日志，不硬闯。
- 轮次结束：profile 63 已关闭（closed: true）。
- 合格客资：0。致命问题：无。本轮不报用户。

## 2026-11-17 20:14–20:44 CST（fb-dm-p63 第二轮）

- 身份核验：登录正常。导航个人资料链接为 `/elainaklocko_lily.02176/`，与首轮实测一致（手册写的 `elainaklocko` 仍不符，待总管核对）；feed 正常，未发任何内容。
- Direct 收件箱（Primary）：针对性重读确认——只有 2 年前的旧群聊（Marco Pires 等、Deleon Sisters 等、Sri Idima Denis 等，含 2 年前本号发出的垃圾链接旧消息，未碰），无新 1:1 私信、无未读。第一次读到的正文是信息流帖子内容（页面未切到收件箱视图），已用 `/direct/t/` 选择器重读核实，非收件箱有新消息。
- Requests：本轮未读到——agent 连续空回复（curl 52/18），两次尝试均失败；首轮（28 分钟前）Requests 为空，本轮 Primary 无新线程，缺口记于此，下轮优先补读。
- 通知：仅一条系统通知（"You're now using a Meta Account on Instagram. Oct 19"）+ "Suggested for you" 推荐关注，无新关注、无新评论/点赞通知，无需处理、未关注任何人。
- 新回复：无。本轮未发任何私信，无需 E07、无需送达核验。
- 异常：无 429、无 226/344。`check()` 再次读到 facebook.com 登录页（与首轮相同，check 读的是另一 tab 的残影，IG tab 实际已登录，非登录失效）。**ixBrowser agent 在本轮后半段频繁空回复**：/eval、/goto、/close、/opened 多次报 curl 52（Empty reply）/ curl 18（transfer closed），疑似 agent 或隧道不稳；close 连续两次回包丢失，但随后 `opened()` 第二次尝试成功，确认 profile 63 已不在打开列表（p63_still_open: false）。关 profile 只用 `opened()` 核对，未对已关的号调 `check()`（按 AGENTS.md 新教训）。
- 轮次结束：profile 63 已确认关闭（opened 列表：1、5、32、38、44、67、80，无 63）。
- 合格客资：0。致命问题：无。本轮不报用户。

## 2026-11-17 20:44–21:00 CST（fb-dm-p63 第三轮）

- 身份核验：登录正常。导航个人资料链接为 `/elainaklocko_lily.02176/`，与前两轮实测一致（手册写的 `elainaklocko` 仍不符，待总管核对）；feed 正常，未发任何内容。
- Direct 收件箱（Primary）：只有 2 年前的旧群聊（Marco Pires 等、Deleon Sisters 等、Sri Idima Denis 等，含 2 年前本号发出的垃圾链接旧消息，未碰），无新 1:1 私信、无未读。
- Requests：本轮成功读到——空（0 条），"Chats will appear here after you send or receive a message"。补上第二轮因 agent 空回复未读到的缺口。
- 通知：仅一条系统通知（"You're now using a Meta Account on Instagram. Oct 19"）+ "Suggested for you" 推荐关注，无新关注、无新评论/点赞通知，无需处理、未关注任何人。
- 新回复：无。本轮未发任何私信，无需 E07、无需送达核验。
- 异常：无 429、无 226/344。`check()` 本轮未调用（按 AGENTS.md 教训，关 profile 只用 `opened()` 核对）。agent 本轮响应较慢（整轮脚本约 4.8 分钟），但各步均成功、无 curl 52/18。
- 轮次结束：profile 63 已确认关闭——两次 close 均回 ok:true，但第一次 close 后 `opened()` 仍列出 63（列表滞后）；等 25 秒后复核，opened 列表为 1、5、32、38、43、44、67、80，无 63。
- 合格客资：0。致命问题：无。本轮不报用户。
