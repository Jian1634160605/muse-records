---
id: tiktok-peer-engage
title: TikTok 同行评论区专业截流
enabled: false
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-10-21T13:01:16
  every: 2h
timeout_secs: 1800
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"f1ccfbbd-1f77-4a79-882a-c4290f0d03df"}'
  presentation_locale: zh-CN
---
在 TikTok 上去同行爆款视频的评论区主动获客，账号 @faciallifting.qinhao。用浏览器已登录会话。

目标：TikTok 上做 facelift、deep plane facelift、rhinoplasty 的医生账号的高播放（爆款）视频（可用站内搜索找最近爆款）。

做法：
- **开工先查私信/通知**：我们主动联系过的人有没有回复，有回复先按下方沟通 SOP 继续聊，别晾着人家。
- 在爆款视频评论区找有购买意向的评论（问价格、问恢复期、问在哪做、要联系方式、求推荐医生）。
- **评论回复**：以医生团队的专业口吻给实质解答（英文，简洁，1–3 句）；不在评论里贴链接、电话或 WhatsApp 号码；不贬低同行。
- **主动私信（2026-10-21 用户新规，不再等客户上门）**：对公开表达过明确意向的人，可以直接发 TikTok 私信：提一句看到他在 XX 视频下的留言，简短专业答疑，问他在哪个国家/城市、想改善哪个部位，引导他点主页链接咨询、或留 WhatsApp 号码。他回复后持续沟通（价格只给"depends on your case, needs doctor assessment"这类范围说法，不报死价；不做病情诊断、不承诺效果）。**注意**：TikTok 私信需要对方开启接收或互关，发不出去时改用评论回复引导到主页链接，不要反复尝试。**拿到 WhatsApp 号码、或对方明确想咨询/预约并给了国家信息 = 合格客资**：立刻记入 ~/workspace/ig-ops/christycrawford85/leads.md（时间/平台/账号名/国家/意向/联系方式），并在报告里报给用户。
- **数量控制**：评论+私信**合计**每轮最多 2 个动作、条条不同视频/不同的人，且全天累计不超过 6 个——开工前先读去重台账 ~/workspace/goals/new-ig-account-content-operations/hidden_files/tiktok-engage-seen.md 数今天的条数（评论和私信都记账），达到上限跳过本轮；评过/私信过的视频、评论、人记入台账，绝不重复触达同一个人
- **人机验证（打法二）**：遇到验证挑战先自己尝试，最多 2 次；仍不过立刻停下并报告"需要用户接管浏览器"
- 出现任何操作受限提示：立即停下并报告
- 有实际评论/私信或被拦截时才向主聊天报告（动作明细、链接+要点、回复/客资情况）；没有合适目标时保持安静
