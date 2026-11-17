# 猎手台账 — Ejje（FB profile 67，品线待定）

## 2026-11-17 19:17 轮次（首轮）— 未完成：浏览器挂起

- **身份核验：通过。** open(67) 成功；facebook.com 显示名 Ejje，个人号 id 61581899105351，feed 正常加载。发帖框署名 "What's on your mind, Ejje?"。
- **通知：已读。**
  - Nayan Nayan 在本号两条 reel 下各留 1 条评论（6h 前），另有 1 个点赞：
    - reel 2057454604961825（鼻子线："A beautiful nose lies in balanced facial aesthetics…"）
    - reel 1750064819402416（面提线："耐心打磨细节，每一处都恰到好处…"）
  - 两条评论正文均为空（纯表情/贴纸类，无文字、无提问、无意向信号），无法按原话接话，未回评。非客资信号，记此备查。
  - 另有系统通知：reel 已发布 ×2、"profile is not being recommended to people under 18"（14h 前，常规提示）。
- **目标搜索：未完成。** `search/posts/?q=rhinoplasty before after` 返回 "We didn't find any results"；随后依次搜 rhinoplasty / facelift 时，/goto 在 170s 超时（curl 28，0 字节返回）。
- **故障经过（均未返回数据）：**
  - 19:2x /goto 搜索页超时 170s
  - /check(67) 超时 45s
  - /tabs(67) 超时 70s
  - /close(67) 超时 80s+（外层 100s 掐断）
  - /opened 超时 40s（此前 /health 正常返回 agent v6）
  - 结论：67 号浏览器在搜索导航时挂起，随后 agent 本身也无响应（可能被挂起的操作阻塞，或用户电脑上 5 个 profile 并发过载——同期 p1/p5/p32/p38 均打开）。**未确认 profile 67 是否已关闭，用户电脑上可能仍挂着该窗口。**
- **评论发出：0 条。** 无草稿、无 E07 打分、无发帖动作，无客资。
- **下一步：** 下轮先查 /opened 与 agent 状态；若 67 仍挂着，重启该 profile 后再跑；若 agent 持续无响应，报总管处理（勿盲重试）。

## 2026-11-17 19:47 轮次 — 未完成：与私信轮次撞号，主动停手

- **Agent 状态：** /health 正常（agent v6）；/opened 显示 10 个 profile 全开，67 号自 19:36 已开着（pid 44580，调试口 127.0.0.1:56543）。
- **回收：** check(67) 60s 超时、tabs(67) 40s 超时（浏览器无响应）；close(67) 130s 内成功返回 closed:true；重新 open(67) 成功（新调试口 127.0.0.1:42147）。
- **身份核验：通过。** facebook.com 显示 "What's on your mind, Ejje?"，个人号 id 61581899105351（与首轮一致），feed 正常加载。
- **通知：已读。** 仍是 Nayan Nayan 的 2 条 reel 评论 + 1 个点赞（7h 前），与首轮同一批，无新增；另有 reel 已发布 ×2、"profile is not being recommended to people under 18" 系统提示。两条评论正文仍为空（reel 页 innerText 仅 120 字符，无评论区文字载入），无法按原话接话，未回评。
- **撞号证据（决定停手的直接原因）：**
  - goto 搜索页 `search/posts/?q=facelift` 返回标题 "facelift - Search Results"，但随后 eval 读到当前 URL 已是 `facebook.com/messages/`（Messenger 聊天列表）。
  - tabs(67) 显示仅 1 个标签页，位于 E2EE 私信线程 `messages/e2ee/t/4660134264225266/`。
  - 重试 goto `search/posts/?q=rhinoplasty` 同样返回搜索页标题，但 5 秒后 URL 已变成另一个 E2EE 线程 `messages/e2ee/t/869501289584668/`。
  - 结论：另一进程（极可能是 fb-dm-p67 私信轮次，67 号 19:36 即已打开）正在同时操控同一浏览器，两次导航均在数秒内被拉走。继续发评论有发错上下文的风险，主动停手。**本轮未关闭 profile**——私信轮次正在使用，关掉会打断对方。
- **附带发现（仅记录，不处理）：** Messenger 列表可见 Ejje 号既有私信线程（Mohsen Aziz 3h 前发贴纸、Nayan Nayan 7h 前、Lando Fer 20h 前等），其中两条 "You:" 历史消息为 1 天前发出（内容含不当用语与一条 wa.ginhao.me 链接），属本轮之前已有的发送记录，猎手轮不介入，留待私信轮次/总管核查。
- **评论发出：0 条。** 未读到目标帖子，无草稿、无 E07 打分、无发帖动作，无客资。
- **下一步：** 猎手与私信轮次须错开时间或错开 profile 占用——同一 profile 两轮同时跑会互相抢浏览器，首轮 19:17 的挂起很可能也是同一原因。建议总管把 fb-hunt-p67 与 fb-dm-p67 的启动时间拉开，或确认 dm 轮次结束后再跑猎手轮。

## 2026-11-17 20:17 轮次 — 未完成：浏览器先挂起、恢复后又与私信轮次撞号，主动停手

