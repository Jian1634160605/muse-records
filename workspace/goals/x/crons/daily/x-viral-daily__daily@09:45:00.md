---
id: x-viral-daily
title: X 每日爆款互动素材
enabled: true
owner: goal:x
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 09:45:00
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"227b032a-b42c-4f8c-ac2b-bbb839eb0dce","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"3a86e1ead60c505a"}'
  presentation_locale: en-US
---
每日 X 互动素材（只准备、不自动发布），只覆盖大号 @TheEasySale1（蓝V；小号 @bwrtuc084 已于 2026-10-23 删除，不再备它的素材）。步骤：1）用 browser.open 读取 https://xbangdan.com/ 首页，提取推文榜（24小时曝光）、长文榜（近7天收藏）、话题榜中与出海/跨境/账号基建/AI工具/搞钱相关度最高的3-5条爆款，记录作者、核心数据和链接。2）为 @TheEasySale1（带货口吻：懂行、给建议、偶尔提产品）写3条可直接粘贴的中文评论（每条<150字，有实质内容和个人观点，不带链接、不硬广、不用emoji堆砌，像真人；话题对口时可在末尾自引自己已发过的帖子）。3）仿照其中一条爆款的结构，写1条推广 chuhai.wiki 的帖子：结合站内真实商品与价格（Gmail老号、ChatGPT Plus纯手工成品号66、Claude Pro月续168、Gemini Pro成品号40、X蓝V月续66、Codex接码），文末带 chuhai.wiki 纯文本，不放超链接。4）在当前聊天汇报：爆款摘要（含链接）+ 3条评论草稿 + 1条推广帖草稿。严禁自动发帖、严禁自动评论、严禁修改 queue.json / promo-queue.json / commented.json。安全口径（2026-10-23 用户定）：互动和发帖不设自设数量上限，按账号存活和内容质量把握，平台出限制信号即停号；但不做几百条/天那种批量 spam 刷量（用户此前明确拒绝，属刷量行为、会毁号）。
