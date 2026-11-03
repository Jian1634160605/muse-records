# 音乐池补货测试批 — 2026-10-23（yt-dlp 工具链实测）

工具：yt-dlp（专用 venv：~/workspace/tools/bgm-dl/.venv，版本 2026.10.21）+ 系统 ffmpeg 8.1.2。
下载走 FB 静态代理（命令示例见下）。本批 3 条均已 ffprobe 验证音频流正常，并通过实际换轨
冒烟测试（queue/2026-10-23/v1.mp4 + bgm-chill-liqwyd.mp3 → h264+aac，54s，正常）。

| 文件 | 来源 | 风格类型 | BPM(librosa 实测) | 时长 | 适用 |
|---|---|---|---|---|---|
| bgm-chill-liqwyd.mp3 | SoundCloud: LiQWYD - Chill（作者官方号，Free download） | 现代 chill / 轻电子 lo-fi，纯音乐 | ≈144（半速体感约 72，chill 律动） | 2:54 | 日常/恢复记录/vlog 感片段 |
| bgm-space-ambient.mp3 | SoundCloud: Royalty Free Music BTM - Space Ambient | 氛围 ambient，纯音乐，无明显节拍点 | ≈117（检测值，ambient 节拍不明显） | 2:48 | 对比展示/科普/舒缓叙事 |
| bgm-epic-inspiring.mp3 | SoundCloud: Royalty Free Music BTM - Epic Inspiring | 电影感励志 cinematic，纯音乐 | ≈86 | 2:59 | 爆点前置/医生出镜/案例高潮 |

选曲标准（用户 2026-10-23 定）：对标爆款风格换同类曲，不用原曲；不用低质土嗨、不用老气过时；
要现代、轻快或有氛围感。本批已按此筛：首轮下载的 Boom Bap 复古嘻哈一条因偏老派已剔除替换。

许可提示：LiQWYD 曲目为作者免费授权（通常 CC BY，需署名——发布时可在文案/评论区加一行
"Music: LiQWYD - Chill"）；Royalty Free Music BTM 频道曲目标注 royalty free。使用前按各曲
详情页许可再确认一次。

补货命令示例（代理值不落盘、不打印）：
  export HTTPS_PROXY="$(cat ~/.agent-reach/proxy-fb.txt)" HTTP_PROXY="$(cat ~/.agent-reach/proxy-fb.txt)"
  ~/workspace/tools/bgm-dl/.venv/bin/yt-dlp -x --audio-format mp3 --audio-quality 192K \
    -o "~/workspace/ig-ops/christycrawford85/music_pool/<名>.%(ext)s" "<SoundCloud/视频页 URL>"
  搜索候选：yt-dlp --flat-playlist "scsearch8:<关键词>" 或 "ytsearch8:<关键词>"

已知坑：YouTube 经该静态代理 IP 会频繁撞 "Sign in to confirm you're not a bot"
（实测 3 条仅 1 条漏网，换 player_client 参数无效）——补货优先走 SoundCloud，
YouTube 只作备选；SoundCloud 搜索偶发超时，重试即可。
