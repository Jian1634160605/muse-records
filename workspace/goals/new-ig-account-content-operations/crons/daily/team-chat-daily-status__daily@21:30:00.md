---
id: team-chat-daily-status
enabled: true
owner: goal:new-ig-account-content-operations
execution:
  kind: space_action
  slug: yun-ying-tuan-dui-qun-liao
  action: refreshTeamStatus
  args: {}
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 21:30:00
metadata:
  originating_chat_context_json: '{"chat_id":"2e7b7db1-0363-40bc-8c95-f4cb3b432c25","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
Invoke the web artifact's published scheduled action and retain its run history.
