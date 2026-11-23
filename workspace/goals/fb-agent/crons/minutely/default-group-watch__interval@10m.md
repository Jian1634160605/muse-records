---
id: default-group-watch
title: 默认分组变动监控
enabled: true
owner: goal:fb-agent
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-19T13:57:50
  every: 10m
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"5b57f032-db35-4bd0-87bf-372f11c7df72"}'
  presentation_locale: zh-CN
---
每 6 小时检查 ixBrowser 默认分组（group_id=1）成员是否变动，防止再用旧名单操作账号（教训：2026-11-18 Emerson 已移到尹卓组，但发布仍按 11-17 旧名单走了 Emerson）。

1. 用 muse.exec 运行：python3 /home/hatch/workspace/ixbrowser-driver/check_default_group.py（超时 300 秒），读它的 stdout。
2. 输出以“CHANGE”开头（成员增减）：把变化全文（哪个号增/减、从哪个组到哪个组、新名单文件路径）写进本轮最终汇报里，以便主 agent 报用户、改记忆。不要自己改 MEMORY.md。
3. 输出是“OK 无变化”：本轮不需要向任何人汇报。
4. 输出是 ERROR（agent 连不上等）：在最终汇报里写清失败原因；状态文件不要动，下次再查。

只读监控，不操作账号、不开浏览器、不改任何 profile 配置。
