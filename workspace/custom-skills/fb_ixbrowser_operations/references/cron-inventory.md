# 定时任务清单（2026-11-17 15:08 实测）

这些任务跑在 Muse 的调度器里，不在电脑上；新电脑只要 agent + Concat 桥装好、Muse 登记了 IP/令牌就能接管。
完整任务正文不在包里（在 Muse 侧），这里是清单，照单重建时按此表。

## 在跑（启用）

| 任务 | 频率 | 作用 |
|---|---|---|
| fb-command-queue-watch | 1 分钟 | FB 园区命令队列盯守，群聊命令有人接 |
| fb-command-center-daily-refresh | 每天 09:45 | FB 园区每日刷新 |
| fb-competitor-watch | 10 分钟 | 同行监控猎手（Victoria 线） |
| fb-dm-thread-watch | 5 分钟 | 私信线程盯回复（Anne/Judi 等） |
| fb-lead-scan | 1 小时 | 客户雷达（新好友差分、好友请求核查） |
| fb-engage-daily | 24 小时 | FB 每日互动养号 |
| fb-warm-am / noon / pm | 每天 10:45 / 14:45 / 18:45 | 养号刷视频三场 |

## 停用（待按 ixBrowser 方案重写或等老板拍板）

| 任务 | 频率 | 备注 |
|---|---|---|
| fb-content-daily | 24 小时 | FB 每日内容（旧版） |
| ai-video-publish-2h | 2 小时 | AI 面诊视频轮流发布 |
| fb-foxprofile-warm-daily | 每天 15:45 | 旧 FoxProfile 养号（方案已删） |
| fb-newpages-post-daily | 每天 18:45 | 旧新主页发布（FoxProfile 方案已删） |
| fb-touche-queue-publish(-19/-21) | 每天 17:00/19:00/21:00 | Touché 排期发布 |
| ig-gaga-watch / ig-gaga-dm-watch | 10 分钟 / 5 分钟 | IG gaga 猎手/私信盯守（待重写启用） |
| ig-sarah-watch / ig-sarah-dm-watch | 10 分钟 / 5 分钟 | IG sarah 猎手/私信盯守（待重写启用） |
| ig-haze-watch / ig-haze-dm-watch | 10 分钟 / 5 分钟 | IG haze 猎手/私信盯守（号被锁，待恢复） |
| ig-competitor-engage | 3 小时 | IG 同行评论区截流 |
| ig-warm-am / noon / pm | 每天 11:45/13:45/15:45 | IG 养号三场 |
| ig-matrix-post-r1/r2/r3 | 每天 17:45/19:45/22:45 | IG 矩阵发布轮次 |
| ig-matrix-prep-daily | 每天 09:45 | IG 每日备料 |
| ig-lead-watch | 30 分钟 | TikTok 评论私信巡查 |

## 10 号铺开后的任务数

每号猎手 + 私信 2 个任务，共 20 个（Jusa/Lark/pokk/elaina + Emerson/38/67/80 共 8 号新建 16 个；gaga/sarah 重写启用 4 个；Victoria 已有自己的、不计）。是否现在建并启用，等老板拍板。
