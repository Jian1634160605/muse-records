# E07 审核报告 — 明星脸 2 条（2026-11-23）

审核员：E07。审核方法：每条抽 6 帧实看（0.5 / 3 / 7.5 / 9.5 / 12 / 14.5 秒，共 12 帧）+ ffprobe + volumedetect + 文案核对。抽帧底本：`~/workspace/fb-ip/e07-sf-frames/`。

## 结论：2 条全部通过

| 视频 | 总分 | 结论 |
|---|---|---|
| starface-01-20261123（明星脸的共同点） | 92 | ✅ 通过 |
| starface-02-20261123（明星同款鼻型） | 92 | ✅ 通过 |

无红线一票否决。两条均为第 1 轮。

## starface-01 — 92 分 ✅ 通过

真实度 18 / 钩子 19 / 结构节奏 14 / 准确合规 15 / 技术质量 9 / 信任感 9 / 转化力 8

- **AI 角标**：左上角“AI 示意 · AI-generated”6 帧全程显示，中文渲染正常（非方框）、清晰可读。
- **人脸**：AI 生成的虚构面孔（2 张不同面孔分段使用），非任何真实明星，无可识别的名人特征。
- **钩子**：0.5 秒“WHY DO SOME FACES JUST LOOK FAMOUS?”完整居中、无裁剪，强好奇钩子。
- **结构**：钩子 → 3 个特征（1·SMOOTH JAWLINE / 2·FULL CHEEKS / 3·STRAIGHT NOSE BRIDGE）→ 结尾问“WHICH ONE DO YOU HAVE?”。3 张特征卡全部完整可读、无裁剪、无重叠。
- **红线**：无变身/前后对比叙事，无患者案例，无承诺效果，无报价。文案明确写“Aesthetic analysis is about direction, not about becoming someone else”，并注明“Faces shown are AI-generated illustrations, not real people”。
- **文案**：钩子 + 3 个设计点 + 互动问题 + AI 声明 + 音乐 credit（relaxation-05-lily-j，Mixkit），齐全。
- **技术**：ffprobe 1080×1920、30fps、1 视频轨 + 1 音频轨、15.00 秒；volumedetect mean -17.2 dB（真实音乐，非静音）。
- 扣分：AI 人脸偏理想化（属格式固有，已标注）；全片为静帧缓推、无动态实拍；转化偏间接（属顶部漏斗科普定位）。

## starface-02 — 92 分 ✅ 通过

真实度 18 / 钩子 19 / 结构节奏 14 / 准确合规 15 / 技术质量 9 / 信任感 9 / 转化力 8

- **AI 角标**：左上角“AI 示意 · AI-generated”6 帧全程显示，中文渲染正常、清晰可读。
- **人脸**：AI 生成的虚构面孔（侧面 + 3/4 面），非任何真实明星。
- **钩子**：0.5 秒“WHY DO CELEBRITY NOSES LOOK SO GOOD?”完整居中、无裁剪，针对鼻子意向人群的强钩子。
- **结构**：钩子 → 3 个要点（STRAIGHT BRIDGE · NO BUMP / REFINED TIP / BALANCED WITH THE FACE）→ 结尾问“WHICH NOSE SHAPE DO YOU WANT?”。3 张要点卡全部完整可读、无裁剪。
- **红线**：无变身/前后对比叙事，无患者案例，无承诺效果，无报价。文案明确写“not a copy of someone else's nose”，直接排除了“变成明星”式承诺。
- **文案**：钩子 + 3 个要点 + 互动问题 + AI 声明 + 音乐 credit（driving-ambition，Mixkit），齐全。
- **技术**：ffprobe 1080×1920、30fps、1 视频轨 + 1 音频轨、15.00 秒；volumedetect mean -16.3 dB（真实音乐，非静音）。
- 扣分：同 sf01（AI 人脸理想化、静帧为主、转化偏间接）。

## 技术核验汇总

| 视频 | 分辨率 | 帧率 | 视频轨 | 音频轨 | 时长 | 音频均值 |
|---|---|---|---|---|---|---|
| starface-01 | 1080×1920 | 30fps | 1 | 1 | 15.00s | -17.2 dB |
| starface-02 | 1080×1920 | 30fps | 1 | 1 | 15.00s | -16.3 dB |

两条均无静音片、无黑帧尾部、无文字裁剪、无水印。
