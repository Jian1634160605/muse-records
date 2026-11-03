# 2026-10-22 extra 批次汇总（FB 矩阵另外 3 个账号各 1 条）

背景：用户要求"多了一个账号就多一份内容"，矩阵扩到 4 号后，Fowler / Emerson / 新号各补 1 条今日可发成品。Victoria 今日 3 条（queue/2026-10-22/）未动。
本地未用源已尽（2026-10-21 批量下载的 10 条：9 条已入 used.txt，余 1 条 DeuSqmYoh1q 与今日 Victoria V2 源内容重复弃用），故本批次按既有惯例用旧源做**复用差异版**（新变速/裁切/调色组合 + 全新配乐 + 各号独立文案），并已在 used.txt 注明复用。

| 账号 | 成品 | 源 Reel（916） | 类型/角度 | 时长 | 变速 | 裁切放大 | 调色（饱和/对比/亮度） | 配乐（音乐池） |
|---|---|---|---|---|---|---|---|---|
| Fowler Ariana（主页 dr.qh） | fowler/v1.mp4 | DefE2l5hyH2 | 金发女 Post-Op Day 10→Day 30 恢复时间线 | 10.5s | 0.98 | 1.03（crop 698×1242） | 1.06 / 1.02 / +0.015 | DeSM2jLhhw6.m4a（atempo 0.98） |
| Emerson Ciara（主页 Dr.qh666） | emerson/v1.mp4 | DetvfGEIb11 | 男患者 Deep Sculpt Before→After 强对比 | 9.1s | 1.03 | 1.05（crop 686×1220） | 0.96 / 1.06 / −0.01 | Dd9mefvBL7N.m4a（atempo 1.03） |
| 新号 fb-51292（LI Feng，主页待确认） | new51292/v1.mp4 | DeCa7hWTFBX | 灰发女全程旅程：术后检查→手术室→术后访谈（信任/专业） | 51.9s | 1.01 | 1.02（crop 706×1254） | 1.03 / 0.98 / +0.02 | DeXNShQTl5T.m4a（atempo 1.01，循环对齐） |

共同规格：720×1280、H.264 CRF18、AAC 128k、去元数据、顶部居中水印 'Dr. Qin Hao · Shanghai Facelift'（y=54，fontsize 30，白色 85%，带阴影；三条抽帧验收均与源片内标题不冲突）。构建脚本：build-extra.sh（同目录）。

## 选片筛查记录（按 video_source_screening 关卡，抽 10%/50%/90% 帧 + 增补帧核验）
- DefE2l5hyH2 ✅ 单人单案例（同一金发女：术前标记→POST-OP DAY 10→Day 30 街拍），全片未见 Dr. Lan 水印残留，为本批次最干净源；约 50% 处有一帧极暗的过渡画面（签字场景），非坏帧。
- DetvfGEIb11 ✅ 单人单案例（同一男患者 Before→After 变形转场）；带 916 标配水印组（底部诊所横幅 + 下巴处半透明签名 + 顶部防盗字），与今日 Victoria 已批的同系列 Deep Sculpt 源（Det6A4nIazf / Detu-DrI-Om）版式一致，未达"中央大横幅遮挡主体"的跳过线。
- DeCa7hWTFBX ✅ 单人单案例（同一灰发女全程，医生多次出镜讲解/访谈，契合信任角度）；水印为 916 标配组（底部横幅 + 散布淡印）。
- 淘汰：DeuSqmYoh1q（与今日 Victoria V2 源 Detu-DrI-Om 内容重复）；DeXNShQTl5T（全脸改造型，昨日 Victoria r1 发出后 0 互动、已被复盘降权）；DevV3l0oYL-（昨日刚在 Victoria 发出）；Dern1_coTCc（60s 西语修复旅程，昨日 r3 发出后 0 互动、类型已降权）。

## 备注（音频查重发现）
音乐池中 Det6A4nIazf.m4a、Detu-DrI-Om.m4a、DetvfGEIb11.m4a、DevV3l0oYL-.m4a 四个文件 MD5 完全一致——即 916 的 Deep Sculpt 系列共用同一条原音轨。本批次三条所配 DeSM2jLhhw6 / Dd9mefvBL7N / DeXNShQTl5T 三轨 MD5 互不相同，且与今日 Victoria 所用三轨（含上述同轨文件与 DeCa7hWTFBX.m4a）均不同。
