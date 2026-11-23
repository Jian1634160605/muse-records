# Muse 电脑操控方案 — deck plan
约束：用户原话「详细说一下这套方案怎么实现的，每个节点在这里面起到了什么作用」；中文。本次为纠错重做：上一版误按抖音 @AI_Panda 视频的四端互联方案（Tailscale+Syncthing+远程桌面）成稿，用户指出要的是昨天文档汇报的那套 — 即 Muse 实际操控用户电脑的方案。内容全部改以已落地的真实文档为准：fb_ixbrowser_operations 完整手册、headless-resume-deployment 部署口径、本机 agent README（D:\ixbrowser-agent、8765、Local API 53200）、素材库经本机中转、CLI 后台发布与核验。Syncthing 按用户 2026-11-20 定：先不装、只备记，PPT 中仅一句带过、不作主线节点。主题、版式、10 页结构与既有风格保持不变，仅换内容。
幻灯片（10）：
1 cover — 标题
2 overview steps — 解决什么问题：云端够不着本机、多账号后台批量、并发与误判
3 architecture two-column — 三层架构（决策/通道/执行）+ 一条指令完整链路（配图沿用）
4 node-muse hero-stats — 节点一 Muse 云端大脑：决策、调度、核验
5 node-tailscale hero-stats — 节点二 Tailscale 只管送达：连通、寻址、安全（含 Syncthing 备记一句）
6 node-syncthing gallery — 节点三 本机 agent 8765：贴着浏览器跑的执行员（新配图）
7 node-control bento — 节点四 ixBrowser 工位：身份隔离、Local API、调试驱动、并发锁
8 node-devices headline-bullets — 三条支线：Concat 桥 8766、CLI 发布、素材库中转、员工受限版
9 workflows headline-bullets — 三件日常工作的完整闭环：猎手、发布、私信
10 landing closing — 现状与边界：主链跑通、无窗口未完全解决、Syncthing 先不装
图片：cover hero 沿用、四端示意沿用（architecture）、本机 agent 新生成图（node-syncthing）

视觉打磨（2026-11-20 按 Impeccable 标准，Persuade 型）：设计观点是「一条指挥链」— 每页底部有五站链路定位条（用户→Muse→Tailscale→本机 agent→ixBrowser），当前节点铜色点亮；标题关键词铜色强调；节点页带大号序号水印 01/02；架构页为五站链路图、Tailscale 页为隧道图、ixBrowser 页为 9 号矩阵（FB 钢蓝左边框、IG 铜色左边框）、工作流页为编号步骤条、结尾为双栏状态看板。文字已压到每卡一至两行。
注：Impeccable 的 context 启动器与 reference 文件未随 skill 落地（目录只有 SKILL.md），本次直接按 SKILL.md 核心原则执行。
