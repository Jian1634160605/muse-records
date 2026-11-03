---
id: fb-newpages-post-daily
title: 4 个新主页每日发布（FoxProfile）
enabled: true
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 18:45:00
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
把今天备好的内容发布到 4 个新主页上（2026-10-22 用户指令：4 个新号正式纳入日常运营）。

**2026-10-26 18:45 轮次限定（用户 15:54 定）**：本轮只发 Jioklm（fb-73057）和 Jusa（fb-91565）；Simon（fb-75128）、Cora（fb-54124）环境打不开（重测确认），本轮跳过两号，不计失败、不重复上报。本条仅限 2026-10-26 18:45 这一轮，之后轮次按原规则执行。

**备料来源（2026-10-25 路径修正）**：~/workspace/ig-ops/christycrawford85/queue/<今天日期>/ 根目录的 pages-captions.md（每个主页一节，标注类型 VIDEO 或 TEXT）；VIDEO 对应的视频文件在同目录 pages/ 子目录里（p73057.mp4 / p91565.mp4 / p75128.mp4 / p54124.mp4），TEXT 的文字帖全文在 pages-captions.md 该节里。队列或某主页的料不存在，就跳过该主页并在报告里注明缺料，不要拿别的文件顶替。

**先审后排（硬门槛，2026-10-24 用户定）**：每个主页发之前，先读 pages-captions.md 对应主页节，只有该节内出现『用户已批准』字样（主代理在用户点头后写入，带日期时间）才发该主页；没有该字样 = 未批，跳过该主页并在报告里注明『未批，跳过』，绝不自动发。

**防重复**：先看同目录 posted-pages.txt，某主页今天已有发布记录就跳过该主页。

**发布通道（FoxProfile，一号一环境，绝不串号）**：
- 先 curl 127.0.0.1:8000/api/v1/profiles 检查 FoxProfile 服务；没起就用 ~/workspace/foxprofile/start-server.sh 启动（setsid 托管），再继续。
- fb-73057（Jioklm Dersx）→ 主页「Dr. Qin Hao Facelift & Facial Rejuvenation」61595888184080
- fb-91565（Jusa Khan）→ 主页「Dr. Qin Hao Eye Rejuvenation」61595765429611
- fb-75128（Simon Dyer）→ 主页「Dr. Qin Hao Rhinoplasty & Nose Reshaping」61595900453604
- fb-54124（Cora Gleichner）→ 主页「Dr. Qin Hao Body Contouring」61595343737797
- 逐个环境处理：启动该环境 → 打开 facebook.com 确认登录的是该号本人（会话落一键登录页「Continue <姓名>」可直接点 Continue 恢复，用户已长期授权；若要输密码或出现验证码/checkpoint，立即停该号、记录现象、跳到下一个号，绝不硬闯）→ 切到主页身份 → 发布 → 停环境，再处理下一个。

**发布方式**：
- VIDEO：走主页自己的 Reels 创建入口上传成品文件（个人号的 /reel/create 直发主页不行，用主页 /reels/create/ 入口或主页 Reels 页签的上传入口；上传走真实文件输入）。成品在备料阶段已嵌入音乐，直接上传，不要进平台曲库找音乐、不要加平台音乐、不要静音。
- TEXT：主页发帖框发文字帖，全文照 pages-captions.md 该节内容。
- 文案用 pages-captions.md 对应主页那一节的 FB 文案，一字不改地用。

**核验与记录**：每条发完确认发布成功、拿到帖子/Reel 链接，把「主页ID + 类型 + 链接」追加写入 posted-pages.txt。4 个主页都处理完后向主聊天报告：每个主页发了什么、链接是什么；失败的说明卡在哪一步、什么现象，不要盲目重试超过 1 次。代理瞬时抖动（ProxyUnreachable）先复测线路再重试启动一次，不要直接判线路死。

**红线**：只发布，不评论、不私信、不加好友、不进群、不邀请任何人；不改主页任何设置。
