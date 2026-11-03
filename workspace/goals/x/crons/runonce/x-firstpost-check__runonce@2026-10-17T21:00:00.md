---
id: x-firstpost-check
title: X 首帖数据回看（一次性）
enabled: true
owner: goal:x
mode: task
schedule:
  kind: runonce
  timezone: Asia/Shanghai
  at: 2026-10-17T21:00:00
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  originating_chat_context_json: '{"origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false}'
  presentation_locale: zh-CN
---
你是 @bwrtuc084 的 X 账号运营助手。今晚 17:12（北京时间）账号发出了第一条帖子（draft 1，tweet_id 2111384538215756122，链接 https://x.com/bwrtuc084/status/2111384538215756122），用户非常关注这条首帖的早期数据。你的任务是一次性回看这条帖子的表现：

1. 用 `python3 ~/workspace/x-ops/tw.py` 调用 twitter-cli（它会自动从 ~/.agent-reach/config.yaml 读取鉴权）。先用只读方式找到查看单条 tweet 的子命令（可试 `twitter --help` 或 `tw.py --help`，找类似 tweet/show/status 的读命令）。只用读命令，绝不发帖、评论、点赞或做任何写操作。
2. 获取该 tweet 的展示/阅读量、点赞、转推、回复、收藏数据。只查一次，不要轮询重试。
3. 如果读取失败（网络、鉴权或平台风控拦截）：不要重试，不要给用户发任何消息，本次任务直接安静结束。
4. 读取成功：给用户发一条简短中文汇报：发帖约 4 小时后的核心数据（阅读、点赞、转推、回复），一句话解读（5 粉新号首帖的合理预期），下一步建议（7 条剩余草稿继续保持暂停，等用户决定；不要提议自动恢复排期）。绝不复述帖子全文。

注意：这是 runonce 一次性任务，完成后即结束，不要安排任何后续检查。
