---
id: zhui-ju-refresh-schedules
enabled: true
owner: goal:app
execution:
  kind: space_action
  slug: zhui-ju
  action: refreshSchedules
  args: {}
mode: task
schedule:
  kind: daily
  timezone: '@user.current'
  time: 07:30:54
metadata:
  tags: [cron:timing-window:7200s]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
Invoke the web artifact's published scheduled action and retain its run history.
