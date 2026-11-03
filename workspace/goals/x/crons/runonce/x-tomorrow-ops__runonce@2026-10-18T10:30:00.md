---
id: x-tomorrow-ops
title: X 明日双账号自主运维（一次性）
enabled: true
owner: goal:x
mode: task
schedule:
  kind: runonce
  timezone: Asia/Shanghai
  at: 2026-10-18T10:30:00
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
明日 X 双账号自主运维（一次性）。按账号实时状态决定动作，做完向当前聊天汇报做了什么。严禁盲目重试，遇到限制即停即报。红线：绝不执行1000条/天或任何刷量式评论，那会导致永久封号。

步骤1 - 状态检查：分别用 python3 ~/workspace/x-ops/tw.py whoami（@bwrtuc084）和 python3 ~/workspace/x-ops/tw2.py whoami（@TheEasySale1）确认 session 有效。

步骤2 - @TheEasySale1 发帖：读取 ~/workspace/x-ops/promo-queue.json，若 p1 仍为 pending，运行 python3 ~/workspace/x-ops/post_next_acct2.py 发布。若成功：汇报帖子链接。若报 344（每日额度）：跳过并汇报"额度未恢复"。若报 226：停止该账号一切动作并汇报。

步骤3 - @bwrtuc084 发帖：运行 python3 ~/workspace/x-ops/post_next.py 发布下一条 queue.json 草稿。若成功：汇报帖子链接。若报 226/344/HTTP 0：先用 tw.py 核实是否实际发出；确认未发出则停止并汇报，不重试。

步骤4 - 养号点赞：每账号 3-5 个赞。用 tw.py / tw2.py search 搜"出海"或"AI出海"找 3 天内中文帖，挑点赞>10、内容正面相关的点赞，每次间隔 5 秒以上。两账号点赞集合尽量错开。

步骤5 - 评论互动（仅大号）：@TheEasySale1 可做 2-3 条评论（10-17 已验证评论功能正常）。找 24 小时内最热的出海/跨境/AI工具/eSIM类帖子（点赞>50或阅读>1万，避开抽奖/广告/政治），用 tw2.py reply 评论。每条中文、<150字、有实质观点和个人经验、不带链接、不硬广、不用emoji堆砌，口吻懂行。先读 ~/workspace/x-ops/commented.json 去重，做完后追加记录（含tweet_id、comment_id、account、时间）。单条失败可隔30秒重试一次，仍失败则停。不做：@bwrtuc084 自动评论（10-17 仍被软限制）、关注、私信。每账号发帖不超过 1 条。

汇报格式：分账号列出"状态检查结果、发了什么（附链接）、点了哪些赞、评了哪些帖（附链接）、遇到什么限制、下一步建议"。只陈述事实。
