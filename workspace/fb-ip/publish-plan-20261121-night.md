# 今晚发布计划 2026-11-21（2 条/号/天，9 个号共 18 条）

## 背景（2026-11-21 08:16 成安定）
昨晚 14/18，4 条失败（Jusa 03a、Lark 05、Bertie 04、Bertie 04-alt-12s）因 02:00 备用档没有定时任务兜底而落空。成安定：**4 条并进今晚两轮一起发，不单设 02:00 定时任务**。
两轮定时任务（fb-ig-publish-round1 22:00、round2 00:00）的正文已同步改读本文件，不再读 2026-11-20 的旧表。

## 分配表（最终版，18 条）
排期原则：同一视频同一天最多发到同线 2 个账号；同一账号 7 天内不重复发同一视频；同一素材的两个版本不放同一账号。
- Bertie 只发 04，04-alt 改派 Jusa（04 与 04-alt 是同一原片 19.67s 的不同段落：04 是鼻子术后即刻，04-alt 是面诊段）。
- 其余 14 条用已发视频同线轮换（昨晚 12 个不同视频 + 02b 未用，今晚无新剪——新片产量缺口白天另补，见下）。
- 02b 7.87s 本晚不用：与 Victoria 第 2 条的 02-reorder-8s 是同一素材家族，避免同晚近重复。

| 账号 | 线 | 22:00 第 1 条 | 00:00 第 2 条 |
|---|---|---|---|
| Victoria p2 | 拉皮 | 02a Hafez 15s + fb02.txt | 02-reorder-8s 7.87s + mv-02-reorder.txt |
| Lark p32 | 拉皮 | 05 18s + fb05.txt（补发） | 01a 15s + fb01.txt |
| Oe p38 | 拉皮 | 01b 10.77s + fb01.txt | 03b 医生口播 10.33s + mv-03-hook.txt |
| Jusa p5 | 鼻子 | 03a CONTE 15s + fb03.txt（补发） | 04-alt-12s + mv-04-alt.txt（补发，改派） |
| Bertie p35 | 鼻子 | 04 15s + fb04.txt（补发） | 06 12.8s + fb06.txt |
| Ejje p67 | 鼻子 | N1 v4 17s + n1-recovery.txt | 06-n2-reverse 12.8s + mv-06-n2.txt |
| sarah p44 | 拉皮 | 03-hook-10s + mv-03-hook.txt | 05-hook-10s + mv-05-hook.txt |
| elaina p63 | 拉皮 | 01-f2-markings 10.77s + mv-01-f2.txt | 02a Hafez 15s + fb02.txt |
| gaga p65 | 鼻子 | 06 12.8s + fb06.txt | 03a CONTE 15s + fb03.txt（03a 今晚第 2 个账号） |

视频复用计数（今晚）：02a ×2（Victoria、elaina）、03a ×2（Jusa、gaga）、06 ×2（gaga、Bertie），其余 ×1，均在上限内。
昨晚已发（今晚不得重复发到同一账号）：FB：Victoria 01a/01-f2、Jusa 06-n2、Lark 05-hook、Oe 02a/02-reorder、Ejje 06/03-hook；IG：sarah 01b/02a、elaina 03b/05、gaga N1 v4/03b。

## 库存核实状态（⚠️ 未完成）
- ixBrowser agent 今早不可达（07:07 default-group-watch curl 52；08:2x 复核仍不通），成安电脑 `桌面\秦浩视频\未发视频\` 未盘点，文件在位情况今晚发前由发布轮次 ffprobe 核验（1 视频轨 + 1 音频轨，0 音轨不发）。
- 文案齐全：`~/workspace/fb-ip/captions/` 有 fb01–fb06、mv-01-f2、mv-02-reorder、mv-03-hook、mv-04-alt、mv-05-hook、mv-06-n2、n1-recovery。

## 执行要点（与昨晚相同）
- 发前 ffprobe 核验 1 视频轨 + 1 音频轨，0 音轨不发；文案已填才发。
- FB 用 `~/workspace/ixbrowser-driver/flows/fb_reel_publish_v4.py <profile_id> <video_path> <caption>`；IG 用 `ig_reel_publish.py`（先读其用法）。只传单个视频文件，不带封面。
- 打开浏览器后立即最小化；Bertie 绝不走 browser.browse，走 ixBrowser profile 35。
- 核验：FB 以 CLI timeline fetch / 通知页 "Your reel is published" 为准；核验不到绝不直接重试。IG 以 Reel 链接可访问为准。
- 发完每条做本号自评引流评论（不贴链接、不贴电话）；同平台其他号随后去看完播 + 顾客口吻评论。
- 结果记进 `~/workspace/fb-ip/publish-log-20261118.md`（续写），只汇报：发了几条、每条链接、失败的哪条 + 原因。

## ⚠️ 待补缺口（今晚之后）
- 今晚 18 条全是轮换、0 条新剪；轮换池（12 个视频）今晚基本用满 2 轮，明晚再排就得靠新片。**产量缺口：明天白天至少要剪 4–5 条新视频**（E07 新稿方向：R1 类 Day 7 揭晓帧开场再回 Day 0；钩子类真人实拍连续镜头主线 + AI 单帧示意插卡）。
- **02:00 备用档仍无定时任务**：今晚两轮若再失败，同样会落空。如需兜底，另设 fb-ig-publish-round3（02:00）定时任务，等成安定。
