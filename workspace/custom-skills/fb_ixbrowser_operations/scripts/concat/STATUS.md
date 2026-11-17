# Concat 剪辑 — 状态

专案对话：Concat 剪辑（side chat 6b978705-28b0-47f6-a545-d7ce98a9ad82）。主对话只下指令和听汇报；这里有进展就同步一份简报回主对话，标题写清是 Concat 剪辑。

## 通路（已验证）

- 用户电脑桥：`D:\ixbrowser-agent\concat_bridge.py`，端口 8766，开机自启。
- Muse 侧客户端：`~/workspace/tools/concat/concat_client.py`（ConcatBridge 类）。
- 2026-11-16 冒烟全通：建项目 → 导视频 → 上时间线 → 加标题 → 导出一次跑通，成品 1080×1920 h264 30fps 9.7 秒。
- 2026-11-17 13:25 复核：桥 health 正常（`ok: True, mcp_running: True`）。
- 今后剪辑一律走 Concat 经桥，不再手拼 ffmpeg。成片仍过 E07 90 分门。

## 等用户定的三件事（2026-11-17 07:41 首问、12:26 合并重提，至今未回）

1. 首批剪哪批素材：桌面 `3d动画鼻子` 5 条 / `fabuneir` 原片 / 等新素材
2. 一次剪几条：是否按 5 条起步，16:00 起排、间隔 2 小时、错开几分钟
3. IG 连接链接今天点不点：不点则新视频 IG 发不出去，只能先发 FB

用户定了就直接动手剪，不用再回主对话请示。

## 发布口径（沿用已定规则）

- 视频统一 16:00 起发，每条间隔 2 小时；同一轮次内各账号错开几分钟，不许同一秒齐发。
- 一个视频 = FB + IG 两个平台才算发完；发布一律走后台（FB 用 facebook-cli 单个视频文件发 Reel，不带封面；IG 用 instagram-cli 带封面）。
- IG Reel 目前 blocked：gaga5456 未连 instagram-cli，须用户点连接链接后才能发。
- 视频文案由 Muse 写（对外英文，钩子+具体设计点+互动问题，AI 视频注明 AI-generated video for illustration）。
- 发完立即发自评引流评论 + 各号互相看完播率。
