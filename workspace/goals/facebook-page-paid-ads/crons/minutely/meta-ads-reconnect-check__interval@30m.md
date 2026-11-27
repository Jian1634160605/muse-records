---
id: meta-ads-reconnect-check
title: Meta 广告重连检查
enabled: false
owner: goal:facebook-page-paid-ads
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-26T16:09:25
  every: 30m
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:automatic-interval-anchor]
  predicted_connector_permissions:
  - connector: meta_ads
    method: ads_get_ad_accounts
  originating_chat_context_json: '{"chat_id":"2e7b7db1-0363-40bc-8c95-f4cb3b432c25","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"5b57f032-db35-4bd0-87bf-372f11c7df72"}'
  presentation_locale: zh-CN
---
每半小时检查一次 Meta 广告连接是否恢复。先运行 /opt/hatch/bin/meta-ads-cli list-tools --names-only，等它返回后再运行 /opt/hatch/bin/meta-ads-cli call-tool --name ads_get_ad_accounts（必须是这条完整命令，不加任何参数）。
- 如果调用成功并返回广告账户列表：立即在主聊告诉用户连接已恢复，并列出看到的广告账户 ID、状态和货币；然后用 cron.update 把本任务（id：meta-ads-reconnect-check）设为 enabled:false，停止继续检查。
- 如果仍失败（例如 FACEBOOK_ACCOUNT_LINK_REQUIRED 或其他错误）：不要给用户发任何消息，保持安静，等下一次检查；把结果简要追加记到 ~/memory/2026-11-26.md（一行即可）。
- 只读检查，不要改 MEMORY.md，不要动任何广告账户、不要做任何写操作。
