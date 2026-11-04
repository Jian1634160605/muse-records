---
id: records-daily-sync
title: 每日记录同步到 GitHub
enabled: true
owner: goal:github-work-records-archive
mode: task
schedule:
  kind: daily
  timezone: Asia/Shanghai
  time: 21:00:00
delivery:
  - chat_id: 07b61800-4784-4c95-a4fe-19ac1fd1c9f3
metadata:
  originating_chat_context_json: '{"chat_id":"07b61800-4784-4c95-a4fe-19ac1fd1c9f3","origin_provider":"main","chat_kind":"direct","event_kind":"message","require_mention":false,"device_id":"0f867438-f925-4a26-98df-a9ce783f57a7"}'
  presentation_locale: zh-CN
---
每晚 21:00 把 Muse 工作记录同步到私有仓 Jian1634160605/muse-records（main 分支）。步骤：1）按既定口径重建暂存 ~/workspace/.records-stage：纳入 ~/MEMORY.md、USER.md、AGENTS.md、PROACTIVE_PREFERENCES.md、SOUL.md、IDENTITY.md、TOOLS.md、HEARTBEAT.md（→home/），~/memory/ 每日日志与 people/、groups/（→memory/），~/workspace/ 下的文本记录（.md/.txt/.json/.yaml/.yml）（→workspace/）；排除：凭据与密钥、媒体与二进制、缓存、浏览器会话数据（.hatch-browser）、运行时内部索引（memory/bank、memory/index）、备份（*.bak*）、虚拟环境、暂存目录本身与同步记录文件。2）把带账号密码的 URL 在暂存副本里打码为 http://<redacted-proxy>，不动原文。3）engage-log.md 单文件转义后超 8MB 推不上去，必须拆成两部分再推：part1 为“- 2026-10-29 19:36”这条之前的所有行（固定不变），part2 为该条起至文末（会继续增长），路径分别为 workspace/x-ops/engage-log-part1.md 与 engage-log-part2.md；不要推原始 engage-log.md。4）与 ~/workspace/.records-manifest.json 里的 sha256 对照，只推新增与变更文件；若 manifest 缺失则全量同步（同样遵守本条的拆分与分批规则）。5）用 github push-files 分批推送，每批转义后大小不超过 7.5MB（12.9MB 原始内容会报 413），提交信息注明日期与批次。6）成功后更新 manifest 与同步记录（~/workspace/.records-stage.muse-github-snapshot-sync.json，临时文件原子替换）。7）无变更不汇报；有推送或失败时向主聊简要汇报（推了几个文件、失败原因），不贴文件内容、不贴凭据。注意：push_files 不删除远端文件，本地已删文件不会从仓库清除；不要用 gh auth login 或 PAT。
