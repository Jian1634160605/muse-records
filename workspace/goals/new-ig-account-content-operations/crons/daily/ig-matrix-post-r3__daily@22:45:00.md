---
id: ig-matrix-post-r3
title: 发布轮次3（v3 只发 FB）
enabled: true
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 22:45:00
timeout_secs: 3600
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
发布轮次 3：把今天队列里的 v3 发到 Facebook 主页。（2026-10-21 用户决定：IG 线已放弃；TikTok @faciallifting.qinhao 已交同事运营，本任务不得再碰 TikTok。2026-10-25 用户批新打法：Victoria 视频从个人时间线挪到主页发。）队列目录：~/workspace/ig-ops/christycrawford85/queue/<今天日期>/，视频 v3.mp4，文案在 captions.md 的 V3 节，用 FB 版文案。

先审后排（硬门槛，2026-10-24 用户定）：发之前先读 captions.md 的 V3 节，只有该节内出现『用户已批准』字样（主代理在用户点头后写入，带日期时间）才发；没有该字样 = 未批，本轮跳过并报告『未批，跳过』，绝不自动发。队列或文件不存在则报告缺料，不要拿别的文件顶替。

防重复：先看队列目录里的 posted.txt，若已有 r3 的 FB 记录则跳过并报告"已发过"。posted.txt 里若只有历史 TikTok 记录，不算 FB 已发，照常发 FB（但仍须先过先审后排门槛）。

音乐规则（2026-10-20 用户新规）：队列里的成品文件在备料阶段已经嵌入配好的音乐。直接上传成品文件，不要在平台内找曲库、不要添加平台音乐、不要静音或改动音频。

发布要求（用浏览器，已登录会话 Victoria Maizie）：
- Facebook 主页 Dr.qh88（61595415571609）：以主页身份发 Reel，用 FB 版文案，直接上传成品文件。若无法以主页身份发布，跳过并报告原因，不要退回发个人号。

发完后：以主页身份在该 Reel 评论区留一句引导评论，引导用户点击主页的 WhatsApp 联系链接；评论本身不贴链接、不贴电话号码。

成功后把「FB+链接」追加写入 posted.txt。完成向主聊天报告 FB 链接；失败时报告失败在哪一步、什么现象，不要盲目重试超过 1 次。
