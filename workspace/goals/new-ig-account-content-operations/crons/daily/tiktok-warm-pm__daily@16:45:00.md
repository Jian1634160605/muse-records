---
id: tiktok-warm-pm
title: TikTok 养号刷视频（下午场）
enabled: false
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 16:45:00
timeout_secs: 2400
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"f1ccfbbd-1f77-4a79-882a-c4290f0d03df"}'
  presentation_locale: zh-CN
---
TikTok 养号会话（下午场）：用浏览器已登录 @faciallifting.qinhao 的会话，像真人一样刷视频，给账号恢复活跃度和垂直标签。

做法：
- 打开 TikTok，先刷 For You 推荐页；再依次搜索 facelift、plastic surgery、before and after、rhinoplasty 等词，刷同类视频
- 节奏放慢：每条视频至少看完大半，短视频看完再划走；单次会话约 15 分钟，总共看 15–25 条
- 只给拉皮/医美类的优质视频点赞，整场 3–5 个赞封顶；不评论、不私信、不关注、不分享
- **人机验证规则（用户定的打法）**：遇到拼图/滑块验证，先自己尝试解决（最多 2 次）；过不去就**立即停下**，在本次结果里报告" TikTok 验证拦截，需要用户接管浏览器"，由主代理喊用户来过验证。不要长时间反复磨验证，单场总时长不超过 25 分钟
- 结束把本场小结写进 ~/workspace/goals/new-ig-account-content-operations/hidden_files/tiktok-warm_log.md；无异常不向用户发报告，有账号安全/限流提示或验证拦截才报告
