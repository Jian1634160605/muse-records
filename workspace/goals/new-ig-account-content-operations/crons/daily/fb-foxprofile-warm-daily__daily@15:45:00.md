---
id: fb-foxprofile-warm-daily
title: FoxProfile 六号每日养号轮换
enabled: false
owner: goal:new-ig-account-content-operations
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 15:45:00
delivery:
  - chat_id: 2e7b7db1-0363-40bc-8c95-f4cb3b432c25
metadata:
  tags: [cron:flexible-time]
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
FoxProfile 六个环境的每日养号轮换（2026-10-22 用户指令：4 个新号纳入日常运营；Fowler/Emerson 一并纳入轮换）。目标：让每个号都像真人一样有日常浏览活动，养权重、保会话。

**轮换名单（一号一环境，逐个处理，绝不串号）**：
- fb-73057（Jioklm Dersx，新号·拉皮主线）
- fb-91565（Jusa Khan，新号·眼部）
- fb-75128（Simon Dyer，新号·鼻部）
- fb-54124（Cora Gleichner，新号·身体塑形）
- fb-3651（Fowler Ariana）
- fb-6399（Emerson Ciara）

**每个环境的养号动作（约 8–10 分钟）**：
1. 先 curl 127.0.0.1:8000/api/v1/profiles 检查 FoxProfile 服务；没起就用 ~/workspace/foxprofile/start-server.sh 启动（setsid）。代理瞬时抖动（ProxyUnreachable）先复测再重试启动一次。
2. 启动该环境，打开 facebook.com 确认登录的是该号本人。会话落一键登录页「Continue <姓名>」可直接点 Continue 恢复（用户已长期授权）；若要输密码、出现验证码或 checkpoint，立即停该号、记录现象、跳下一个，绝不硬闯。
3. 像真人一样浏览：首页动态 + Reels，以医美/拉皮/抗衰垂类为主，视频看大半再划走；推荐流跑偏就搜 facelift 把垂类拉回来。点赞 3–5 条垂类优质内容（间隔拉开，不要连点）。
4. 停环境，处理下一个。

**红线（只养号）**：不评论、不私信、不加好友、不进群、不发帖、不点广告、不改任何设置。发帖由发布任务负责，评论/私信由猎手与私信任务负责，本任务一律不碰。

**汇报**：向主聊天报告每个号的养号结果（浏览/点赞完成情况）和异常（会话过期、验证、代理问题分别注明是哪个号）。全部正常且无异常时可简短汇报。
