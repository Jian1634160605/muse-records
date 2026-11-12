# v4-B2 数据盯守台账 — Dr.qh88 面诊 v4-B2（Q-Muse Nose™ 鼻尖塑形）

- 账号：Dr.qh88 公共主页，CLI page_id `1398056210053725`，profile_id `61595415571609`
- 成片：`~/workspace/fb-ip/ai-video-batch-20261111-v4/v4-b2-nose-consult-10s-r2-fixed.mp4`（10.0 秒，720×1280，1 视频流+1 音频流），E07 94 分通过
- 发布状态：**已发布**：Dr.qh88 一条 Reel，post_id `122112560577513852`，链接 https://facebook.com/reel/1711238830423696/ ，发布时间 2026-11-12T01:38:13Z（北京时间 2026-11-12 09:38:13），文案英文 + 文案内注明 AI-generated video for illustration。封面已嵌在视频开头 2 秒、与视频同条发出。
- 首读：2026-11-12 09:43 CST（T+约5分钟），见下表首行。
- 自评引流评论：已发，comment_id `29247865031543692`，https://www.facebook.com/122112560577513852?comment_id=29247865031543692
- 规则：只报 facebook-cli 读到的数，不编数据；读不到写「未读到」；`value` 为 null 时只记 `rendered_text` 显示值，不做算术、不四舍五入冒充精确值；每次读数注明 as_of 与时间范围。

## 读取命令（每次用同一套）

```sh
/opt/hatch/bin/facebook-cli pages posts list --page-id 1398056210053725 --fields views,unique_viewers,engagements,engagements_including_clicks,clicks,link_clicks,saves --limit 5
/opt/hatch/bin/facebook-cli pages posts get --page-id 1398056210053725 --post-ids '122112560577513852' --fields views,unique_viewers,engagements,engagements_including_clicks,clicks,link_clicks,saves
/opt/hatch/bin/facebook-cli post read --post-id '122112560577513852'
/opt/hatch/bin/facebook-cli post comments read --post-id '122112560577513852' --limit 20
/opt/hatch/bin/facebook-cli post reactions read --post-id '122112560577513852'
/opt/hatch/bin/facebook-cli pages account-insights --page-id 1398056210053725 --time-range LAST_7D --metrics follower_count,views,unique_viewers,engagement_including_clicks,profile_visits,new_followers
```

## 读数时间点

- T+1h、T+6h、T+24h、T+48h（T=发布时间），之后每天一次，直至总管叫停。
- 每次读数后在下表追加一行；有值得报的变化（播放明显起量、评论出现问价/要联系方式/明确意向、分享突增）立即回传总管汇总，不自己发日报、不直接打扰老板。

## v4-B2 读数记录

| 读数时间（CST） | 距发布 | post_id / 链接 | views | unique_viewers | engagements | engagements_incl_clicks | clicks | link_clicks | saves | shares | comment_count | reactions | 备注（意向评论原文摘要） |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2026-11-12 09:43 | T+约5分钟 | 122112560577513852 / https://facebook.com/reel/1711238830423696/ | 0（显示） | 0（显示） | 0（显示） | 1（显示） | 0（显示） | 0（显示） | 0（显示） | 0 | 1 | 0 | 首读刚发出；评论 1 条为本号自评引流评论，无观众评论、无意向评论。as_of 2026-11-11T17:42:55-08:00；各指标 `value` 均为 null，此处记 `rendered_text` 显示值。注：同次 pages posts get 的 activity comment_count 显示 0，与 post read / comments read 的 1 条不一致，属读取口径时滞，以 comments read 为准。 |
| | T+1h（约10:38） | | | | | | | | | | | | |
| | T+6h（约15:38） | | | | | | | | | | | | |
| | T+24h（约09:38 次日） | | | | | | | | | | | | |
| | T+48h | | | | | | | | | | | | |

## 判断口径（给下一批的调整建议用）

- 好的放大：播放/互动明显高于基线（基线 views 9–53）的那类，下一批换新案例、同型放大。
- 连续垫底换型：播放/互动持续垫底的那类，下一批换角度/换患者/换画线重点，不重复同一条。
