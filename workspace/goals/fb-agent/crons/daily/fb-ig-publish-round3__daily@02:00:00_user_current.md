---
id: fb-ig-publish-round3
title: FB/IG 发布第 3 轮（02:00，钩子起号轮）
enabled: true
owner: goal:fb-agent
mode: task
schedule:
  kind: daily
  timezone: '@user.current'
  time: 02:00:00
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:exact-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"5b57f032-db35-4bd0-87bf-372f11c7df72"}'
  presentation_locale: zh-CN
---
今晚 02:00 发布轮次（第 3 条/号，钩子起号轮）。先读 `~/workspace/fb-ip/hook-batch-20261124.md` 第三轮表和 `~/workspace/fb-ip/publish-plan-20261124-night.md`。按钩子表给 12 个号各发 1 条 FB/IG Reel（FB 10 个：Victoria p2、Jusa p5、Lark p32、Oe p38、Ejje p67、p102、p103、p106、p108、p109；IG 2 个：sarah p44、gaga p65；Bertie p35 通道故障今晚 0 条；p130 今晚不排）。

执行要求：
- 只发已剪好、已过 E07 90 分、已在用户电脑上核实存在的钩子版；没剪好、没过审、文件不存在的位空着，不硬发、不拿原片凑数。
- Lark 两条待验证：验证未确认解除就空着，不硬发。
- 发前用 ffprobe 核验每个视频 1 视频轨 + 1 音频轨，0 音轨不发；文案必须已填（文案在 ~/workspace/fb-ip/captions/；缺文案就按钩子表要求现写英文文案：钩子+设计点+互动问题，AI 部分注明 AI-generated video for illustration，带音乐的贴音乐 credit）。封面 = 钩子大字 + 揭晓帧。
- FB 用 `~/workspace/ixbrowser-driver/flows/fb_reel_publish_v4.py <profile_id> <video_path> <caption>`；IG 先读 `ig_reel_publish.py` 的用法再发。只传单个视频文件，不带封面。打开浏览器后立即最小化；Bertie 绝不走 browser.browse，走 ixBrowser profile 35。Emerson(p1)/pokk(p43)/Winsino(p80)/elaina(p63，已删) 绝不操作。
- 核验：FB 以 CLI timeline fetch / 通知页 "Your reel is published" 为准，只认本轮时间窗口内的通知 + 文案比对，核验不到绝不直接重试；IG 以 Reel 链接可访问为准。
- 发完每条做本号自评引流评论（不贴链接、不贴电话，转化走主页）。
- 结果续写进 `~/workspace/fb-ip/publish-log-20261118.md`。汇报只说结果：发了几条、每条链接、失败的哪条+原因，不讲过程。失败的留明天，不当轮反复重试。
