# VideoSeek — 本地视频语义检索（无头部署）

在本地视频库里用**中文一句话**或**一张参考图**找镜头，返回 `视频路径 + 起止秒/时间码`，还能按命中导出 mp4 片段、抽帧核对。适合给剪辑找素材（例：搜"术后包扎""机场接机"直接定位片段）。

- 源码/venv：`~/workspace/videoseek`（GitHub 6v17/VideoSeek，venv 在 `.venv/`）
- 数据目录：`~/.videoseek`（config.json、models/、data/model_assets/ Lance 索引都在这）
- 当前模型：**Chinese-CLIP ViT-B/16**（profile `chinese_clip_vit_base_patch16`，512 维，CPU 推理）
- Agent API：`http://127.0.0.1:8765/api/v1`（仅本机回环、无鉴权）
- 上游完整 API 文档：仓库 `docs/for-agents.md`（端点字段以它为准）；本文件只记本机部署的启停与坑

## 1) 启动 API 服务（搜索前必须先启）

```bash
cd ~/workspace/videoseek
setsid env TMPDIR=/home/hatch/workspace/.tmp nohup .venv/bin/python headless_server.py > /tmp/videoseek_server.log 2>&1 < /dev/null &
curl -s http://127.0.0.1:8765/api/v1/health   # 看 index_ready / model / ffmpeg
```

停服务：`pkill -f headless_server`（注意别在同一条命令里再写这个字面串，会把自己的 shell 一起杀掉；用变量拼接）。

## 2) 建库 / 同步索引（新增视频后必做，API 本身不能建索引）

```bash
cd ~/workspace/videoseek
TMPDIR=/home/hatch/workspace/.tmp .venv/bin/python headless_sync.py /path/to/视频目录 [更多目录...]
```

- 目录即一个「库」；重复跑只补新增/变化的视频。
- CPU 速度参考：2 核下短视频约 15–35 秒/条（抽帧 2fps + 编码），长视频按时长线性增长；批量入库请预留时间、让它在后台跑完再搜。
- 切换模型 profile 后必须对所有库重新同步。

## 3) 搜索（服务已启动时）

```bash
# 中文文搜
curl -s -X POST http://127.0.0.1:8765/api/v1/search \
  -H 'Content-Type: application/json; charset=utf-8' \
  -d '{"query":"术后包扎","top_k":5}'

# 图搜（query 换成本地图绝对路径 + query_type=image_path；或用 image_base64）
curl -s -X POST http://127.0.0.1:8765/api/v1/search \
  -H 'Content-Type: application/json; charset=utf-8' \
  -d '{"query":"/abs/frame.jpg","query_type":"image_path","top_k":5}'

# 批量：POST /api/v1/search/batch（queries 最多 64 条，可内嵌 export 直接导 mp4）
# 查库/视频：GET /api/v1/libraries、GET /api/v1/videos?q=关键词
# 抽帧核对：POST /api/v1/frames/extract {video_path, time_sec} → JPEG base64
# 导片段：POST /api/v1/export/clip {video_path, start_sec, end_sec, output_path}
#   encode_mode=copy 时两侧各多约 2s 边距；要精确时长用 "original"
```

命中字段：`video_path`（**必须原样使用**，禁止自己拼/猜中文文件名）、`start_sec/end_sec`、`start_timecode/end_timecode`、`score`。
路径规则、scope 用法、`text_enhance`（复合描述难命中时给文搜加 `"text_enhance": true`）、无命中时的处理顺序，全部见仓库 `docs/for-agents.md` §2–§5。

## 4) 本机部署的坑（都踩过，别重犯）

1. **`/tmp` 是 512MB tmpfs**：pip 安装和运行时解压会 `No space left`。凡跑 pip / 本工具脚本，一律带 `TMPDIR=/home/hatch/workspace/.tmp`（先 `mkdir -p`）。
2. **config 必须先升到 schema v2**：导入模型 zip 前先跑一次
   `.venv/bin/python -c "from src.storage.migration_runner import ensure_config_schema_v2_bootstrap; ensure_config_schema_v2_bootstrap()"`
   否则 `scripts/import_runtime_resources.py` 报 "requires config schema v2"（文件其实已解压、但 profile 没注册）。
3. **数据目录逻辑**：代码读 `LOCALAPPDATA` 环境变量，没有就用 `~/.videoseek`——Linux 下什么都不用设。导入脚本在 Linux 下可直接用：
   `.venv/bin/python scripts/import_runtime_resources.py /path/to/chinese-clip.zip`（不要传 ffmpeg.exe，Windows 二进制没用；系统 `/usr/bin/ffmpeg` 会被自动识别，health 里 `ffmpeg_available: true`）。
4. **大文件下载别用裸 curl 后台跑**：本机出口代理会截断长下载且并发写会损坏文件；用分块 Range + 逐块校验的方式（参考 `~/workspace/videoseek-downloads/dl.py`），下完核对字节数。模型源包在 `~/workspace/videoseek-downloads/chinese-clip.zip`（691,547,505 字节）。
5. **GUI 不用开**：`python main.py` 是 PySide6 桌面端，无头环境跑不了也不需要；索引和 API 都走上面的无头脚本。VLC 缺失只影响桌面预览，搜索/建库/导出不受影响。
6. **台词搜索（dialogue）未启用**：`dialogue_search: false`——需要先有硬字幕 OCR 索引（桌面字幕库流程），本部署没做；要用时再单独处理（rapidocr 包已随 requirements 装好）。

## 5) 验证基线（2026-10-20 实测）

- 测试库 `~/workspace/videoseek-testlib`（4 条 fb-ip 小样视频，已建库，随时可删/换）
- 文搜：「术后包扎」→ c3_postop.mp4 第 1 名（0.447）；「机场接机」→ c1_arrival.mp4 第 1 名（0.443）
- 图搜：c3_postop 第 2 秒帧 → 本体 0.979、旅程片对应段 0.881
- health：`index_ready: true`、model `chinese_clip_vit_base_patch16`、ffmpeg `/usr/bin/ffmpeg`
