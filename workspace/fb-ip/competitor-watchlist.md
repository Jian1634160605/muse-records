# FB 医美同行监控名单（截流用）

生成：2026-10-22。用途：猎手任务的同行监控名单扩充——盯这些账号/主页/患者群的评论区与新帖，发现海外客户问价/问预约/求推荐时按既定 SOP 触达。
本轮为**只读调研**，未发任何评论/私信/点赞。

## 核实方法与限制（如实说明）
- FB 内部数据走 facebook-cli（静态代理）：`groups search` 可用，医生自营患者群是本轮最硬的证据（群在 FB 内真实存在且有成员数）。
- CLI 对**非好友的外部主页** `profile info` / `timeline fetch` 返回 403（仅本人/好友可读），FB 网页对未登录抓取也被拒——所以外部主页的"最近一帖日期/单帖评论数"多数**无法精确取得**，表中以公开索引（官网更新时间、三方目录抓取的近期帖子时间戳、患者群规模）作活跃证据，评论量只给量级/迹象，**没有编造数字**。
- `groups posts` 仅对 Victoria 已加入的群有数据，非成员群读不到帖子明细。

## 一、新增同行（本轮新增 12 个）

| 账号名 | FB 链接/ID | 主营项目 | 目标客群地区 | 最近活跃证据 | 评论区客户提问迹象 | 优先级 |
|---|---|---|---|---|---|---|
| Dr. Amir Karam（San Diego Facial Plastics） | facebook.com/sandiegofacialplastics | 深平面拉皮（Vertical Restore）、颈部提升、鼻整形 | 美国 + 全球飞入客 | 三方索引到其 FB 在 2026-10-11、10-12 连续发患者案例帖（7 天内） | 有：案例帖面向"想做拉皮"人群，官网明示全球患者飞入咨询；FB 评论精确数未登录不可读 | 高 |
| Dr. Ben Talei（Beverly Hills Center） | facebook.com/drbentalei | AuraLyft 深平面全脸拉皮、唇提升 | 美国 + 名人/全球客 | 2026-10 其明星患者（Denise Richards）拉皮案例全网热议，社媒持续同步分发（TikTok 同案例 488 评论） | 有：案例内容自带大量"多少钱/在哪做"类围观提问（跨平台同题） | 高 |
| Dr. Fatih Cinar | 自营患者群 facebook.com/groups/1601517861115720（523 人） | 深平面拉皮、颈部提升、鼻整形 | 欧洲、中东、美国（伊斯坦布尔医旅） | FB 内自营患者群在册；Bookimed 2026 在售拉皮套餐 $5,000 起、持续收治国际患者 | 有：患者群即其术后客户社群，群内问恢复/问行程是常态 | 高 |
| Dr. Yasin Kürşad Varsak | 自营患者群「Dr Varsak - Turkey Facelifts」facebook.com/groups/237641828891613（1,000 人） | Extended 深平面拉皮、鼻整形（只做脸） | 美国、英国（伊斯坦布尔医旅） | 官网 2026-10-04 更新；RealSelf 2026-07 仍有美国患者新评价 | 有：评价与患者群高频出现"从美国/英国飞来做"、问协调/问恢复的真实客户内容 | 高 |
| Dra. Maribel Belmontes | 自营患者群 facebook.com/groups/2638294223014636（729 人） | 深平面拉皮、颈部提升（瓜达拉哈拉） | 美国跨境客 | 2026 年患者案例病毒传播（Michelle Wood）；RealSelf 2026-09 新评价；患者群在册 | 有：患者群为其客户社群，跨境患者问行程/问恢复密集 | 高 |
| THE FACELIFT SOCIETY by Dr. Espino | facebook.com/groups/1110865075451943（542 人） | 拉皮专科（医生本人运营的教育型社群） | 全球英语客群 | FB 群搜索在册，定位"国际面部年轻化社群：患者教育、手术规划与恢复" | 有：群定位即患者问答场；注：医生本人主页 handle 未核实，监控入口先用该群 | 中 |
| ID Hospital Korea | facebook.com/idhospital.eng | 眼鼻综合、面部轮廓、鼻整形 | 全球（英语专线，东南亚/中东/欧美） | 官网 2026 持续更新在线咨询答复；FB 为其官网明示的官方页 | 有：官网咨询区大量问价/问恢复期，FB 页承接同一批国际咨询客 | 中 |
| Kamol Cosmetic Hospital | FB 主页（官网有链接，handle 待 FB 内搜索确认） | 面部整形、拉皮、面部女性化（曼谷） | 全球（欧美澳为主） | 2026-10 三方报道仍引用其 FB 主页图；JCI 认证、国际患者多语种接待 | 有：国际患者评论体量大（Google 侧 599 条），FB 为其主阵地之一 | 中 |
| PlacidWay | FB 企业主页 + 自营支持群 facebook.com/groups/1214570405856612（469 人） | 医美旅游平台（整形为其核心品类之一） | 全球 | 2026 持续发布行业内容/播客，官网明示 FB 企业页在运营 | 有：自营支持群即患者问答场，平台帖下问诊所/问价格为常态 | 中 |
| Bookimed | FB 主页（其官网标注 FB 评分 4.8/5） | 医美旅游平台（全球第一梯队） | 美国、英国、西欧为主 | 官网内容 2026-10-21 仍在更新，平台月访约 17 万 | 有：平台型账号，帖下问价/问诊所是其日常评论构成；FB 精确评论量未取得 | 中 |
| Dr. Ashkan Ghavami | FB 主页（Feedspot 索引 FB 约 10.2K 粉） | 鼻整形、修复鼻（Beverly Hills） | 美国 + 国际 | IG 侧约 57 万粉持续活跃，FB 同步运营（目录数据近期抓取） | 未取得 FB 评论样本，仅确认主页体量 | 中 |
| Dr. Huseyin Balikci | 自营患者群「Huseyin Balikci Rhino」facebook.com/groups/260043095451900（931 人） | 鼻整形（伊斯坦布尔） | 全球（欧美医旅客） | FB 内患者群在册 | 有：患者群为术后客户交流场 | 中 |

