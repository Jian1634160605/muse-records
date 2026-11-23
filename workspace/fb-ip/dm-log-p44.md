# 私信盯守台账 — sarahcook6809（IG 面提线，profile 44）
## 2026-11-17 19:41 轮次（IG 首轮）

- 身份核验：通过。登录态正常，个人资料链接 `/sarahcook6809/`，主页显示 sarahcook6809 / Dr. Qin Hao，0 帖子、6 粉丝、15 关注。Feed 正常加载。
- 通知（instagram.com/notifications/）：本周/月内 6 个新关注，全部仅为“started following you”，无评论、无私信、无医美意向信号：
  - shyam_ka_ladla_202（5 天前）
  - ashishbdbshd（11-09）
  - pk_sona_love（11-06）
  - rahul2389977（11-04）
  - chameleon.951509（11-02，已回关；其 Note 为歌词，非私信）
  - bym_esteticaterapiasbcn（10-30，巴塞罗那美容机构号，同行/机构，已回关，不联系）
  - 处置：均不联系、不盲目回关。无真人个人号+医美意向的组合，不符合首条私信条件。
  - 另见一条 10-12 旧安全提示（“未识别设备尝试更改敏感设置”），为历史通知，本轮登录正常，不作升级。
- Direct 收件箱（instagram.com/direct/inbox/）：Primary、General、Requests 三栏全部为空（“Chats will appear here after you send or receive a message”；Requests 为 0）。无新私信、无待回复。
- 本轮动作：无发信。无合格客资，无致命问题。
- 备注：直接 goto /direct/inbox/ 后页面会先跳走（一次跳到个人主页、一次跳到通知页），改从首页点 Messages 链接进入收件箱可稳定停留；Requests 需点文字切换。账号 0 帖子，内容发布走另外流程。
- 轮次结束已关 profile 44。

## 2026-11-17 20:11 轮次

- 身份核验：通过。Direct 收件箱顶部显示 sarahcook6809；通知列表与 19:41 轮一致（同批 6 个新关注），IG 登录态正常。
- 通知（instagram.com/notifications/）：自 19:41 轮起无新增。仍是同一批 6 个仅“started following you”的关注，无评论、无私信、无医美意向信号，不联系。
- Direct 收件箱 Primary：为空（“Chats will appear here after you send or receive a message”），无新私信、无待回复。
- Direct Requests / General：**本轮未核验到**。点“Requests”文字超时 15 秒未找到可见元素，随后页面漂移到一条 IG 帖子（/p/DeLrpausQ85/，nurse.sarahlouise 的拉皮讨论帖，未做任何评论/互动）；再点“General”同样超时，页面又漂到 facebook.com 登录页。按手册不硬闯，记日志。上一轮（19:41）Requests 为 0，本轮 Primary 为空，30 分钟内新请求概率低，但 Requests 未读回即为未核验，下轮优先复查。
- 另见：check 步骤默认标签页落在 facebook.com 登录页（account_name 为空），属 profile 44 默认标签页状态；IG 侧登录正常，不作登录失效升级。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-17 20:41 轮次（首跑 agent 故障 + 重试成功）

- 首跑：health/open/check/goto-home 正常，但随后 identity、通知、收件箱等连续 7 个调用全部 curl 52 空回复（ixBrowser agent 端瞬时故障，非平台 429/226/344）；末段 agent 自行恢复，req-text/gen-text 读到的是首页 feed、close 成功。首跑**未核验到任何有效内容**，按手册不硬闯、不谎报，立即按恢复口径重试一次（open 后等 45 秒再导航）。
- 重试：全部一次成功。
  - 身份核验：通过。导航栏含本号个人资料链接 `/sarahcook6809/`，IG 登录态正常。
  - 通知（instagram.com/notifications/）：自 20:11 轮起**无新增**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 5 天前、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无评论、无私信、无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，本轮登录正常，不作升级。
  - Direct 收件箱 Primary：为空（“Chats will appear here after you send or receive a message”），无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
  - Direct Requests：**本轮已核验，0 条**（“Delete all 0”），补上 20:11 轮的缺口。
  - Direct General：**本轮仍未核验到**。Requests 页上点“General”文字未找到可点元素（clicked:false），页面仍停留在 Requests。收件箱全站无任何对话（Primary 空、Requests 0），General 栏无对话可藏，但未读回即记为未核验，下轮优先用直接 goto /direct/general/ 方式复查。
- 本轮动作：无发信。无合格客资，无致命问题（首跑的 curl 52 是 agent 传输层瞬时故障，重试后全部恢复，登录态完好，不作封号/登录失效升级）。
- 轮次结束已关 profile 44。

## 2026-11-19 21:00 轮次（fb-dm-p44）

- 首跑失败原因（已查明，非平台问题）：我误用 `~/.agent-reach/proxy-acct2.txt` 覆盖了 HTTPS_PROXY，导致 health 超时 170s、其后全部调用 curl 56 Connection reset；改用默认环境 HTTPS_PROXY 后 health 立即恢复（agent v10）。教训：本任务不要覆盖默认代理。
- 重试：全部一次成功。
  - 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
  - 通知（instagram.com/notifications/）：自 11-17 轮起无新增关注，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
  - 通知新增 3 条本号帖子评论，均为矩阵内号的互刷评论，非客户，无需私信回复：elainaklocko_lily.02176（2h 前，问拉皮费用）、gaga5456（6h 前，问如何约视频面诊）、elainaklocko_lily.02176（6h 前，问面诊费用）。属 11-19 互刷轮次已完成动作。
  - Direct 收件箱 Primary：为空，无新私信、无待回复。
  - Direct Requests：已核验，0 条（“Delete all 0”）。
  - Direct General：**本轮已核验到，为空**（直接 goto /direct/general/ 成功，补上 11-17 两轮的缺口；点“General”文字仍点不到，页面停在 Requests，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-19 22:00 轮次（fb-dm-p44）

