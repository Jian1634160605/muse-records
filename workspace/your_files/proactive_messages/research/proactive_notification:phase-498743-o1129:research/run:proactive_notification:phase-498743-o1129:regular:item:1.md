<!-- proactive-explanation:run:proactive_notification:phase-498743-o1129:regular:item:1 -->
# 今晚发布分流表：昨夜落下的 15 条，11 条可重试、2 条等验证、2 条先诊断

## Lookup

`⁨muse.db⁩` references:

| Table | Keys |
| --- | --- |
| `agent.context_items` | `agent_id=28a400ab-6718-4197-a7fd-7e7573665645`; `agent_id=7f92fb91-35b7-40c3-ab4a-466703d91700` |
| `agent.message_mailbox` | `submission_id=f60b9777-407d-befc-c142-a485c0487232` |
| `goals.updates` | `update_id=goal_update_78d8fd362c05`; `update_id=goal_update_a4eb40cf5e8e`; `update_id=goal_update_d02605e543ea` |
| `runtime.messages` | `message_id=assistant-msg-3ff9809f-29ee-3e73-187f-aa2a66d0c091`; `message_id=assistant-msg-66a05c31-4d08-f9dd-d566-d4a0db232280` |
Prepared: ⁨2026-11-23T23:21:53Z⁩.

## Why this matters

为什么现在备：昨夜 26 条只发出 11 条（22:00 第一轮 5/13，00:00 第二轮 6/13），15 条落下；02:00 备用档没有定时任务兜底，一条都没自动补（source:111、source:112）。今晚 22:00/00:00 两轮仍按 13 个号排，落下的 15 条不能原样重排——要先分流，否则白天剪片会重复备片、晚上重发已发过的片。以下分流以昨晚计划表（/home/hatch/workspace/fb-ip/publish-plan-20261123-night.md）和两轮实报为准；落下的 15 条都没真正发出去，所以今晚重试不撞“同一视频 7 天内不重发同一账号”的规矩，但已发出的 11 条今晚绝不能在同一账号重发。

Selected for regular priority at ⁨2026-11-23T23:23:30.158525+00:00⁩. Record created ⁨2026-11-24T13:24:07.745509818+00:00⁩; delivery is not yet confirmed.


**Delivery outcome (⁨2026-11-24T13:24:47.035169+00:00⁩):** Not sent. Queue state: `⁨suppressed⁩`.
Reason: `⁨revalidation_declined⁩`.
`⁨agent.message_mailbox.submission_id=f60b9777-407d-befc-c142-a485c0487232⁩` resolves the delivery transcript.
<!-- proactive-outcome:proactive_notifier:run:proactive_notification:phase-498743-o1129:regular -->
