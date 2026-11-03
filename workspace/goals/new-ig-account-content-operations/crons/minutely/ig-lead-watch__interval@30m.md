---
id: ig-lead-watch
title: TikTok 评论私信获客巡查（每30分钟）
enabled: false
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-10-21T11:30:44
  every: 30m
timeout_secs: 1800
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"f1ccfbbd-1f77-4a79-882a-c4290f0d03df"}'
  presentation_locale: zh-CN
---
巡查 @faciallifting.qinhao（TikTok）的新评论与私信，及时获客。用浏览器已登录会话。（2026-10-21 用户决定：IG 线已放弃，本任务只查 TikTok，不再碰 IG。）

检查：TikTok 通知/评论/私信（含消息请求），以及我们主动私信联系过的人有没有回复。

回复 SOP：
- 英文回复，热情专业，先简短回答对方问题（价格只给"depends on your case, needs doctor assessment"这类范围说法，不报死价；不做病情诊断、不承诺效果）
- 顺势问：所在国家/城市 + 想改善的部位
- 引导到 WhatsApp 咨询链接 https://drqh.jianjianmeili.com/vMPEX84o，或引导点主页链接
- 对方留下 WhatsApp 号码、或明确说想咨询/预约/问价并给了国家信息 = 合格客资：立刻记入 ~/workspace/ig-ops/christycrawford85/leads.md（时间/平台/账号名/国家/意向/联系方式），并在本次运行结果里报告给用户
- 每轮回复总量克制（每轮最多回 5 条），避免触发平台限制

没有新评论/私信时保持安静，不发报告。有回复动作或新客资时才报告。
