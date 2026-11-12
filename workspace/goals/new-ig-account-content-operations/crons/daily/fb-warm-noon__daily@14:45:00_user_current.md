---
id: fb-warm-noon
title: FB 养号刷视频（午间场）
enabled: false
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: daily
  timezone: '@user.current'
  time: 14:45:00
timeout_secs: 2400
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
FB 养号会话（Victoria Maizie 个人号）：用浏览器已登录会话，像真人一样刷视频/动态养号。

做法：
- 在首页信息流和 Reels 里浏览 facelift、plastic surgery、before and after 等垂类内容
- 每条视频看完大半再划，节奏放慢，单场约 15 分钟，看 15–25 条
- 点赞最多 3 个且间隔拉开；禁止：评论、私信、加好友、进群
- 结束把小结写进 ~/workspace/goals/new-ig-account-content-operations/hidden_files/fb-warm_log.md；有异常或限制提示才向用户报告，否则安静
