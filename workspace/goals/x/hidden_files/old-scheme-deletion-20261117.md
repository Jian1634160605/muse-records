# 旧方案删除记录（2026-11-17 13:30，用户当面下令）

用户原话要点：Emerson 这个号好像没有了，不要再用之前那套方案；改用指纹浏览器（ixBrowser，用户电脑）这套；默认分组所有账号都可用；如 ixBrowser 账号与我电脑上之前的不一样，按现在 ixBrowser 的逻辑来；删除我电脑上的静态 IP、指纹浏览器、以及登录在我电脑指纹浏览器上的账号。

## 删除执行（移到回收站，30 天内可恢复，过期 2026-12-17）

### 静态 IP 文件（~/.agent-reach/，共 9 个，只记文件名，不记凭据值）
- proxy-fb.txt — trash_id 20261117-053433-f4083ad88cc54876b13a0cad32b0ecdc
- proxy-fb-20010.txt — trash_id 20261117-053433-31a79cfa82514ef4ac23e5f1aa6d6a01
- proxy-fb-20011.txt — trash_id 20261117-053433-71fdb8951c8a425dbd6e3f6d217b72b6
- proxy-fb-20012.txt — trash_id 20261117-053433-4b12f81af6e04fcba9a517f28f156ab9
- proxy-fb-20013.txt — trash_id 20261117-053433-cb31b60ea4a8475995ba962b5c786973
- proxy-fb-emerson.txt — trash_id 20261117-053433-76dbcb5991824265bcd11ec793efb819
- proxy-fb-fowler.txt — trash_id 20261117-053433-2afff3b1b9384c518380b849f23d46d7
- proxy-fb-sg.txt — trash_id 20261117-053433-338e8cc3d3d94e61bda2dcd002ab6b30
- proxy-fb-victoria-before-restore.txt — trash_id 20261117-053433-b36ad88d53d844ac8fe5817a3eb1f120

### 指纹浏览器（我 VM 上的 FoxProfile，整目录）
- ~/workspace/foxprofile/ — trash_id 20261117-053433-ed2e77a7ebd240c48eccefa62e4fc781
- 含 camoufox_data/（约 7.2G，12 个环境目录：fb-victoria、fb-3651、fb-6399、fb-73057、x-theeasysale1、ig-01、ig-02、ig-03、fb-1030 及 3 个 20261029 备份目录）与 profiles.json（环境注册表）
- 注：FoxProfile 环境里没有 Emerson（profiles.json 共 9 个环境，无 Emerson）；Emerson 在 ixBrowser 41 个 profile 里也没有，确认已无此号。

## 保留未删（不在本次删除范围内）
- ~/.agent-reach/proxy-acct2.txt、config.yaml、config-acct2.yaml、tools/（X 业务 acct2 相关，不属于 FB 旧方案）
- facebook-cli / hatch_messenger_cli 后台连接器线路未动（直连调用，不走代理）
- ixBrowser 用户电脑侧全部未动

## 定时任务正文同步改动（删代理指令，防下轮读到已删文件）
- fb-lead-scan（每小时，启用中）：网络出口段改为“旧静态 IP 方案已删，命令行工具直接调用，不做代理导出”。
- fb-competitor-watch（每 10 分钟，启用中）：通道与网络出口段同上改法；浏览器模式段尾改为“不再等新线、不再切回 CLI 主路线；猎手主路线就是浏览器”。
- fb-foxprofile-warm-daily 已是停用状态，未动；6 个 IG 旧任务（gaga/sarah/haze）已是停用状态，未动正文（待按 ixBrowser 方案重写）。
- fb-dm-thread-watch、fb-warm-am/noon/pm、fb-engage-daily 本来就不引用代理与 FoxProfile，未动。

## ixBrowser 核验（同日并行）
- 默认分组现为 11 个号（FB 7：1、2、5、32、38、67、80；IG 4：43、44、63、65），2026-11-16 是 9 个，新增入组 1、67；全量 41 个 profile（新增 84、85，在少婷组）。
- Emerson 在 ixBrowser 全量里不存在。
- 登录态核验脚本 ~/workspace/ixbrowser-driver/flows/check_default11.py，结果见 check-default11-20261117.json。
