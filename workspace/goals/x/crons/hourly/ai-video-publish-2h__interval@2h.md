---
id: ai-video-publish-2h
title: AI 面诊视频 2 小时轮流发布
enabled: true
owner: goal:x
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-11T21:15:37
  every: 2h
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
AI 面诊视频 2 小时轮流发布（老板 2026-11-11 19:07/19:13 定：两个 FB 号轮流发，每 2 小时发一次；Bertie 登录仍死，先由 Victoria 每 2 小时接着发，Bertie 好了再轮进来）。

每轮只做一件事：发队列头部一条。先读队列文件 `~/workspace/fb-ip/ai-video-data/publish-queue.md` 和 routine `~/workspace/fb-ip/ai-video-routine.md`，按队列办事。

1. 看队列头部第一条待发项：如果已有 post_id，说明已发过，跳过并报重复风险，不要重发；如果已标记“尝试中/等审批”，说明上一轮的发布审批还没结果，不要再发新的一条，只报“等上一条审批结果”，然后结束。
2. 去向判断：头部去向是 Bertie 时，一律不发——Bertie 登录仍死，需老板重导新鲜 cookie 才能发；只报“Bertie 仍未恢复，本轮跳过”，然后结束。头部去向是 Victoria/Dr.qh88 时才发。
3. 发布（只发 Victoria/Dr.qh88）：用 facebook-cli `pages posts create --page-id 1398056210053725 --text '<队列里该条的英文文案>' --privacy PUBLIC --file '<队列里该条的成片绝对路径>'`，单 MP4 即为一条 Reel，封面已嵌在视频开头 2 秒、与视频同条发出。文案一律用队列里写好的英文（含 AI-generated video for illustration），不要自己改文案、不要加中文、不要加链接电话。发前先用 ffprobe 核对该成片是 10.0 秒、720x1280、1 视频流+1 音频流；不对就停手并报。
4. 核验：只有返回 `state: published` 才算发出，拿到 post_id 和 post_url 后立刻把队列文件里该条改成已发并记下 post_id 和链接，再到 `~/workspace/fb-ip/ai-video-data/` 给该条开数据盯守表（播放/点赞/评论/分享，首读记下）。发完用本号在该视频评论区留一句队列里写好的自评引流评论（英文、引导点主页 WhatsApp 链接、不贴链接、不贴电话）；评论发不出去就如实报，不要因此重发视频。
5. 队列少于 2 条待发时，在汇报里加一句“队列快空了，需要补下一批”，不要在本轮里自己做视频。
6. 队列已空时什么都不发，只报“队列已空，等下一批”，然后结束。
7. 每轮结束向主聊汇报：发了哪一条、去向、链接；没发则报没发的原因（Bertie 未恢复 / 等审批 / 队列已空）。不要编数据，读不到就写未读到。观察记到当日日志 `~/memory/2026-11-11.md`（只记事实），不要改 MEMORY.md。
