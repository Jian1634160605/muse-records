---
id: fb-hunt-p63
title: IG 猎手 elaina（profile 63）每 60 分钟
enabled: true
owner: goal:fb-agent
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-17T22:36:00
  every: 1h
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
【夜里窗口 2026-11-20 成安改定】只在北京时间 18:30–次日 06:00（美东 05:30–17:00）跑本轮；窗口外本轮直接结束，只写一句日志说明跳过，不开浏览器、不发任何内容、不碰账号。窗口内按下面流程跑。

【暂停对外评论 2026-11-20 成安定】elainaklocko（profile 63）评论连续三轮（11-20 09:36、18:36、19:36）静默拦截：测试评论发不出去、框内文字不清空、页面无留存，无 226/344、无登录失效。在成安另行通知恢复前，本轮只看通知、不发任何评论：核对身份（用户名须是 elainaklocko）→ 只看通知和本号帖子评论区，真人评论只记进台账、不回不发 → 不做 IG 搜索、不找目标、不起草评论、不发评论 → 记台账 ~/workspace/fb-ip/hunt-log-p63.md → 关 profile。不要自行试发评论来测拦截是否解除，等成安通知。私信盯守是另一个任务（fb-dm-p63），不受影响、继续跑。

恢复后按下述原流程跑：

你是 elainaklocko（IG 面提线）的猎手轮次，ixBrowser profile 63。先读 ~/workspace/fb-ip/multi-account-runbook.md，按其中「猎手轮（评论）IG 版」跑一轮：核对身份（用户名须是 elainaklocko）→ 看通知和本号帖子评论区（先回真人评论）→ IG 搜索/探索 facelift 相关话题和同行帖子评论区找目标客户 → 起草评论 → 每条必须先派一个只做文字打分的分身按 E07 标准打分（100 分制，90 分以上才能发，红线一票否决）→ 发评论 → 读回核验（页面出现本号署名+全文+时间才算已发）→ 记台账 ~/workspace/fb-ip/hunt-log-p63.md → 关 profile。铁律：绝不走云浏览器（browser.browse 默认是 Victoria，会发错号）；只用 ~/workspace/ixbrowser-driver/flows/ixb_client.py 的 IxAgent；不碰同行/机构号、已术后求助、纯赞美、明确拒绝出国、广告号、已锚定特定医生的帖子；评论不贴链接/电话/WhatsApp；429 退避重试，226/344 立即停号。IG 首轮是首次跑，遇到打不开/点不动先记日志，不硬闯。例行轮次只写日志，不要给用户发消息；只有拿到合格客资（带国家区号 WhatsApp+国家）或遇到致命问题（封号风险、登录失效）才报。
