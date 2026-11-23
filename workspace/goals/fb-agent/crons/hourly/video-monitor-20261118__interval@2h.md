---
id: video-monitor-20261118
title: 视频监控 2026-11-18 晚 8 条
enabled: false
owner: goal:fb-agent
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-19T00:17:53
  every: 2h
timeout_secs: 1800
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","provider":"main","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
视频监控轮次（2026-11-18 晚发出的 8 条视频，监控期至 2026-11-19 22:00）。

1. 运行监控脚本：`python3 ~/workspace/fb-ip/video_monitor.py`（脚本自带重试、25 分钟预算、22:00 后自动停跑；ixBrowser 操作只读数据、不发评论私信、开号后自动最小化）。
2. 读本轮新追加到 `~/workspace/fb-ip/video-monitor-20261118.md` 的一轮数据。
3. 只在以下情况向主聊汇报，其余情况只写台账、不打扰：
   - 有视频播放破 1 万（台账标 🚨）：立即报哪条、哪个号、多少播放。
   - 有视频 2 小时内增长超过 2000 播放：报哪条、增速。
   - 连续两轮有 2 条以上视频读不到数据：报哪几条、什么原因。
   - 脚本本身报错退出或 agent 连续不通：报错误。
4. 注意：发布台账里 Lark、Ejje 两条 FB 链接经核实有误（指向他人/旧 Reel），读不到是链接问题；Oe 的链接无误但 insights 页曾报内容不可用。8 条静音版按用户决定要删了重发带音乐版——重发后监控列表须用新链接/新帖子更新（改 `~/workspace/fb-ip/video_monitor.py` 的 VIDEOS 列表），不要继续盯已删的旧链接。