- agent 传输层瞬时故障（非平台信号）：`open` 两次失败（curl 18、curl 52），但随后 goto-home 一次成功，说明 profile 实际已打开；中途 identity、click-general 各一次 curl 18/52，重试后均恢复。无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`；Direct 收件箱顶部显示 sarahcook6809，登录态正常。
- 通知（instagram.com/notifications/）：自 21:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（9 分钟前，聊翻修鼻子）、elainaklocko_lily.02176（3 小时前，问拉皮费用）、gaga5456（7 小时前，问如何约视频面诊）、elainaklocko_lily.02176（7 小时前，问面诊费用）。属 11-19 互刷轮次动作。
- Direct 收件箱 Primary：为空，无新私信、无待回复。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-19 23:00 轮次（fb-dm-p44）

- agent 传输层瞬时故障（非平台信号）：轮次开始时 health 连续 3 次 curl 52 空回复，等待 60 秒后重试一次即恢复（agent v10）；其后 open 及全部步骤一次成功。无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 22:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（1 小时前，聊鼻子翻修）、elainaklocko_lily.02176（4 小时前，问拉皮费用）、gaga5456（8 小时前，问如何约视频面诊）、elainaklocko_lily.02176（8 小时前，问面诊费用）。属 11-19 互刷轮次动作。
- Direct 收件箱 Primary：为空，无新私信、无待回复。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 00:00 轮次（fb-dm-p44）

- agent 传输层瞬时故障（非平台信号）：health 一次 curl 52、open 两次 curl 52 失败，但其后 goto-home 一次成功，说明 profile 44 实际已打开（open 报错为空回复，profile 本身已开）；中途 identity 一次 curl 18、goto-home2 两次 curl 52，重试后均恢复。无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 23:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（2 小时前，聊鼻子翻修）、elainaklocko_lily.02176（5 小时前，问拉皮费用）、gaga5456（9 小时前，问如何约视频面诊）、elainaklocko_lily.02176（9 小时前，问面诊费用）。属 11-19 互刷轮次动作。
- Direct 收件箱 Primary：为空，无新私信、无待回复。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 02:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 01:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（4 小时前，聊翻修鼻子）、elainaklocko_lily.02176（7 小时前，问拉皮费用）、gaga5456（11 小时前，问如何约视频面诊）、elainaklocko_lily.02176（11 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 01:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 01:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 00:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（3 小时前，聊鼻子翻修）、elainaklocko_lily.02176（6 小时前，问拉皮费用）、gaga5456（10 小时前，问如何约视频面诊）、elainaklocko_lily.02176（10 小时前，问面诊费用）。属 11-19 互刷轮次动作。
- Direct 收件箱 Primary：为空，无新私信、无待回复。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 03:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 02:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（5 小时前，聊翻修鼻子）、elainaklocko_lily.02176（8 小时前，问拉皮费用）、gaga5456（12 小时前，问如何约视频面诊）、elainaklocko_lily.02176（12 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 02:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 04:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 03:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（6 小时前，聊翻修鼻子）、elainaklocko_lily.02176（9 小时前，问拉皮费用）、gaga5456（13 小时前，问如何约视频面诊）、elainaklocko_lily.02176（13 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 03:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 06:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 05:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（8 小时前，聊翻修鼻子）、elainaklocko_lily.02176（11 小时前，问拉皮费用）、gaga5456（15 小时前，问如何约视频面诊）、elainaklocko_lily.02176（15 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 05:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 05:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 04:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（7 小时前，聊翻修鼻子）、elainaklocko_lily.02176（10 小时前，问拉皮费用）、gaga5456（14 小时前，问如何约视频面诊）、elainaklocko_lily.02176（14 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 04:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44。

## 2026-11-20 07:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 06:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（9 小时前，聊翻修鼻子）、elainaklocko_lily.02176（12 小时前，问拉皮费用）、gaga5456（16 小时前，问如何约视频面诊）、elainaklocko_lily.02176（16 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 06:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（opened() 复核为空）。

## 2026-11-20 08:00 轮次（fb-dm-p44）

- 首跑脚本被服务重启打断：open 已成功（profile 44 于 07:58:12 打开），后续步骤未跑；重启后先查 opened() 确认 profile 已开，再用不含 open 的续跑脚本完成全部步骤，无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 07:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（10 小时前，聊翻修鼻子）、elainaklocko_lily.02176（13 小时前，问拉皮费用）、gaga5456（17 小时前，问如何约视频面诊）、elainaklocko_lily.02176（17 小时前，问面诊费用）。属 11-19 互刷轮次动作，与 07:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（opened() 复核为空）。

## 2026-11-20 09:00 轮次（fb-dm-p44）——本轮未跑成：profile 44 打不开

- 异常：ixBrowser agent 本身健康（health OK，v10，探查 <3s 即回），但 `open(44)` 连续失败：`code=1004 message=Unknown internal error`（12s 快败）；先 `close(44)` 再重开仍同错，`close` 报 `code=1009 Process not found`（本来就没打开）。与今早 08:36 p5（Jusa）轮次同款故障——agent 侧打不开指定 profile 的内部错误，非 IG/FB 平台信号，未撞 429/226/344，不作封号/登录失效升级。
- 首跑脚本另有教训：本轮脚本经 `| tail -40` 管道执行，中间输出要等脚本结束才可见，两次等到 10 分钟以上仍零输出才停掉——表象像挂住，实为输出被管道吞掉 + open 失败后各步重试拉长耗时。下次跑轮次脚本不用 tail 管道，或直接重定向到日志文件。
- 通知 / 收件箱 / Requests / General：均未读到（profile 未打开，无页面可读）。**本轮无法确认有无新回复——不是“无新回复”，是“未读到”，不谎报。**08:00 轮的已知状态（6 个旧关注、无新私信、互刷评论 4 条）不拿来顶替本轮。
- 动作：无发出消息。profile 44 本就未打开，无需 close；opened() 复核为空。
- 处理：按手册“读不到记日志、报总管”——留待总管决定是否等 agent 恢复后补跑本轮，或检查 profile 44 环境本身（是否残留进程/占用）。同日 p5 08:36 同款 1004 故障已在案，疑似 agent 侧间歇性打不开个别 profile（p63 08:06、p65 08:12 同日正常打开）。
- 合格客资：无（未读到）。致命问题：无（agent 内部错误，非账号封禁/登录失效）。本轮不报用户。

## 2026-11-20 10:00 轮次（fb-dm-p44）——本轮未跑成：ixBrowser Local API 失联

- 首跑：agent 本身健康（health OK，v10）。`open(44)` 一次成功（debugging 127.0.0.1:18385），但随后全部步骤失败：先是 goto/eval 连撞 curl 52 空回复，随后报错变为连不上用户电脑上的 ixBrowser Local API（http://127.0.0.1:53200/api/v2/，ConnectTimeout）——agent 与 ixBrowser 客户端之间的本地通道断了，不是 IG/FB 平台信号。identity、通知、收件箱、Requests、General 全部未读到；close 与 opened() 同样失败，**无法确认 profile 44 是否还开着**（首跑 open 成功后失联，close 未成功）。
- 重试（首跑结束后约 15 分钟）：opened-before 与 open(44) 3 次重试仍报同一 Local API ConnectTimeout，确认故障未恢复；为避免无意义地反复撞死接口，提前停掉了重试脚本（剩余步骤只会报同一错误，不再提供新证据）。未撞 429/226/344。
- 横向对照：今早 p63 09:06 轮 open 1004 两次、第三次成功；p65 09:12 轮 open 1004 三次失败；p5 09:36 轮全程正常。Local API 失联是本轮新出现的更深一层故障（前几轮 Local API 均可达），疑似用户电脑上的 ixBrowser 客户端崩溃/退出或 Local API 开关异常，需总管决定是否让用户在电脑上重启 ixBrowser 客户端或检查 Local API 设置。
- 通知 / 收件箱 / Requests / General：均未读到。**本轮无法确认有无新回复——不是“无新回复”，是“未读到”，不谎报。**08:00 轮的已知状态（6 个旧关注、无新私信、互刷评论 4 条）不拿来顶替本轮。
- 动作：无发出消息。profile 44 状态未知（open 成功、close 失败、opened() 读不到），留待总管/下轮复核。
- 合格客资：无（未读到）。致命问题：无已确认的封号/登录失效（登录态从未验证到，属环境阻塞，非账号问题）。按手册记日志留待总管处理；本轮不报用户。
2026-11-20 13:57 fb-dm-p44：窗口外跳过（夜里窗口 22:00–06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-20 14:57 CST fb-dm-p44（sarahcook6809，profile 44）跳过：窗口外（夜里窗口 22:00–次日 06:00），未开浏览器、未发任何内容、未碰账号。
- 2026-11-20 15:57 CST fb-dm-p44 跳过：窗口外（夜里窗口 22:00–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-20 16:57 CST fb-dm-p44（sarahcook6809，IG profile 44）轮次跳过：未到夜里窗口 22:00–06:00，按成安定只写日志，未开浏览器、未发内容、未碰账号。
## 2026-11-20 17:57 CST — fb-dm-p44 (sarahcook6809 / profile 44) 跳过：当前时间在夜里窗口（18:30–次日 06:00）之外，本轮未开浏览器、未发任何内容、未碰账号。

## 2026-11-20 19:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。**agent 已恢复**：09:00 轮 open 1004、10:00 轮 Local API 失联之后，本轮 health 一次 OK（agent v10）、open 一次成功（debugging 127.0.0.1:11931），为 08:00 轮后首个完整跑通的轮次。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 08:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（21 小时前，聊翻修鼻子）、elainaklocko_lily.02176（1 天前，问拉皮费用）、gaga5456（1 天前，问如何约视频面诊）、elainaklocko_lily.02176（1 天前，问面诊费用）。属 11-19 互刷轮次动作，与 08:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；紧随其后的 opened() 仍列出该 profile 系列表滞后，20 秒后复核 opened() 为空）。

## 2026-11-20 20:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（19:00 轮后第二个完整跑通的轮次）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 19:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（22 小时前，聊翻修鼻子）、elainaklocko_lily.02176（1 天前，问拉皮费用）、gaga5456（1 天前，问如何约视频面诊）、elainaklocko_lily.02176（1 天前，问面诊费用）。属 11-19 互刷轮次动作，与 19:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；20 秒后复核 opened() 为空）。

## 2026-11-20 21:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（19:00、20:00 轮后第三个完整跑通的轮次）。轮次开始时 opened() 显示 profile 35（Bertie，另一轮次在跑）已开，与本轮无关，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 20:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（23 小时前，聊翻修鼻子）、elainaklocko_lily.02176（1 天前，问拉皮费用）、gaga5456（1 天前，问如何约视频面诊）、elainaklocko_lily.02176（1 天前，问面诊费用）。属 11-19 互刷轮次动作，与 20:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-20 22:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（19:00、20:00、21:00 轮后第四个完整跑通的轮次）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 21:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（1 天前，聊翻修鼻子）、elainaklocko_lily.02176（1 天前，问拉皮费用）、gaga5456（1 天前，问如何约视频面诊）、elainaklocko_lily.02176（1 天前，问面诊费用）。属 11-19 互刷轮次动作，与 21:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；20 秒后复核 opened() 仅剩 profile 2（Victoria，另一轮次在跑），本号已关）。

## 2026-11-20 23:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（19:00、20:00、21:00、22:00 轮后第五个完整跑通的轮次）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 22:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 4 条本号帖子评论，**均为矩阵内号的互刷评论，非客户**，无需私信回复：gaga5456 回复了 sarah 在 gaga 帖子下的评论（1 天前，聊翻修鼻子）、elainaklocko_lily.02176（1 天前，问拉皮费用）、gaga5456（1 天前，问如何约视频面诊）、elainaklocko_lily.02176（1 天前，问面诊费用）。属 11-19 互刷轮次动作，与 22:00 轮同一批，仅时间推移。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 00:00 轮次（fb-dm-p44）

- agent 传输层瞬时故障（非平台信号）：轮次开始时 health、opened-before、open 连续 curl 52 空回复（各 2 次重试均失败）；但其后 goto-home 一次成功，说明 profile 44 实际已打开（open 报错为空回复，profile 本身已开，与 11-19 22:00、11-20 00:00 轮同款）；中途 click-requests、req-text、gen-text 各一次 curl 18，重试后均恢复。无 429/226/344，不作封号/登录失效升级。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 23:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增 1 条**非矩阵号真人评论回复（首见）**：deb_broadway 17 分钟前回复了 sarah 在 anatomyofthesoul.11 帖子下的评论：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——在聊拉皮恢复期占用假期，属真实意向信号（在考虑拉皮、担心恢复时间）。本轮为私信盯守，评论回复属猎手动作且须先过 E07，本轮未发评论、未私信她；已记入台账，留待猎手轮次跟进（先核她主页身份再回评）。其余 4 条本号帖子评论仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，1 天前），无需私信回复。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 01:00 轮次（fb-dm-p44）

- agent 传输层瞬时故障（非平台信号）：click-messages 步骤一次 curl 28 超时 170s，重试后一次成功；其余全部一次成功。无 429/226/344，不作封号/登录失效升级。轮次开始时 opened() 显示 profile 5（Jusa，另一轮次在跑）已开，与本轮无关，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 00:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知顶部仍是 deb_broadway 回复 sarah 在 anatomyofthesoul.11 帖子下评论的那条（现为 1 小时前，与 00:00 轮同一条，仅时间推移）：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——真实意向信号，属猎手动作（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余 4 条本号帖子评论仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，1 天前），无需私信回复。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核仅剩 profile 5、67，均为其他轮次在跑，本号已关）。

## 2026-11-21 02:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（19:00–01:00 轮后第七个完整跑通的轮次）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 01:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知顶部仍是 deb_broadway 回复 sarah 在 anatomyofthesoul.11 帖子下评论的那条（现为 2 小时前，与 01:00 轮同一条，仅时间推移）：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——真实意向信号，属猎手动作（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余 4 条本号帖子评论仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，1 天前），无需私信回复。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 03:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（19:00–02:00 轮后第八个完整跑通的轮次）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 02:00 轮起**无新增关注**，仍是同一批 6 个仅“started following you”的关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号），无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知顶部仍是 deb_broadway 回复 sarah 在 anatomyofthesoul.11 帖子下评论的那条（现为 3 小时前，与 02:00 轮同一条，仅时间推移）：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——真实意向信号，属猎手动作（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余 4 条本号帖子评论仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，1 天前），无需私信回复。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：**本轮未核验到**。点“General”文字仍点不到（clicked:false，老问题）；直接 goto /direct/general/ 返回 ok，但随后的 gen-text2 读到的是首页 feed（url 已跳回 instagram.com/，len 1385），页面未停留在 General 收件箱。Primary 为空、Requests 0，General 藏对话概率低，但未读回即记为未核验，下轮优先复查（与 11-17 20:11 轮同款缺口口径）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 关 profile 异常（需总管留意）：轮次脚本末尾 close 返回 closed:true，但紧随其后的 opened() 仍列出 profile 44（pid 33664，端口 19590，open_time 03:00:23）；随后又调一次 close（仍 closed:true），20 秒后复核 opened() 仍在列，但 pid/端口/open_time 全变了（pid 20292，端口 24959，open_time 03:01:06）；再隔 20 秒复核仍是这一条。两次 close 均报成功、opened() 却持续列出且身份每次不同，像 agent 侧列表滞后/残留，而非真实浏览器未关（真实浏览器 close 后 pid 不会变）。按手册不盲目反复 close、不调 check()（check 会拉起已关的 profile），记日志留待总管复核；本轮未再发任何内容。

## 2026-11-21 04:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 03:00 轮起**无新增关注**——通知顶部仍是 deb_broadway 回复 sarah 在 anatomyofthesoul.11 帖子下评论的那条（现为 4 小时前，与 03:00 轮同一条，仅时间推移）：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——真实意向信号，属猎手动作（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她；其下为 gaga5456 昨日回复（矩阵内号互刷）。通知文本读回截断于 4000 字符，旧的 6 个仅“started following you”关注未在本轮读回中逐一重现，但新增内容只会出现在顶部，顶部无新关注，即无新增。旧系统提示为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：**本轮已核验到，为空**（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”，补上 03:00 轮的缺口）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。03:00 轮的 close 后 opened() 仍列出且身份变化的异常本轮未再现。

## 2026-11-21 05:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 04:00 轮起**无新增关注**——通知顶部仍是 deb_broadway 回复 sarah 在 anatomyofthesoul.11 帖子下评论的那条（现为 5 小时前，与 04:00 轮同一条，仅时间推移）：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——真实意向信号，属猎手动作（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她；其下为 gaga5456 昨日回复（矩阵内号互刷）。通知文本读回截断于约 400 字符（脚本打印截断），旧的 6 个仅“started following you”关注未在本轮读回中逐一重现，但新增内容只会出现在顶部，顶部无新关注，即无新增。旧系统提示为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 06:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。轮次开始时 opened() 为空。本轮 05:58 启动（窗口 18:30–06:00 内），close 与 opened-after 复核落在 06:00 之后，属同一轮次收尾。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 05:00 轮起**无新增**。列表顶部仍是 deb_broadway 回复 sarah 在 anatomyofthesoul.11 帖子下评论的那条（现为 6 小时前，与 05:00 轮同一条，仅时间推移）：“@sarahcook6809 I have three weeks of vacation per year so using two weeks for a lift is a lot.”——真实意向信号，属猎手动作（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其后为 Yesterday 的 gaga5456 互刷回复。通知文本日志截断为前约 400 字（与 05:00 轮同口径），新增与否以列表顶部为准：顶部无 05:00 轮后的新项，6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功；点“General”文字仍点不到，改走直接 goto 可稳定核验）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 06:57 CST（fb-dm-p44 定时轮次）
- 窗口外跳过：本轮定于 07:00，夜里窗口为 18:30–次日 06:00，当前 06:57 已出窗口。按任务口径直接结束：未开浏览器、未发任何内容、未碰账号。
- 无合格客资，无致命问题，无需上报。

## 2026-11-21 08:00 CST（fb-dm-p44 定时轮次）
- 窗口外跳过：本轮定于 08:00，夜里窗口为 18:30–次日 06:00，当前 07:57 已出窗口。按任务口径直接结束：未开浏览器、未发任何内容、未碰账号。
- 无合格客资，无致命问题，无需上报。

## 2026-11-21 08:57 CST — fb-dm-p44 (sarahcook6809 / profile 44) 跳过：当前时间在夜里窗口（18:30–次日 06:00）之外，本轮未开浏览器、未发任何内容、未碰账号。

## 2026-11-21 10:00 CST（fb-dm-p44 定时轮次）
- 窗口外跳过：本轮定于 10:00，夜里窗口为 18:30–次日 06:00，当前 09:57 已出窗口。按任务口径直接结束：未开浏览器、未发任何内容、未碰账号。
- 无合格客资，无致命问题，无需上报。
- 2026-11-21 10:57 CST fb-dm-p44（sarahcook6809 / profile 44）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。

- 2026-11-21 12:00 CST 跳过：窗口外（本轮窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-21 12:57 CST fb-dm-p44（sarahcook6809 / profile 44）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-21 13:57 CST fb-dm-p44（sarahcook6809 / profile 44）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
## 2026-11-21 15:00 CST fb-dm-p44 跳过：当前时间在夜里窗口（18:30–次日 06:00）之外，本轮直接结束，未开浏览器、未发任何内容、未碰账号。
## 2026-11-21 15:57 — 窗口外跳过：当前时间在夜里窗口（18:30–次日 06:00）之外，本轮未跑，未开浏览器、未发内容、未碰账号。
- 2026-11-21 16:57 CST fb-dm-p44（sarahcook6809 / profile 44）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。
- 2026-11-21 17:57 CST fb-dm-p44（sarahcook6809 / profile 44）跳过：窗口外（夜里窗口 18:30–次日 06:00），未开浏览器、未发内容、未碰账号。

## 2026-11-21 19:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 06:00 轮起**新增 1 个关注**：ahmed.wakib.79，5 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系（同前几轮 6 个旧关注的处置口径；不确定身份先记下来，不盲目通过/回关）。其余新增为评论互动：anatomyofthesoul.11 7 小时前点赞了 sarah 回复 deb_broadway 的评论（“The work question is exactly what kept me going back and forth too, Deborah — wanting the lift is o...”），并回复了 sarah 在其帖子下的评论——属评论区互动、猎手动作范畴（须先过 E07、核对方主页身份再回评），本轮为私信盯守，未发评论、未私信，留待猎手轮次跟进。通知文本日志截断为前约 400 字（与 05:00/06:00 轮同口径），新增与否以列表顶部为准：顶部除上述两项外无其他新项；6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 20:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 19:00 轮起**无新增关注**。19:00 轮新增的 ahmed.wakib.79（现为 6 小时前）仍仅“started following you”，无评论、无私信、无医美意向信号，不联系（推荐栏显示其为 Ahmed Wakib、被 pk_sona_love 关注，无医美信号）。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 通知新增评论区互动（均为 anatomyofthesoul.11 帖子下的评论串，非私信，属猎手动作范畴，本轮未发评论、未私信，留待猎手轮次跟进）：
  - anatomyofthesoul.11 8 小时前点赞了 sarah 回复 deb_broadway 的评论，并回复了 sarah 在其帖子下的评论：“a bit of both but we are a hospitality business with a lot of staff so not easy to hide!!”（在聊术后藏不住、同事会发现，恢复期顾虑的延续）。
  - anatomyofthesoul.11 8 小时前另点赞了 sarah 回复 deb_broadway 的另一条评论。
  - deb_broadway 9 小时前回复了 sarah 在 anatomyofthesoul.11 帖子下的评论：“it’s 100% in person.”（接她“假期不够用两周做拉皮”的顾虑，说明其工作须全程到岗）。
  - deb_broadway 那条“three weeks of vacation per year so using two weeks for a lift is a lot.”现为 20 小时前，与 00:00–06:00 轮同一条，仅时间推移。——deb_broadway 仍为真实意向信号（在考虑拉皮、担心恢复时间占用假期），但私信盯守不主动私信未发过私信的评论者；猎手跟进须先过 E07、核她主页身份再回评。
  - 其余仍为矩阵内号互刷（gaga5456 1 天前回复 sarah 在其帖子下的评论、elainaklocko_lily.02176 与 gaga5456 各 2 条 2 天前评论），无需私信回复。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 21:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 20:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 20:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 7 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 9 小时前点赞 sarah 回复 deb_broadway 的评论、anatomyofthesoul.11 回复 sarah 在其帖子下的评论。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。通知文本日志截断为前约 400 字（与 05:00/06:00/19:00 轮同口径），新增与否以列表顶部为准：顶部无 20:00 轮后的新项。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-21 22:00 轮次（fb-dm-p44）

- 全程无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 21:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 21:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 8 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 10 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论、deb_broadway 11 小时前回复“it’s 100% in person.”、deb_broadway 那条“three weeks of vacation per year so using two weeks for a lift is a lot.”现为 22 小时前。deb_broadway 的意向信号仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：**本轮经补跑核验，为空**，无新私信、无待回复。首跑时从首页点 Messages 链接连续 3 次点击超时（`a[href="/direct/inbox/"]` 定位器能解析但 click 15 秒超时，疑似侧边栏元素不可点），改走直接 goto /direct/inbox/ 一次成功，页面稳定停留、两次读回均为“Chats will appear here after you send or receive a message”空态。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：**本轮经补跑核验，0 条**（直接 goto /direct/requests/ 成功，“Delete all 0”）。
- Direct General：**本轮经补跑核验，为空**（直接 goto /direct/general/ 成功，页面停留收件箱、显示空态；首跑时 5 秒等待后读回仅有用户名、系页面未加载完，补跑 10 秒等待后读回完整空态）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（两次 open/close 均 closed:true；opened() 复核仅剩 profile 2（Victoria，另一轮次在跑），本号已关）。

## 2026-11-21 23:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 22:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 22:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 9 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 11 小时前点赞 sarah 回复 deb_broadway 的评论、anatomyofthesoul.11 回复 sarah 在其帖子下的评论。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：**本轮未核验到**。直接 goto /direct/general/ 返回 ok，但随后 gen-text 首次读回报 `TypeError: Cannot read properties of null (reading 'innerText')`（页面跳转瞬间未就绪），重试后读回的是首页 feed（url 已跳回 instagram.com/），页面未停留在 General 收件箱。与 11-21 03:00 轮同款缺口口径。Primary 为空、Requests 0，General 藏对话概率低，但未读回即记为未核验，下轮优先复查。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 00:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 23:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 23:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 10 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 12 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：**本轮已核验到，为空**（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”；补上 23:00 轮的缺口——本轮 gen-text 首次读回即成功，未触发重试逻辑）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 01:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 仅有 profile 63（elaina，另一轮次在跑），与本轮无关，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常（innerText 片段未含用户名系页面加载片段所致，profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/）：自 00:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 00:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 11 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 13 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核仅剩 profile 63（elaina，另一轮次在跑），本号已关）。

## 2026-11-22 02:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 01:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 01:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 12 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 14 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论、deb_broadway 15 小时前回复“it’s 100% in person.”、deb_broadway 那条“three weeks of vacation per year so using two weeks for a lift is a lot.”现为 1 天前。deb_broadway 的意向信号仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 03:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空（was-open False，本轮自开自关）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 02:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 02:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 13 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 15 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论、deb_broadway 回复“it’s 100% in person.”、deb_broadway 那条“three weeks of vacation per year so using two weeks for a lift is a lot.”。deb_broadway 的意向信号仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 04:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空（was-open False，本轮自开自关）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 03:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 03:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 14 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 16 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论、deb_broadway 回复“it’s 100% in person.”、deb_broadway 那条“three weeks of vacation per year so using two weeks for a lift is a lot.”。deb_broadway 的意向信号仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 05:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent 持续恢复中（自 11-20 19:00 起的完整轮次链未断）。轮次开始时 opened() 为空（was-open False，本轮自开自关）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 04:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 04:00 轮同一批，仅时间推移：ahmed.wakib.79 关注（现为 15 小时前，仍仅“started following you”，无评论、无私信、无医美意向信号，不联系）、anatomyofthesoul.11 17 小时前点赞 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论、deb_broadway 回复“it’s 100% in person.”、deb_broadway 那条“three weeks of vacation per year so using two weeks for a lift is a lot.”。deb_broadway 的意向信号仍在列表中，属猎手动作范畴（须先过 E07、核她主页身份再回评），本轮为私信盯守，未发评论、未私信她。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，2 天前），无需私信回复。6 个旧关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）无医美意向信号，不联系。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 06:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK；轮次开始时 opened() 为空，本轮自己开的 profile，轮末已关。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常。
- 通知（instagram.com/notifications/）：自 05:00 轮起**无新增**，仍是 05:00 轮已见的同一批：ahmed.wakib.79 新关注（现 16h，05:00 轮为 15h，仅时间推移）、anatomyofthesoul.11 点赞 sarah 回复 deb_broadway 的评论（现 18h）、anatomyofthesoul.11 回复了 sarah 在其帖子下的评论。ahmed.wakib.79 仅为关注、无医美意向信号，不联系、不盲目回关；anatomyofthesoul.11 的点赞/回复属评论区互动（deb_broadway 线程），归猎手动作，本轮为私信盯守，未发评论、未私信。旧 6 个关注（shyam_ka_ladla_202、ashishbdbshd、pk_sona_love、rahul2389977、chameleon.951509、bym_esteticaterapiasbcn 美容机构号）仍在列表下方，无新增意向信号。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面正常停留）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。
2026-11-22 07:00 CST fb-dm-p44（sarahcook6809 IG私信盯守）：窗口外跳过（夜里窗口18:30–次日06:00），未开浏览器、未发内容、未碰账号。
--- 2026-11-22 08:00 fb-dm-p44（sarahcook6809 IG 私信盯守）窗口外跳过：北京时间 08:00 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。
--- 2026-11-22 09:00 fb-dm-p44（sarahcook6809 IG 私信盯守）窗口外跳过：北京时间 09:00 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。
--- 2026-11-22 10:00 fb-dm-p44（sarahcook6809 IG 私信盯守）窗口外跳过：北京时间 10:00 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 10:57 CST 跳过
- 窗口外（18:30–次日 06:00）：本轮直接结束，未开浏览器、未发任何内容、未碰账号。
--- 2026-11-22 12:00 fb-dm-p44（sarahcook6809 IG 私信盯守）窗口外跳过：北京时间 12:00 不在 18:30–次日 06:00 夜里窗口内，未开浏览器、未发任何内容、未碰账号。

- 2026-11-22 12:57 CST fb-dm-p44（sarahcook6809 / profile 44）跳过：当前时间在夜里窗口（18:30–次日 06:00）之外，本轮直接结束，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 13:57 CST 跳过
- 窗口外（18:30–次日 06:00）：本轮直接结束，未开浏览器、未发任何内容、未碰账号。
## 2026-11-22 14:57 CST — 跳过（窗口外）
- 本轮定时 15:00，当前北京时间 14:57，处于窗口外（窗口 18:30–次日 06:00）。按任务规则直接结束，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 15:57 CST — 跳过（窗口外）
- 本轮定时 16:00，当前北京时间 15:57，处于窗口外（窗口 18:30–次日 06:00）。按任务规则直接结束，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 16:57 CST — 跳过（窗口外）
- 本轮定时 17:00，当前北京时间 16:57，处于窗口外（窗口 18:30–次日 06:00）。按任务规则直接结束，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 17:57 CST — 跳过（窗口外）
- 本轮定时 18:00，当前北京时间 17:57，处于窗口外（窗口 18:30–次日 06:00）。按任务规则直接结束，未开浏览器、未发任何内容、未碰账号。

## 2026-11-22 19:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK；轮次开始时 opened() 仅有 profile 35（Bertie，另一轮次在跑），与本轮无关，未碰；本轮自开自关。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 06:00 轮起**新增 2 个关注**，均为仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关：
  - shreyansh_pandya_2216，8 小时前
  - moger4123，9 小时前
  - ahmed.wakib.79 关注现为 1 天前（06:00 轮为 16 小时前，仅时间推移），仍无意向信号，不联系。
  - anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。
  - 通知文本读回截断于 4000 字符，旧的 6 个仅“started following you”关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回中逐一重现，但新增内容只会出现在顶部，顶部除上述两项新关注外无其他新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 20:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK；轮次开始时 opened() 为空，本轮自开自关（debugging 127.0.0.1:47678）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常。
- 通知（instagram.com/notifications/）：自 19:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 19:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 9 小时前，19:00 轮为 8 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 10 小时前，19:00 轮为 9 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202、ashishbdbshd、pk_sona_love、rahul2389977、chameleon.951509、bym_esteticaterapiasbcn 美容机构号）仍在列表下方，无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 21:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK；轮次开始时 opened() 仅有 profile 35（Bertie，另一轮次在跑），与本轮无关，未碰；本轮自开自关（debugging 127.0.0.1:9090）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，Direct 收件箱顶部显示 sarahcook6809，登录态正常。
- 通知（instagram.com/notifications/）：自 20:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 20:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 10 小时前，20:00 轮为 9 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 11 小时前，20:00 轮为 10 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。通知文本读回截断于 4000 字符，旧的 6 个仅“started following you”关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回中逐一重现，但新增内容只会出现在顶部，顶部除时间推移外无新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束已关 profile 44（close 返回 closed:true；opened() 复核为空）。

## 2026-11-22 22:00 轮次（fb-dm-p44）

- 本轮 21:58–22:20 跑完（agent 传输层极不稳，全程 curl 52/18 反复重试，耗时拉长）。无 429/226/344，不作封号/登录失效升级。
- **was-open 误判 + 并发处理（本轮关键）**：轮次开始时 opened-before 明确列出 profile 44 已开（debugging 127.0.0.1:58648，open_time 21:27:32，系 21:30 猎手轮次打开），但 `is_open(44)` 内部的 opened() 调用撞上 curl 52 抛异常、按客户端设计返回 False；脚本据此误判为未开，执行了 open（返回同一调试地址 58648，即复用已开浏览器）并按原计划会在轮末 close。**中途发现另一 worker 的 hunt_read.py（21:30 猎手恢复读帖，6 条）正在用同一浏览器后，立即杀掉本轮主脚本（杀在 req-text 读到一半之前），避免轮末 close 关掉猎手轮次的窗口。**随后等 hunt_read 写完 /tmp/hunt_p44_recovery_retry.json（5/6 条读到正文，DRaHipTAOEs 一条因 curl 18 两次失败未读到，属 agent 传输层故障；其余 5 条含 DV_6YjQEnzC 均读到正常帖文，我方导航未造成可辨认的污染）且进程完全退出后，用不含 open/close 的补跑脚本完成剩余核查。**profile 44 全程未关**：补跑时 opened() 显示其调试地址已变为 127.0.0.1:51610、open_time 22:13:36（轮次中途被另一进程关掉重开，非本轮所为），本轮未再碰 close。
- 身份核验：通过（两次核验，两个会话均含本号个人资料链接 `/sarahcook6809/`；前一会话落在猎手读帖页 /p/DV_6YjQEnzC/，后一会话为首页 feed，登录态正常）。
- 通知（instagram.com/notifications/）：自 21:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 21:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 11 小时前，21:00 轮为 10 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 12 小时前，21:00 轮为 11 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202、ashishbdbshd、pk_sona_love、rahul2389977、chameleon.951509、bym_esteticaterapiasbcn 美容机构号）仍在列表下方，无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 教训留待总管：is_open 的“查不到就当没开”在 agent 闪断时段会误判——opened() 抛异常时应先重试/以 opened-before 列表为准再定 was_open，否则复用已开浏览器后轮末 close 会误关别人的窗口。本轮靠中途人工发现才躲过；下轮起若 opened-before 已列出本号而 is_open 报 False，应直接按已开处理（不 open、不 close）。

## 2026-11-22 23:00 轮次（fb-dm-p44）

- agent 传输层极不稳（非平台信号）：全程几乎每步都撞 curl 18/52、靠重试恢复，耗时约 17 分钟（22:58–23:15）。health、goto-home、goto-notif、notif-text、goto-requests、goto-general 均经 2–3 次重试后成功。无 429/226/344，不作封号/登录失效升级。
- **was-open 判定修正生效（22:00 轮教训已落实）**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用），脚本直接按已开处理——跳过 open、轮末跳过 close，profile 44 全程未关（本轮未碰 close，opened() 复核仍列出 44，调试地址 127.0.0.1:13383，open_time 22:17:05）。轮次开始时另有 profile 32、35、38 已开，均为其他轮次在跑，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 22:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 22:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 12 小时前，22:00 轮为 11 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 13 小时前，22:00 轮为 12 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202、ashishbdbshd、pk_sona_love、rahul2389977、chameleon.951509、bym_esteticaterapiasbcn 美容机构号）仍在列表下方，无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：**本轮经补跑核验，为空**。主跑全文 eval（innerText 前 4000 字）连续 3 次失败（curl 18/52/52），补跑又 3 次失败（curl 18/18/52），6 次均截断于“317 bytes remaining”；改走极小探针 eval（只回 url + 是否含空态文案 + 文本长度）一次成功：url 为 /direct/inbox/，含“Chats will appear here”空态文案，innerText 长 188——Primary 为空，无新私信、无待回复。教训：收件箱页全文 eval 的大响应在 agent 闪断时段会被截断，6 次同点失败后应改小探针，不必反复撞同一大响应。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 00:00 轮次（fb-dm-p44）

- agent 传输层极不稳（非平台信号）：主跑 health 3 次 curl 52、goto-notif 3 次 curl 52、notif-text 2 次 curl 52，耗时约 7.5 分钟；补跑 goto-notif、notif-text 各经 2–3 次 curl 18 截断重试后成功。无 429/226/344，不作封号/登录失效升级。
- **was-open 判定（22:00 轮教训已落实）**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 22:17:05，自 23:00 轮起未关），主跑与补跑均跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、38、63、65 在跑，均为其他轮次，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/，经补跑核验）：自 23:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 23:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 13 小时前，23:00 轮为 12 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 14 小时前，23:00 轮为 13 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。通知文本读回截断于 4000 字符，旧的 6 个仅“started following you”关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回中逐一重现，但新增内容只会出现在顶部，顶部除时间推移外无新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- 主跑缺口说明：主跑 goto-notif 3 次失败后，notif-text 读回的是首页 feed（url 为 instagram.com/），不是通知页，故主跑通知栏记为未核验；随后立即用不含 open/close 的补跑脚本重登通知页并读回成功（url 为 /notifications/，顶部与 23:00 轮一致），缺口已补上。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809；inbox-text 首试 curl 18“317 bytes remaining”截断，重试后一次成功）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 01:00 轮次（fb-dm-p44）

- agent 传输层瞬时故障（非平台信号）：opened-before 2 次 curl 52/18 后成功；goto-inbox、inbox-text 各 1 次 curl 18 截断后重试成功。无 429/226/344，不作封号/登录失效升级。
- **was-open 判定（22:00 轮教训已落实）**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 2026-11-22 22:17:05，自 23:00 轮起未关），主跑跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、63 在跑，均为其他轮次，未碰。
- **主跑两处读回被并发导航污染（已补跑核验）**：profile 44 正被另一轮次（猎手）共用同一浏览器，主跑 notif-text 与 inbox-text 的 eval 读回分别是猎手正在看的帖子页 /p/DdmSRk3EdqI/（dredmarminchio 拉皮帖）与 /p/DfP5ucjolAB/（drsametsendur 拉皮帖），不是目标页，故主跑通知栏与 Primary 收件箱记为未核验；随后立即用不含 open/close 的补跑脚本重登两页、带 URL 校验一次成功，缺口已补上。本轮未对猎手轮次的浏览造成可辨认的污染（只做了 goto + 只读 eval，未点赞/评论/发信）。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常（identity 读回时页面落在猎手帖子页，但 profileLinks 含本号链接为准，与前几轮同一口径）。
- 通知（instagram.com/notifications/，经补跑核验）：自 00:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 00:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 14 小时前，00:00 轮为 13 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 15 小时前，00:00 轮为 14 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。通知文本读回截断于 4000 字符，旧的 6 个仅“started following you”关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回中逐一重现，但新增内容只会出现在顶部，顶部除时间推移外无新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：**经补跑核验，为空**，无新私信、无待回复（收件箱顶部显示 sarahcook6809；“Chats will appear here after you send or receive a message”）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 02:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK。
- **was-open 判定**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 2026-11-22 22:17:05，自 23:00 轮起未关），主跑跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、63 等在跑，均为其他轮次，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 01:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 01:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 15 小时前，01:00 轮为 14 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 16 小时前，01:00 轮为 15 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回截断内逐一重现，但新增内容只会出现在顶部，顶部除时间推移外无新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809；“Chats will appear here after you send or receive a message”）。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 03:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK。
- **was-open 判定**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 2026-11-22 22:17:05，自 23:00 轮起未关），主跑跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、63 在跑，均为其他轮次，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 02:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 02:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 16 小时前，02:00 轮为 15 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 17 小时前，02:00 轮为 16 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）仍在列表下方，无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809；“Chats will appear here after you send or receive a message”）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 04:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK。
- **was-open 判定**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 2026-11-22 22:17:05，自 23:00 轮起未关），主跑跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、63 在跑，均为其他轮次，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 03:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 03:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 17 小时前，03:00 轮为 16 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 18 小时前，03:00 轮为 17 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回截断内逐一重现，但新增内容只会出现在顶部，顶部除时间推移外无新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809；“Chats will appear here after you send or receive a message”）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 05:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK。
- **was-open 判定**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 2026-11-22 22:17:05，自 23:00 轮起未关），跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、63 在跑，均为其他轮次，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 04:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 04:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 18 小时前，04:00 轮为 17 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 19 小时前，04:00 轮为 18 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论并回复 sarah 在其帖子下的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。其余仍为矩阵内号互刷（gaga5456、elainaklocko_lily.02176 各 2 条，3 天前），无需私信回复。旧 6 个关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）仍在列表下方，无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809；“Chats will appear here after you send or receive a message”）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。

## 2026-11-23 06:00 轮次（fb-dm-p44）

- 全程一次成功，无 agent 传输层故障、无 429/226/344，不作封号/登录失效升级。agent v10，health 一次 OK。
- **was-open 判定**：轮次开始时 opened-before 明确列出 profile 44 已开（另一轮次在用，同一会话调试地址 127.0.0.1:13383、open_time 2026-11-22 22:17:05，自 23:00 轮起未关），跳过 open、轮末跳过 close，profile 44 全程未关。轮次开始时另有 profile 32、35、63 在跑，均为其他轮次，未碰。
- 身份核验：通过。IG 首页正常加载，导航栏含本号个人资料链接 `/sarahcook6809/`，登录态正常。
- 通知（instagram.com/notifications/）：自 05:00 轮起**无新增关注、无新增评论互动**。列表顶部仍是 05:00 轮同一批，仅时间推移：shreyansh_pandya_2216 关注（现为 19 小时前，05:00 轮为 18 小时前，仅“started following you”，无评论、无私信、无医美意向信号，不联系、不盲目回关）、moger4123 关注（现为 20 小时前，05:00 轮为 19 小时前，同上，不联系）、ahmed.wakib.79 关注现为 1 天前（仍无意向信号，不联系）、anatomyofthesoul.11 点赞了 sarah 回复 deb_broadway 的评论（deb_broadway 线程，评论区互动，属猎手动作范畴，本轮为私信盯守，未发评论、未私信）。deb_broadway 的意向信号（假期不够用两周做拉皮）仍在列表中，留待猎手轮次跟进（须先过 E07、核她主页身份再回评）。旧 6 个关注（shyam_ka_ladla_202 11-11、ashishbdbshd 11-09、pk_sona_love 11-06、rahul2389977 11-04、chameleon.951509 11-02、bym_esteticaterapiasbcn 10-30 巴塞罗那美容机构号）未在本轮读回截断内逐一重现，但新增内容只会出现在顶部，顶部除时间推移外无新项，即无新增意向信号。旧系统提示（10-19 新 Meta 账号、10-12 未识别设备）为历史通知，登录正常，不作升级。
- Direct 收件箱 Primary：为空，无新私信、无待回复（收件箱顶部显示 sarahcook6809；“Chats will appear here after you send or receive a message”）。chameleon.951509 那条是 Note（歌曲分享），不是私信。
- Direct Requests：已核验，0 条（“Delete all 0”）。
- Direct General：已核验到，为空（直接 goto /direct/general/ 成功，页面停留在收件箱、显示空态“Chats will appear here…”）。
- 本轮动作：无发信。无合格客资，无致命问题。
- 轮次结束未关 profile 44（轮开始时已是别轮在用，按手册不关别人的窗口）。
- 2026-11-23 06:57 CST 窗口外跳过：本轮窗口为北京时间 18:30–次日 06:00，当前 06:57 已出窗口，未开浏览器、未发内容、未碰账号。
- 2026-11-23 07:57 CST 窗口外跳过：本轮窗口为北京时间 18:30–次日 06:00，当前 07:57 已出窗口，未开浏览器、未发内容、未碰账号。
- 2026-11-23 09:00 CST 窗口外跳过：本轮窗口为北京时间 18:30–次日 06:00，当前 09:00 已出窗口，未开浏览器、未发内容、未碰账号。
