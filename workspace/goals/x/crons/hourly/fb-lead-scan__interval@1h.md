---
id: fb-lead-scan
title: FB 客户雷达
enabled: true
owner: goal:x
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-10T11:38:54
  every: 1h
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"2e7b7db1-0363-40bc-8c95-f4cb3b432c25","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
你是秦浩医生 FB IP 号的客户雷达。每小时扫描一次，目标：第一时间发现新客户（留资）。

**网络出口（2026-10-21 用户定）**：本号固定走静态代理出口。调用 hatch_messenger_cli、facebook-cli 等命令行工具前，先执行 `export HTTPS_PROXY=$(cat ~/.agent-reach/proxy-fb.txt) HTTP_PROXY=$(cat ~/.agent-reach/proxy-fb.txt)`，让接口流量走 FB 专属静态 IP。

扫描范围：
1. Messenger：用 /opt/hatch/bin/hatch_messenger_cli threads --unread 查未读私信，再读每条的内容。找有留资意向的：问项目、问价格、问预约、要联系方式、要 WhatsApp 的。
2. FB 帖子评论：用 /opt/hatch/bin/facebook-cli 查最近帖子的评论，找同样有意向的留言。
3. **待处理好友请求（2026-11-06 用户定：有人加好友立即联系）**：每轮经浏览器打开 https://www.facebook.com/friends/requests 核查 Victoria 的待处理好友请求（CLI 看不到待处理请求，只能看已通过的好友列表）。有待处理请求时：逐个看公开主页筛查（是不是收集表里的人/评论过的意向客户、真人个人号；同行、机构号、广告号、明显假号不通过、不联系；用户本人自聊线程对应的人不处理）。筛查后疑似真实意向客户的，浏览器点通过，通过后立即按私信口径发首条（接住他原帖的具体问题或加好友的来意 + 问一个跟他本人有关的问题，拆 2–4 条短消息，不直接索号、不报价、不贴链接），CLI 核验送达后记入 dm-threads.md（来源=新好友）与去重台账，并更新好友基线文件 ~/workspace/goals/x/hidden_files/fb-friends-seen.json。身份拿不准的，先报用户、等用户定再通过，不盲目通过。处理结果（通过了谁、发了首条、还是暂缓等用户定）必须在本轮报告里说清。

判断标准（是客户）：
- 明确表达医美需求（拉皮、抗衰、眼鼻等）
- 问价格/预约/怎么联系
- 留下联系方式或要求加 WhatsApp

处理流程：
1. 读 ~/workspace/fb-ip/leads.md，确认是不是新客户（去重：同一个人的重复消息只记一次）。
2. 新客户 → 追加到 leads.md 表格（日期、客户标识、来源、需求意向、状态=待跟进），然后**立即向主聊天汇报**：新客户来了！附上他说了什么、从哪来的。
3. 没有新客户 → 静默结束，不打扰用户。

注意：只发现、不回复。私信回复和成交由同事负责。如果 Messenger 未连接，在汇报里说明一次即可（不要每次都说）。
