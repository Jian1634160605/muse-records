# 今晚 22:00 发布轮次运行记录（2026-11-20）

## 发前核验（22:0x）
- ixBrowser agent v10 健康，opened=[]。
- 9 条视频 ffprobe 全过：1 视频轨 + 1 音频轨；时长：01a 15.00s、01b 10.77s、02a 15.00s、03a 15.00s、03b 10.33s、04 15.00s、05 18.00s、06 12.80s、N1 v4 17.00s。
- 文案齐全：fb01/fb02/fb03/fb04/fb05/fb06/mv-03-hook/n1-recovery（fb04.txt 实际存在）。

## 结果
- [x] Victoria p2 — 01a + fb01 — ✅ 已发 https://www.facebook.com/reel/1459919795515983/ （post 122155121841352570；通知 "Your reel is published" 1m 前；文案直进核验 found=True；自评可见 True）
- [ ] Jusa p5 — 03a + fb03 — ❌ 上传 180 秒超时未完成（14:09:25 挂视频 → 14:12:32 超时，脚本 rc=1）；通知页查无新 "Your reel is published"（0 条），确认未发出。留 02:00 备用档补发，本轮不重试。
- [ ] Lark p32 — 05 + fb05 — ❌ 没走到文案页（上传完成 14:15:01，版权检查后 hasCap/hasNext 皆无，脚本 rc=1）；通知页 0 条，确认未发出。留 02:00 备用档补发，本轮不重试。
- [x] Oe p38 — 02a + fb02 — ✅ 已发 https://www.facebook.com/reel/1121778250481002/ （直进 Reel 页文案核验 found=True，Nov 20；通知页暂未刷出 "Your reel is published"，时间线只渲染 1 条链接——均系渲染延迟，文案页为准）
  - 自评引流评论 ✅ 已补（JS 路线：Playwright 点击框 15 秒超时两次，改 execCommand 填字 + 派发 Enter，核验可见 True）
  - 页头曾出现 "We removed your comment | We don't allow people to take actions at high volume…" 提示，需留意。
- [ ] Bertie p35 — 04 + fb04 — ❌ 上传 180 秒超时未完成（14:26:56 挂视频 → 14:30:02 超时，脚本 rc=1）；通知页 0 条，确认未发出。留 02:00 备用档补发，本轮不重试。
- [x] Ejje p67 — 06 + fb06 — ✅ 已发 https://www.facebook.com/reel/1131600799617292/ （通知 "Your reel is published" 1m 前；文案直进核验 found=True）
  - 自评引流评论 ✅ 已补（JS 路线，核验可见 True）
- [x] sarah p44 — 01b + fb01 — ✅ 已发 https://www.instagram.com/sarahcook6809/reel/Df95QHiNj48/ （脚本核验 Reels 标签首条；自评可见 True）
- [x] elaina p63 — 03b + mv-03-hook — ✅ 已发 https://www.instagram.com/elainaklocko_lily.02176/reel/Df95uIfhUTF/ （脚本核验 Reels 标签首条；自评可见 True）
- [x] gaga p65 — N1 v4 + n1-recovery — ✅ 已发 https://www.instagram.com/gaga5456/reel/Df96NLVMX8g/ （gaga 专用版脚本；自评可见 True）

## 小结
- 已发 6/9：FB 3 条（Victoria 01a、Oe 02a、Ejje 06），IG 3 条（sarah 01b、elaina 03b、gaga N1 v4）。
- 失败 3/9：Jusa 03a（上传超时）、Lark 05（没走到文案页）、Bertie 04（上传超时）——均通知页确认未发出，留 02:00 备用档补发。
- 自评：6 条已发全部完成（Victoria ✅；Oe ✅ JS 路线；Ejje ✅ JS 路线；sarah ✅；elaina ✅；gaga ✅）。
- 备注：本轮多次遇到其他定时轮次占用 profile（p65、p32、p38、p63），发前均复查 opened、等空闲再动手，未撞车。
