# E03 交活单：任务卡44 试做成片（2026-08-20 104331）

- 任务：任务卡 51 / 派单 85；任务卡 44；老板 5 点定稿试做成片
- 状态：**成片已做好，只做片送审，未发布**。待 E07 打分（90 分门）→ 总管确认 → 老板点头后才由 E04 发。
- 成片：`~/workspace/fb-ip/cuts/task44-104331/104331-trial-cut.mp4`
- MD5：`1555dc789c4be5304bc7ac8dfcf2aea6`
- 规格：1080×1920 竖屏，44.0 秒，h264 + AAC，30fps，19.3 MB
- 目标去向（本次只做片，不发）：Victoria 个人号 + Dr.qh88 公共主页
- 构建脚本与字幕源：同目录 `build_cut.py`、`104331-trial-cut.ass`；原片转录 wav 与质检帧同目录。

## 老板 5 点逐项对账

1. 原片：`your_files/秦浩口播-确认5条-20261027/2026-08-20 104331.mp4`（2160×3840 HEVC，48.44 秒）。台词逐字转录：faster-whisper base + small 各跑全片 1 次，另对争议片段 greedy/beam5 各跑 1 次，共 5 次解码交叉核对；语言检测中文（prob 0.997–1.0）。数字逐字对：**3到5厘米、7天、10到14天**，5 次解码一致；金句「小切口不等于小事情」5 次解码一致。
2. Logo 原文件缺失：本次用文字字标「Dr. Qin Hao」+ 通用金 #C9A227 占位，全片左上常驻。**此为替代，待 Logo 原文件到后再换。**
3. 姓名条（0–5 秒，下三分之一底框）：秦浩医生 · 面部抗衰整形外科医生 · 上海 / Dr. Qin Hao · Facial Anti-Aging Plastic Surgeon · Shanghai，中英双语。
4. 字体（替代注明）：中英字幕用系统 Noto Sans；**系统 Noto Sans 本身无中文字形，中文实际用同系列 Noto Sans CJK SC**；英文数字用 DejaVu Sans（3 处数字词组已单独套用）。
5. 目标双号 Victoria 个人号 + Dr.qh88；本次只做片送审，不发布。

## 剪辑口径

- 只留医生讲话主体：语音 1.10–44.68 秒；成片取原片 1.0–45.0 秒（44.0 秒），裁掉片头 1.0 秒无讲话段与片尾 3.4 秒无讲话段；片尾 46.00–47.16 秒为画外人声（46.5 秒帧确认医生未张口，属摄影师方向），按口播口径当废片裁掉。
- 音频：原声单轨直出，ffprobe 核验音轨数 = 1（AAC 单声道，mean -34.9 dB，max -13.7 dB）；**未加音乐**：本片为口播讲解片，语音即内容，5 点未要求配乐，加音乐会压语音。
- 画面未做镜像/翻转（原片白大褂刺绣字样本身呈镜像，属源片特征，未动）。

## 逐字转录（成片字幕对照）

| 成片时间 | 中文（烧录） | 英文（烧录，2026-10-31 批次人工校对版翻译） |
|---|---|---|
| 0.10–3.54 | 如果你正在考虑小拉皮，先记住三个数字 | If you're considering a mini lift, here are three numbers to know. |
| 3.54–8.26 | 第一个就是3到5厘米左右，小拉皮的切口相对比较短 | First: around 3 to 5 centimeters, the incision for a mini lift is relatively short, |
| 8.26–14.26 | 通常会设计在我们的发际线或者耳周，尽量让恢复后的痕迹更隐蔽 | usually placed at the hairline or around the ear, so the scar stays as hidden as possible after healing. |
| 14.26–21.50 | 第二个是7天左右，很多情况下一周左右进入拆线和明显的消肿阶段 | Second: around 7 days, in many cases, about a week in, you reach stitch removal and visible de-swelling. |
| 21.50–23.60 | 但每个人的恢复速度都不一样 | But everyone heals at a different pace. |
| 23.60–30.14 | 第三个，10到14天左右，不少患者会在这个阶段恢复正常的社交 | Third: around 10 to 14 days, many patients by this stage are back to normal social life. |
| 30.14–34.72 | 但我要提醒你，小切口不等于小事情 | But one reminder: a small incision doesn't mean a small procedure. |
| 34.72–40.32 | 它依然是一项外科手术，真正决定恢复速度的是你的组织条件、手术范围以及医生的操作方式 | It's still surgery. What really decides how fast you recover is your tissue condition, the surgical area, and the surgeon's technique. |
| 40.32–43.68 | 想知道你大概需要多久恢复，可以留言问我 | Want to know roughly how long your recovery would take? Leave a comment and ask me. |

## 需 E07 / 总管复核的两处（未悄悄定稿，已标注）

1. 3.10–4.54 秒动词：ASR 五次解码均为「先去做三个说字/锁子/梭子」，不成词；结合英文翻译 “here are three numbers to know” 与上下文，字幕取「先记住三个数字」。若老板/总管听出是别的词，按原词改。
2. 29.52–31.14 秒：「不少患者会在这个阶段足够恢复正常的社交」中「足够」为 ASR 谐音残留，字幕略去该词，取「不少患者会在这个阶段恢复正常的社交」，与英文对齐。

## E07 自查项（按 REVIEW-RUBRIC）

- 水印：画面无他人水印/签名/中央大水印；白大褂刺绣为秦浩本人姓名（源片自带，镜像方向未动）；字标为文字占位（替代，已注明）。
- 他医冒充：无。画面与声音均为秦浩本人（2026-10-27 确认 5 条秦浩口播之一）。
- 假对比/伪造疗效/修患者影像/虚构服务点：无。本片无患者画面、无前后对比、无地址宣称。
- 过程与结构（请 E07 如实打分）：**本片为单场景口播讲解片，无划线/手术/恢复多阶段画面、无患者记忆点与患者原话主题句**——按老板任务卡 44 的 5 点原片直做，未编造过程段落；若按过程型 25 分项扣分，属片子本身形态所限，不是我方漏剪。
- 技术：1080×1920、44.0 秒、单音轨已核验；抽帧 7 处（0.5/3.0/6.0/17.0/26.0/33.0/42.0 秒）全部验看：字标、姓名条、双语字幕均正常，无烧录残留代码。
- 转化收口：片尾 CTA 为「留言问我」（原片原话）；发布文案草稿（英文，待审）见下。

## 发布文案草稿（英文，待 E07 打分、老板点头后才用）

Considering a mini lift? Here are 3 numbers to know: a 3–5 cm incision, about 7 days to stitch removal, and 10–14 days back to social life. A small incision doesn't mean a small procedure — it's still surgery. Want to know roughly how long your recovery would take? Leave a comment and ask me.

## 未做的事

- 未发布（两道门均未过：E07 未打分、老板未点头）。
- 未改老板 5 点；未擅自找素材（原片老板指定）；未进发布队列。