## 二、附带猎场（不是账号，是客户密集的群，顺手盯）
- Facelift & Necklift Turkey（facebook.com/groups/1146474503904898，约 1.1 万人）、Facelift / Eye Lift Turkey（1013711189799224，约 9,000 人）——土耳其拉皮求推荐帖密集。
- deep plane facelift and neck lift and rhinoplasty support group（1052731386791309，约 3.4 万人）、Deep Plane Facelift and Neck Lift Global Support Group（1854363335255993，约 2,000 人）。
- The Plastic Surgery Support Group（350903875578893，约 11.5 万人）、305 Plastic Surgery Dolls（389270235338338，约 3.8 万人，迈阿密诊所客户群）。
- Korea Plastic Surgery & Cosmetic Procedures（1418461198411390）、Facelift in Korea: clinics+price+surgeons（766187188947209）——韩国线求价帖。
（注：非成员群 CLI 读不到帖子明细，需 Victoria 加入后才能巡查帖子内容；加群动作不在本轮只读范围内。）

## 三、已在监控（原名单，本轮复核附注）
| 账号 | 附注 |
|---|---|
| doctor.truesdale | 原名单；本轮因 CLI 对外部主页 403，未能复核最近发帖 |
| nayakplasticsurgery | 原名单（Dr. Mike Nayak，深平面拉皮）；同上，未能复核 |
| reface_scarless | 原名单；**注意：非公司号，只学内容结构，绝不分发其素材**（既定红线） |
| drkassir | 原名单；侧面数据更新：Feedspot 索引其 FB 约 59.8K 粉、IG 约 110 万 |
| dra.camimartinez | 原名单；同上，未能复核 |
| toropclinic | 原名单；同上，未能复核 |
| dr.zhang.3u | 原名单；同上，未能复核 |
| @internationalplasticsurgery916（Dr. Lanlan） | 内容选源在用（非截流监控对象） |
| @tan.iasampson | 内容选源在用 |
| @dr.chen8801 | 内容选源备用 |

## 四、Instagram 同行参考名单（只做内容结构学习与备用，不触达、不登录互动）
| 账号 | 粉丝量级 | 备注 |
|---|---|---|
| @dr.lifeng | 约 30.3 万 | 公司李峰号，内容基线（医生出镜+大字英文标题+案例故事） |
| @drkassir | 约 110 万 | Feedspot 索引；鼻整形，与 FB 已监控为同一人，IG 体量更大 |
| @drsamrizk | 约 86.6 万 | Feedspot 2026 索引；纽约深平面拉皮+鼻整形 |
| Dr. Ashkan Ghavami | 约 57.2 万 | Feedspot 索引；Beverly Hills 鼻整形 |
| @internationalplasticsurgery916（Dr. Lanlan） | 蓝V，量级未核实 | 现行内容选源 #1 |
| @drbentalei | 量级未核实 | 2026-10 明星拉皮案例热度高，深平面 AuraLyft 结构可学 |
