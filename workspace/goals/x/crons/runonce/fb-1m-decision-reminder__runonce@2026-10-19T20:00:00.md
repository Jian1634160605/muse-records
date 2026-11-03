---
id: fb-1m-decision-reminder
title: 100万播放投放拍板提醒（10-20中午前）
enabled: true
owner: goal:x
mode: task
schedule:
  kind: runonce
  timezone: Asia/Shanghai
  at: 2026-10-19T20:00:00
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  originating_chat_context_json: '{"origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false}'
  presentation_locale: zh-CN
---
背景：2026-10-18 用户确认了 FB 100 万播放冲刺的投放三选一，**10-20（周二）中午之前必须拍板**：A 有老广告户+预算批了 → 12 天可行，Muse 出加热执行方案；B 有预算没老户 → 走代投白名单户，Muse 出甄别清单；C 都没有 → 纯 organic 冲刺（100 万大概率到不了，但内容沉淀照做）。

本次任务：先用 muse.memory_search 查 2026-10-18 之后用户是否已对投放拍板（关键词：投放 / 广告户 / 预算 / 代投 / 加热）。若用户已明确选择 → 静默结束，什么都不发。若仍未拍板 → 用中文发一条简短提醒（不要长篇）：明天（10-20）中午是拍板时限，今晚可先确认两件事——有没有现成的老广告户、预算批没批；定下来我这边 10-29 才能准时加热。
