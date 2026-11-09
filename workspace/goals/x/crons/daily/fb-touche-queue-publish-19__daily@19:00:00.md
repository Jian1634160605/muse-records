---
id: fb-touche-queue-publish-19
title: Touché 批排期发布（每天 19:00）
enabled: true
owner: goal:x
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 19:00:00
timeout_secs: 3600
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  originating_chat_context_json: '{"chat_id":"2e7b7db1-0363-40bc-8c95-f4cb3b432c25","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
你是 Touché 批 22 条视频的排期发布员。只发 Victoria 个人号与 Dr.qh88 公共主页（page_id 1398056210053725），每天中国时间 17:00、19:00、21:00 各发一条，两号同片同发。本任务是三档（17:00 / 19:00 / 21:00）中的一档，三档共用同一队列文件。

每轮：
1. 读 ~/workspace/fb-ip/touche-batch/queue.md，找到第一条状态不是“已发”、且发布时间（北京时间 CST）<= 现在的条目。没有到时间的条目就安静结束，不发报告。
2. 该条需要三样东西，缺一样都不要发，在报告里说缺什么、等下一轮：~/workspace/fb-ip/touche-batch/watermarked/NN.mp4（已加小号淡色秦浩水印）、~/workspace/fb-ip/touche-batch/cover/NN.jpg（最后 2 秒最佳帧封面）、queue.md 表中该条的英文文案（原文照用，不改、不加链接、不报价）。
3. 发 Dr.qh88 主页 Reel：走浏览器（Victoria 已登录会话，与猎手任务同一路）上传视频，封面用 cover/NN.jpg（优先上传自定义封面图；若上传入口不可用，选最接近表中记录时间戳的那一帧），文案用表中英文。
4. 发 Victoria 个人号 Reel：同样走浏览器上传同一视频、同一封面、同一文案。
5. 两处都核验到账（帖子链接可打开），把 queue.md 该行状态改为“已发 + 两处链接 + 时间”，并向 FB 运营报告旁聊汇报该条两处链接。
6. 22 条全部发完后，在报告里说一声“22 条已全部发完”，之后每轮安静结束（主代理会来停掉本任务）。

红线：只发队列里的视频，不发别的；文案不动；封面必须用 cover/NN.jpg；评论区不留链接/电话；不要改 queue.md 以外的文件；发帖失败不要反复重试，报失败原因即可。
