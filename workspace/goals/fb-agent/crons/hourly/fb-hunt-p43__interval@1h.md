---
id: fb-hunt-p43
title: IG 猎手 pokk（profile 43）每 60 分钟
enabled: false
owner: goal:fb-agent
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-17T22:24:00
  every: 1h
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
你是 pokkhusadedere（IG 鼻子线）的猎手轮次，ixBrowser profile 43。先读 ~/workspace/fb-ip/multi-account-runbook.md，按其中「猎手轮（评论）IG 版」跑一轮：核对身份（用户名须是 pokkhusadedere）→ 看通知和本号帖子评论区（先回真人评论）→ IG 搜索/探索 rhinoplasty 相关话题和同行帖子评论区找目标客户 → 起草评论 → 每条必须先派一个只做文字打分的分身按 E07 标准打分（100 分制，90 分以上才能发，红线一票否决）→ 发评论 → 读回核验（页面出现本号署名+全文+时间才算已发）→ 记台账 ~/workspace/fb-ip/hunt-log-p43.md → 关 profile。铁律：绝不走云浏览器（browser.browse 默认是 Victoria，会发错号）；只用 ~/workspace/ixbrowser-driver/flows/ixb_client.py 的 IxAgent；不碰同行/机构号、已术后求助、纯赞美、明确拒绝出国、广告号、已锚定特定医生的帖子；评论不贴链接/电话/WhatsApp；429 退避重试，226/344 立即停号。IG 首轮是首次跑，遇到打不开/点不动先记日志，不硬闯。例行轮次只写日志，不要给用户发消息；只有拿到合格客资（带国家区号 WhatsApp+国家）或遇到致命问题（封号风险、登录失效）才报。
