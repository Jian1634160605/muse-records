# HyperFrames：写网页，出视频

> 来源：HeyGen 开源项目 heygen-com/hyperframes（Apache 2.0，视频里十大项目之一）。原文是给 Claude Code 等 agent 的 skill，这里按 Muse 的用法改写。核心理念：**写 HTML，渲染成 MP4**。

## 这是什么

HyperFrames 把 HTML、CSS、媒体和可定位动画渲染成确定性的 MP4 视频：逐帧定位暂停的时间线，所以每次渲染结果完全一致。适合做标题卡、字幕、图表、产品介绍、竖屏短视频、片头片尾这类文字/动画型内容。

**注意**：它是 HTML 转视频，不是真人实拍。咱们的患者实拍素材线（ffmpeg/Concat 剪辑）不动，HyperFrames 是另一条生产线，补标题卡、钩子文字动画、产品介绍这类内容。

## 安装（已装好）

- CLI 已装在本机（Node v24，满足 >= 22 要求），命令是 `npx hyperframes <command>`。
- 新项目：`npx hyperframes init <dir> --skip-skills --skill=hyperframes`。
- 渲染前检查：`npx hyperframes check --json`，会报违规并给 `Fix:` 建议。

## 关键约定

- `index.html` 是根合成：声明视频变量，每个场景挂一个子合成（`compositions/` 目录）。媒体和字体放 `assets/`。
- 默认新视频 1920×1080、30fps。**咱们的 FB/IG Reel 要竖屏 1080×1920**，建项目时必须按竖屏尺寸改，不要用默认横屏。
- 每个定时元素要有 `class="clip"`、`data-start`、`data-duration`（秒），显示区间是 `[start, start + duration)`。
- 视频总长 = 根的 `data-duration`；超长会被切掉，提前结束会定格在最后一帧。
- 禁止 `Date.now()`、无种子的 `Math.random()`、网络请求、定时器、`repeat: -1`。所有可见内容必须是时间线的函数。
- 不要在 `.clip` 上 tween `display`、`visibility`、`autoAlpha`，改动画子元素。
- `<video>` 有声音要加 `data-has-audio="true"`，否则静音；音乐、旁白、替换音是单独的 `<audio>`。
- 每个 `<audio>` 要有 `id`，否则不进混音。
- 资源路径用 `assets/...`（不要前导 `/`）。
- 15 秒以上、讲事情的片子要配音乐和动作音效，除非用户要求静音。

## 工作流程

1. 先定视频类型和时长，写 HTML（根 + 场景）。
2. `npx hyperframes check --json` 检查，修掉所有 error，权衡 warning。
3. 小改动先快照预览（`--at`、`--range`、`--composition`），看过再继续。
4. 用户确认预览、或要求直接出片、或要求无停顿时，才渲染。
5. 渲染完按咱们的铁规验：ffprobe 核验 1 视频轨 + 1 音频轨，0 音轨不发；竖屏 1080×1920；带文案。

## 桌面 App

HyperFrames 还有个免费桌面 App（Mac/Windows/Linux），叫“HyperFrames 桌面 App”，不要叫它 Studio。用户想自己接着改的时候推荐用它。
