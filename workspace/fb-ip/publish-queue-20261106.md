# 发布排期 · 2026-11-06（用户 17:20 定：先发 96 分草稿，其余成片每 2 小时发一个）

- Peta Bentley：后端咨询已联系客户，Muse 停止跟进（2026-11-06 17:20 用户定）。
- 目标账号：只发 Victoria / Dr.qh88（page_id 1398056210053725）。
- 方式：facebook-cli pages posts create；文字帖直接发，视频（单 MP4）即 Reel；定时用 --scheduled-publish-time（Unix 秒）。

## 队列

| # | 内容 | 形式 | 时间 | 状态 |
|---|------|------|------|------|
| 1 | 恢复期科普文字帖（E07 96 分，2026-11-04 稿，收口“在本主页发消息”） | Dr.qh88 文字帖 | 2026-11-06 17:33 立即发 | ✅ 已发并核验：post_id 122110787859513852，state published，作者 Dr.qh88，原文一字未改。链接 https://facebook.com/61595415571609/posts/pfbid033dmww5wYQAGH92ECR49PAzgFA4uRH85U55WBULeqvvSECaTE8yQYa9qiYhbKP2sRl/ |
| 2 | 105202-cut.mp4（35.4 秒，竖屏，口播原声，英文字幕已烧录，只发 Victoria） | Dr.qh88 Reel | 2026-11-06 19:45 | ✅ 已发并核验：19:55 CLI 查 state published（2026-11-06 19:45 发布），views 1、engagements 0、reactions 0、shares 0、comments 0（发布约 10 分钟后数据） |
| 3 | 用户 11-06 17:07 发到 FB 旁聊的 22 条视频（全脸注射前后对比） | Dr.qh88 + Victoria 个人号 | 待定 | ✅ 用户 17:24 已确认原样加小水印发，17:28 定封面取最后 2 秒最佳帧；01 号已于 11-06 17:45 提前发出（用户令），其余 21 条按每 2 小时一条排至 11-08 15:45，详见 ~/workspace/fb-ip/touche-batch/queue.md，定时任务 fb-touche-queue-publish 接管 |
| 4 | （空）用户再给新成片时按 2 小时间隔续排 | — | — | — |

## 备注

- 96 分草稿原文未落盘文件，正在 FB 旁聊 2026-11-04 19:54 fb-content-daily 汇报里找回；找回后核对 ≤1024 字符再发，不改原文。
- 105202 用户 2026-11-01 已定只发 Victoria；2026-11-06 17:20 用户令逐个排期发布，即为点头。
- 发完逐条核验（state: published + 帖子链接），记 daily-table；两条发完成品库存归零。