- **Agent 状态：** /health 正常（agent v6）；/opened 显示 9 个 profile 全开，67 号自 20:12 已开着（pid 52088，调试口 127.0.0.1:40132）。
- **挂起回收：** tabs(67) 60s 超时、check(67) 45s 超时（0 字节返回）；close(67) 约 66s 内成功返回 closed:true；重新 open(67) 成功（新调试口 127.0.0.1:2600）。
- **身份核验：通过。** check(67) 返回 account_name 'Ejje'（name_source: composer），facebook.com 正常，个人号 id 61581899105351（与前两轮一致）。
- **通知：已读。** 无新增，仍是 Nayan Nayan 的 2 条 reel 评论 + 1 个点赞（7h 前），评论正文为空（纯表情/贴纸类），无法按原话接话，未回评；另有 reel 已发布 ×2、"profile is not being recommended to people under 18" 系统提示。
- **目标搜索：未完成。**
  - `search/posts/?q=facelift` 正常返回搜索页标题，但结果全是建筑/汽车"翻新"类无关内容（The Straits Times 邮轮中心翻新、Peugeot E-2008 facelift、Honda Freed facelift 等），无医美目标帖。
  - `search/posts/?q=deep plane facelift` goto 返回搜索页标题，但数秒后 eval 读到当前 URL 已是 `facebook.com/messages/`（Messenger 聊天列表）；tabs(67) 确认仅 1 个标签页、位于 Messenger。**与 19:47 轮次完全相同的撞号特征：另一进程（极可能是 fb-dm-p67 私信轮次，约 20:32 启动）正在同时操控同一浏览器。**
- **撞号决定：主动停手，本轮未关闭 profile**——私信轮次正在使用，关掉会打断对方。未发任何评论，无草稿、无 E07 打分，无客资。
- **附带发现（仅记录，不处理）：** Messenger 列表可见 Ejje 号既有私信线程（Mohsen Aziz 4h 前发贴纸、Nayan Nayan 8h 前、Lando Fer 21h 前等），其中 "You:" 历史消息含 1 天前发出的不当用语与一条 wa.ginhao.me 链接，属本轮之前已有的发送记录，猎手轮不介入，留待私信轮次/总管核查。
- **结构性问题（第三轮连续受阻）：** 19:17 挂起、19:47 撞号、20:17 挂起+撞号。15 分钟错峰不够：经 tunnel 的每次 agent 调用耗时 60–130 秒，一轮猎手（通知+2 次搜索+读帖）实际耗时远超 15 分钟，必然撞上下一轮私信。建议总管：① 把 fb-hunt-p67 与 fb-dm-p67 的启动间隔拉到 45 分钟以上，或 ② 猎手轮开始前先查 /opened 与 tabs，确认无其他轮次占用再动手（本轮 20:12 的 open 即为占用信号，当时误判为残留窗口），或 ③ 两轮共用同一轮次脚本串行跑。

## 2026-11-17 20:47 轮次 — 未完成：私信轮次仍在占用，主动停手（连续第 4 轮受阻）

- **Agent 状态：** 首次 /health 返回空回复（curl 52），20 秒后重试恢复正常（agent v6）；/opened 显示 8 个 profile 全开，67 号自 20:23:42 已开着（pid 36216，调试口 127.0.0.1:2600，与 20:17 轮次重开后的同一实例）。
- **身份核验：通过。** check(67) 返回 account_name 'Ejje'（name_source: composer），个人号 id 与前三轮一致（61581899105351），facebook.com 正常。
- **撞号证据（决定停手的直接原因）：** 本轮未做任何导航，仅两次 eval 读 URL：第一次 `https://www.facebook.com/`，45 秒后第二次已变成 `https://www.facebook.com/friends/requests`——浏览器在无人操作的情况下自行跳转到好友请求页，证明另一进程（极可能是 fb-dm-p67 私信轮次，正在处理好友请求）正在实时操控同一浏览器。tabs(67) 此前显示仅 1 个标签页，位于 facebook.com 首页。
- **通知/目标搜索/评论：均未做。** 撞号已确认，继续动手有发错上下文的风险，主动停手。**本轮未关闭 profile**——私信轮次正在使用，关掉会打断对方。
- **评论发出：0 条。** 无草稿、无 E07 打分、无发帖动作，无客资。
- **结构性问题（连续第 4 轮）：** 19:17 挂起、19:47 撞号、20:17 挂起+撞号、20:47 撞号。20:17 轮次建议的“先查 /opened 与 tabs 确认无占用再动手”本轮已执行并确实探到了占用，但探到占用的结果只能是停手——猎手轮在私信轮次的 30 分钟节拍里根本找不到空窗。建议总管：① 把 fb-hunt-p67 与 fb-dm-p67 的启动间隔拉到 45 分钟以上，或 ② 两轮共用同一轮次脚本串行跑（同一进程内先私信后猎手，或反之），或 ③ 暂停 fb-hunt-p67 直到节拍改好，否则每轮都是空转。
