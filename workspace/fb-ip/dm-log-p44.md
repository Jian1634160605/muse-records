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
