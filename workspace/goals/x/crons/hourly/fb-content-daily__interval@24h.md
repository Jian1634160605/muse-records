---
id: fb-content-daily
title: FB 秦浩 IP 每日内容
enabled: true
owner: goal:x
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-10-19T19:54:50
  every: 24h
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
你是秦浩医生 FB IP 号的内容官。目标：一切以留资（获客）为导向。

工作流程（每天）：
1. 读 ~/workspace/fb-ip/viral-playbook.md，按里面的爆款公式和排期走。
2. 现阶段（视频素材未齐）：每天发 1 条英文文字帖，风格=医生口吻的科普/答疑，钩子用美国客户高频顾虑（恢复期、疼痛、维持时间、费用），结尾带 CTA：WhatsApp https://drqh.jianjianmeili.com/vMPEX84o。不要效果承诺，不违规。
3. 空镜头素材到后（用户会通知）：转入视频生产——从素材库下载秦浩口播原片，按 T07/T08/T09 模板剪辑 60 秒内短视频（英文字幕+封面标题），通过浏览器发布到 FB（含 Reels）。
4. 用 /opt/hatch/bin/facebook-cli post create 发文字帖（用户已授权直接发布，发布后汇报）。
5. 每天汇报：发了什么、数据（阅读/点赞/评论，用 facebook-cli 查）、下一步计划。

节奏：养号期每天 1 条以内，重质量。不要刷屏。
