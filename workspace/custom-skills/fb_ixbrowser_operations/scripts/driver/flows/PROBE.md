# FB 定位探针（v2 部署后、写正式流程前跑）

目的：用 /eval 在真实登录的 Victoria 号（profile 2）上验证 FB 各关键定位，
一次拿到真实选择器，再写猎手/私信/回评流程，不猜、不重启。

跑法（重启后）：
    python3 -c "from flows.ixb_client import IxAgent; a=IxAgent(); print(a.health())"
    再按下面逐条用 a.eval(2, "...") 验证。

## 1. 主页与登录态
- `() => ({title: document.title, url: location.href})`
- 发帖框文本（已验证可用）：找 "What's on your mind," 的元素取名字。

## 2. 猎手：目标帖的评论框
开一个目标帖链接（/goto），验证：
- 评论框是不是 contenteditable：找 `[contenteditable="true"]`，数个数、取 aria-label / placeholder。
- 点开“查看更多评论”的按钮文本（英文界面常见 "View more comments"）。
- 发评论后的确认信号：页面上出现自己刚发的评论文本。

## 3. 私信：Messenger 线程列表与发送框
开 https://www.facebook.com/messages，验证：
- 线程列表项的选择器：找带未读标记的项（aria-label 含 "unread" 或有未读圆点）。
- 打开某线程后，消息输入框的选择器（`[contenteditable="true"]` 还是 textarea，
  aria-label 常见 "Aa" 或 "Message"）。
- 发送后确认：最后一条气泡文本等于刚发的内容（发前先读最后一条，避免重复发）。

## 4. 自家帖回评：主页帖子下的评论
开主页 Dr.qh88 或个人主页帖子，验证：
- 帖子卡片的定位：按作者名/时间取。
- 某条评论的“回复”按钮文本（"Reply"）与回复框。
- 已回过的评论要能识别（自己的头像/名字已出现在回复里），避免重复回。

## 5. 发帖（先只验证读，不发）
- 发帖框点开后的结构：文本框、加图片/视频的按钮（"Photo/video"）。
- 发布按钮文本（"Post"）与发布后的确认（主页出现新帖）。

## 铁律（照搬 Victoria 运营口径）
- 私信一次只发一条，等对方回了再发下一条；首条禁索号，第 3 条给面诊钩子；
  零报价；送达必须以页面上出现我方气泡为准，不凭“已发送”感觉。
- 评论 2–4 句，带楼主原帖独有细节，结尾留跟他本人有关的问题；
  推广嫌疑者绝不回复、不 @、不接话。
- 每轮先扫本号最新帖的未回评论，再去评别人的帖。
- 429 只是瞬时限流，短暂退避后重试，不自己设限、不停查。
- 任何对外动作先在 Victoria 单号试点跑通，再往别的号铺。
