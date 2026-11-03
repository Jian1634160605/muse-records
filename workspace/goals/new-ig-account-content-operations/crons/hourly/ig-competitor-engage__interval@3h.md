---
id: ig-competitor-engage
title: IG 同行评论区专业截流（每日）
enabled: false
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: interval
  timezone: Asia/Shanghai
  at: 2026-10-21T14:00:44
  every: 3h
timeout_secs: 1800
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:automatic-interval-anchor]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"f1ccfbbd-1f77-4a79-882a-c4290f0d03df"}'
  presentation_locale: zh-CN
---
在 Instagram 上去同行爆款 Reel 的评论区主动获客，账号 lillieflores24（2026-10-21 接管的新号）。用浏览器已登录会话。

**首要目标：@internationalplasticsurgery916**（用户 2026-10-21 指定优先）——她的高播放 Reel（恢复时间线 149 万播放那条、近期 47 万那条等）的评论区优先扫。其他目标账号（拉皮同行）：doctor.truesdale、nayakplasticsurgery、reface_scarless、drkassir、dra.camimartinez、toropclinic、dr.zhang.3u、@tan.iasampson。挑他们最近的高播放 Reel。

做法：
- **开工先查私信收件箱**：我们主动联系过的人有没有回复，有回复先按下方沟通 SOP 继续聊，别晾着人家。
- 在爆款 Reel 评论区找有购买意向的评论（问价格、问恢复期、问在哪做、要联系方式、求推荐医生）。
- **评论回复**：以医生团队的专业口吻给实质解答（英文，简洁，1–3 句），结尾自然引导一句：主页有 WhatsApp 咨询链接（"Consult link is in my bio"这类说法）。
- **主动私信（2026-10-21 用户新规，不再等客户上门）**：对公开表达过明确意向的人（问价、要联系方式、说想做），可以直接发 IG 私信：提一句看到他在 XX Reel 下的留言，简短专业答疑，问他在哪个国家/城市、想改善哪个部位，引导他点主页链接咨询、或留 WhatsApp 号码。他回复后持续沟通（价格只给"depends on your case, needs doctor assessment"这类范围说法，不报死价；不做病情诊断、不承诺效果）。**拿到 WhatsApp 号码、或对方明确想咨询/预约并给了国家信息 = 合格客资**：立刻记入 ~/workspace/ig-ops/christycrawford85/leads.md（时间/平台/账号名/国家/意向/联系方式），并在报告里报给用户。
- **禁止**：在评论里贴链接、贴 WhatsApp 号码、留电话；禁止私信没有意向的路人；禁止贬低同行。
- **数量控制（新号保护，最重要）**：评论+私信**合计**每轮最多 2 个动作，且全天累计不超过 5 个——开工前先读去重台账 ~/workspace/goals/new-ig-account-content-operations/hidden_files/ig-engage-seen.md 数今天的条数（评论和私信都记账），达到上限就跳过本轮。评过/私信过的帖子、评论、人记入该台账，绝不重复触达同一个人。
- **出现任何"操作受限/稍后再试"类提示：立即停下，本轮不再触达，并在报告中明确说明**（旧号就是栽在评论风控上，新号宁可慢）
- 完成后向主聊天简报：评了哪几条、私信了谁、有没有回复/客资（帖子链接+要点）；没有合适目标就安静跳过并简单说明
