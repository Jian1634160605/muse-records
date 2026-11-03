# 源片池补给登记 — 2026-10-23

## 结果：本轮 CLI 下载 0 条（通道全线受阻，待主代理浏览器通道接手）

子代理已把所有非浏览器路线逐条实测，结论与 2026-10-21 的记录一致：**当前唯一实测可用的下载通道仍是「实时浏览器 + fastdl.app」**（2026-10-21 用该路线从 916 成功下载 5 条），该通道归主代理执行，本子代理无浏览器权限。

### 本轮实测的路线与卡点（2026-10-23 11:4x）

| 路线 | 结果 |
|---|---|
| instagram-cli 连接器 | `accounts` 返回空数组——IG 账号未连接（IG 线 10-21 弃用后已解绑），所有读命令都要求已连接账号的 `--account-id`，无法列出/读取同行帖子 |
| yt-dlp（videoseek venv）+ FB 静态代理 | 列表页走 generic 提取器不支持；单条 Reel 报错 "This content isn't available to everyone"（IG 未登录墙，与 10-21 实测一致）。注：代理有 TLS 拦截，需 `--no-check-certificate` 才能连通，但连通后仍被登录墙挡 |
| IG 官方 web_profile_info 接口 + 代理 | HTTP 429（两条 FB 出口 IP 均同）——数据中心 IP 被 Meta 限流/标记 |
| ddinstagram 镜像站 | 直连与走代理均连接失败（HTTP 000） |
| 历史已证伪路线（10-21 记录，未重复试） | SaveFrom 地域停服、Cobalt 需 JWT、fastdl/snapinsta 网页接口下线或被 Cloudflare 拦 |

### 待下载目标（交主代理用浏览器 + fastdl.app 执行）

选源优先级与数量（按任务口径）：
1. **@internationalplasticsurgery916**：最新 Reels **10–15 条**未用过的源片（恢复时间线、面诊、前后对比优先；水印在画面边缘的优先，中央大签名/横幅挡主体的跳过）
2. **@tan.iasampson / @dr.chen8801** 补专科，各 2–4 条：
   - 眼部 → Jusa 主页（Eye Rejuvenation）
   - 鼻部 → Simon 主页（Rhinoplasty）
   - 身体塑形/吸脂 → Cora 主页（Body Contouring）

红线复核：@reface_scarless、@yefacialdesign 不下载不分发；台湾人案例禁用；"不能发/不可发"标记不取；血腥手术画面慎取。

### 必须排除的已用短码（used.txt 去重后 15 条）

DR3eGMvkWDr、Dd-ytvziqla、Dd9mefvBL7N、DdYB0YnKKVe、DeCa7hWTFBX、DeOQjV0iTo1、DeQ2W0yCUAM、DeSM2jLhhw6、DeXNShQTl5T、DefE2l5hyH2、Dern1_coTCc、Det6A4nIazf、Detu-DrI-Om、DetvfGEIb11、DevV3l0oYL-

### 存放惯例（下载后沿用）

- 源片目录：`~/workspace/ig-ops/christycrawford85/src-<日期>/`（上一批为 `src-2026-10-21/`；10-21 晚间批次曾放在 `queue/2026-10-21-other/src/`）
- 新片在此文件补登记：出处账号、部位/类型、时长、适合主页；used.txt 不动，由备料任务在实际使用时登记。

## 入库结果（2026-10-23 12:49 主代理磁盘核验）

浏览器通道实际下载并已移入 `src-2026-10-23/`：**共 25 条，79MB**
- IG 侧（fastdl.app）：17 条，命名 `ig-fastdl-01..17-*.mp4`（916 为主，含 tan.iasampson 的 Dr.QinHao 标题片数条、dr.chen8801 备用片；逐条出处/部位待备料时筛片确认）
- FB 侧（getmyfb.com）：8 条，命名 `fb-getmyfb-01..08.mp4`（浏览器报告口径：鼻部 3、眼部 2、身体塑形 3，逐条待筛片核对）
- 注：浏览器报告称 26 条，磁盘实数 25 条——1 条 IG 下载未落盘，按实数 25 入账。
- 未完成：dumpor.io 被 Cloudflare 机器人验证卡住、浏览器会话中途准入失败，anonyig.com 尚未验证；后续会话恢复后可再补，眼部素材仍偏少（2 条）。
- 状态：全部待筛（部位归类、水印位置、帧质量按 video_source_screening 流程在备料时逐条过）。

- 2026-10-23 17:4x 用户品鉴样片已用 fb-getmyfb-01（眉提升+上睑+鼻修复+颏下成形术后效果，25s）剪辑成品于 showcase-2026-10-23/final.mp4，备料勿重复使用此源。注：ig-fastdl 系列（916）全带 Dr. Lanlan 中央签名水印+底部机构横幅，按 17:07 新规（无医生身份/去水印）筛片时须逐条评估，中央签名过不去的弃用。

## 筛片结论（2026-10-23 17:5x 主 agent 全量抽帧筛完 25 条）
- 916 过程型（ig-02/03/04/05/07/08 等）：全部带 Dr. Lanlan 签名+底部机构横幅，部分带"盗图者替我挡灾"防盗字。ffmpeg delogo 实测失败（拉出竖条糊痕、还会糊到人脸），此路不通；硬裁底部会切掉下巴/对比小图，构图残缺。
- ig-11、ig-16（画面干净的两条）：前后对比人物对不上（术后换了个人）——疑似假对比，触医疗造假红线，禁用。ig-10 同类问题+带签名弧。
- ig-13 中文口播科普、ig-12 提拉贴演示：类型不对，不用。fb-01 已被用户否决（单人大脸成果特写）。
- 结论：今日池内无"过程型+可干净处理"的成品候选；后续补货筛片按此标准：优先只要横幅无签名无防盗字的过程片，或公司自有素材。
