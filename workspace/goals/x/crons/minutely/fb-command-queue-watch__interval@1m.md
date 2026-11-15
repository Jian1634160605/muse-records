---
id: fb-command-queue-watch
title: FB 园区命令队列盯守（1 分钟）
enabled: true
owner: goal:x
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-11-13T14:28:23
  every: 1m
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
每 1 分钟查一次 FB 园区（空间 fb-yun-ying-zhi-hui-zhong-xin-2）的新命令队列，让群聊里的命令有人接：

1. 先用 artifact.listpendingcommands 列出待处理命令，再用 artifact.getstate 看一眼当前快照（看当前是否暂停、Victoria 状态）。
2. 逐条处理：先 artifact.acknowledgecommand 认领，再按命令类型执行。拍板类：决定已记在后台，执行后续动作（发私信/发回复走 Messenger，发布走 facebook-cli 并核验送达才算发出）；派活类：按分工执行对应工作；发布/排期类：只有未暂停时才发；Bertie 已退役，任何 Bertie 的发布/派活一律拦下；执行完用 artifact.completecommand 写回执（outcome 用 done/blocked/failed，写清结果和原因），再用 artifact.postagentmessage 在群聊里回一句话。
3. FB 全线暂停期间（快照 opsStatus 写明暂停）：不执行任何 FB 对外动作，只认领并写 blocked 回执说明原因。
4. 主聊保持安静：只有需要老板动手（比如过安全检查、点审批卡、定夺）时才在主聊说一句；其余只在空间群聊里回执，没新命令时不汇报。
5. 不要编造执行结果，没发出去就写没发出去；不要重复执行已完成的命令。
