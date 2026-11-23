---
id: fb-ig-publish-round1
title: FB/IG 发布第 1 轮（22:00）
enabled: false
owner: goal:fb-agent
mode: task
schedule:
  kind: daily
  timezone: '@user.current'
  time: 22:00:00
timeout_secs: 7200
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:exact-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
今晚 22:00 发布轮次（第 1 条/号）。先读 `~/workspace/fb-ip/publish-plan-20261121-night.md` 的分配表，按 22:00 那一列给 9 个号各发 1 条 FB/IG Reel（FB 6 个：Victoria p2、Jusa p5、Lark p32、Bertie p35、Oe p38、Ejje p67；IG 3 个：sarah p44、elaina p63、gaga p65）。

执行要求：
- 发前用 ffprobe 核验每个视频 1 视频轨 + 1 音频轨，0 音轨不发；文案必须已填（缺 fb04.txt、R1 文案就按计划文件里的要求现写英文文案：钩子+设计点+互动问题，AI 部分注明 AI-generated video for illustration，带音乐的贴音乐 credit）。
- FB 用 `~/workspace/ixbrowser-driver/flows/fb_reel_publish_v4.py <profile_id> <video_path> <caption>`；IG 先读 `ig_reel_publish.py` 的用法再发。只传单个视频文件，不带封面。打开浏览器后立即最小化；Bertie 绝不走 browser.browse，走 ixBrowser profile 35。Emerson(p1)/pokk(p43)/Winsino(p80) 绝不操作。
- 核验：FB 以 CLI timeline fetch / 通知页 "Your reel is published" 为准，核验不到绝不直接重试；IG 以 Reel 链接可访问为准。
- 发完每条做本号自评引流评论（不贴链接、不贴电话，转化走主页）。
- 结果续写进 `~/workspace/fb-ip/publish-log-20261118.md`。汇报只说结果：发了几条、每条链接、失败的哪条+原因，不讲过程。失败的留到 02:00 备用档补发，不要在当轮反复重试。
