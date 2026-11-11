# V1 数据盯守台账 — Dr.qh88 面诊 V1（Q-Muse Nose™）

- 账号：Dr.qh88 公共主页，CLI page_id `1398056210053725`，profile_id `61595415571609`
- 标杆成片：`~/workspace/fb-ip/ai-video-batch-20261111-v3/v1-nose-consult-10s-cover-r3.mp4`（10.0秒，0–2秒封面+2–7秒面诊+7–10秒尾卡，720×1280，单音轨纯音乐），E07 第4轮 94分通过
- 封面：`~/workspace/fb-ip/ai-video-batch-20261111-v3/v1-cover-qmuse-nose-alt-c-1280.png`
- 发布状态：**已发布**：Dr.qh88 一条 Reel，post_id `122112357993513852`，链接 https://facebook.com/reel/1611977133404199/ ，发布时间 2026-11-11T10:43:57Z（北京时间 18:43:57），文案英文 + 文案内注明 AI-generated video for illustration。封面已嵌在视频开头 2 秒、与视频同条发出。
- 首读：2026-11-11 18:44:24 CST（T+约1分钟），见下表首行。
- 规则：只报 facebook-cli 读到的数，不编数据；读不到写「未读到」；`value` 为 null 时只记 `rendered_text` 显示值，不做算术、不四舍五入冒充精确值；每次读数注明 as_of 与时间范围。

## 读取命令（每次用同一套）

```sh
/opt/hatch/bin/facebook-cli pages posts list --page-id 1398056210053725 --fields views,unique_viewers,engagements,engagements_including_clicks,clicks,link_clicks,saves --limit 5
/opt/hatch/bin/facebook-cli pages posts get --page-id 1398056210053725 --post-ids '<V1 post_id>' --fields views,unique_viewers,engagements,engagements_including_clicks,clicks,link_clicks,saves
/opt/hatch/bin/facebook-cli post read --post-id '<V1 post_id>'
/opt/hatch/bin/facebook-cli post comments read --post-id '<V1 post_id>' --limit 20
/opt/hatch/bin/facebook-cli post reactions read --post-id '<V1 post_id>'
/opt/hatch/bin/facebook-cli pages account-insights --page-id 1398056210053725 --time-range LAST_7D --metrics follower_count,views,unique_viewers,engagement_including_clicks,profile_visits,new_followers
```

## 读数时间点

- T+1h、T+6h、T+24h、T+48h（T=发布时间），之后每天一次，直至总管叫停。
- 每次读数后在下表追加一行；有值得报的变化（播放明显起量、评论出现问价/要联系方式/明确意向、分享突增）立即回传总管汇总，不自己发日报、不直接打扰老板。

## 基线（V1 发出前，2026-11-11 18:44 CST 读到，as_of 2026-11-11T02:44:02-08:00）

| 帖子 | 发布时间 | views（显示） | unique_viewers（显示） | engagements | engagements_including_clicks | clicks | shares | comment_count | reactions |
|---|---|---|---|---|---|---|---|---|---|
| 122111737455513852 “Cheeks, jawline, chin — balance…” | 2026-11-09T09:03:39Z | 44 | 1 | 0 | 6 | 6 | 0 | 0 | 0 |
| 122111147163513852 “Full-face balance for men…” | 2026-11-07T12:59:58Z | 53 | 4 | 0 | 12 | 12 | 0 | 0 | 0 |
| 122111116839513852 “A mature full-face refresh…” | 2026-11-07T11:02:58Z | 41 | 12 | 1 | 10 | 9 | 1 | 0 | 0 |
| 122111086779513852 “Before, mapped, after — lips…” | 2026-11-07T08:57:48Z | 15 | 3 | 0 | 1 | 1 | 0 | 0 | 0 |
| 122111012727513852 “Every millilitre has an address…” | 2026-11-07T03:47:51Z | 9 | 4 | 0 | 1 | 1 | 0 | 0 | 0 |

注：以上 `value` 字段均为 null，此处记的是返回的 `rendered_text` 显示值，仅作基线对照，不用于算术。

## V1 读数记录（待填）

| 读数时间（CST） | 距发布 | post_id / 链接 | views | unique_viewers | engagements | engagements_incl_clicks | clicks | link_clicks | saves | shares | comment_count | reactions | 备注（意向评论原文摘要） |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2026-11-11 18:44:24 | T+约1分钟 | 122112357993513852 / https://facebook.com/reel/1611977133404199/ | 0（显示） | 0（显示） | 0（显示） | 0（显示） | 0（显示） | 0（显示） | 0（显示） | 0 | 0 | 0 | 首读刚发出，`post read` 核对：Dr.qh88、public、文案与总管给的一致；评论 0、点赞 0。as_of 2026-11-11T02:44:24-08:00；各指标 `value` 均为 null，此处记 `rendered_text` 显示值。 |
| — | T+1h（约19:44） | 122112357993513852 | 未读到 | 未读到 | 未读到 | 未读到 | 未读到 | 未读到 | 未读到 | 未读到 | 未读到 | 未读到 | 本任盯守员接替时该时点已过、无记录可补，不编数。 |
| 2026-11-11 20:43:16 | T+2h | 122112357993513852 / https://facebook.com/reel/1611977133404199/ | 79（显示） | 44（显示） | 1（显示） | 1（显示） | 0（显示） | 0（显示） | 0（显示） | 1 | 0 | 0 | 起量初现：views 显示 79 已超基线最高 53（基线 9–53），unique_viewers 显示 44 超基线最高 12（基线 1–12）；shares 由首读 0 变 1；评论 0、点赞 0，无意向评论；自评引流评论未见（评论区 0 条，按 routine 应补一条）。as_of 2026-11-11T04:43:14-08:00（posts list/get）；post read retrieved 20:43:16 CST；各指标 `value` 均为 null，此处记 `rendered_text` 显示值，不做算术。 |
| | T+6h（约00:44） | | | | | | | | | | | | |
| | T+24h（约18:44 次日） | | | | | | | | | | | | |
| | T+48h | | | | | | | | | | | | |

## 判断口径（给下一批的调整建议用）

- 好的放大：播放/互动明显高于基线（基线 views 9–53）的那类，下一批换新案例、同型放大。
- 连续垫底换型：播放/互动持续垫底的那类，下一批换角度/换患者/换画线重点，不重复同一条。
- 唯一目标是获客：评论区出现问价/在哪里做/项目/医生/预约/恢复/想做等真实意向，立即标出并回传总管；合格客资定义不变（带国家区号 WhatsApp + 国家）。
- 迭代到爆为止：每批发出后按本表数据调下一批，不凭感觉改。
