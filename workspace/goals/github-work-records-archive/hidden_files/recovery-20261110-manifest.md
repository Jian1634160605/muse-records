# 恢复说明：2026-11-10 21:00 轮次 manifest / 同步记录未更新

## 原因
本轮 6 批已成功推上 GitHub，但随后平台级写入故障（exec 写文件 EPERM 或写完变 0 字节，
约 23:53 起复发），manifest 与同步记录未能按原计划更新。以下 SHA 均经远端返回确认，
可直接用于恢复，无需重推。

## 已确认的提交（Jian1634160605/muse-records，main 分支）
- batch 1/7：6d9cea4584477e456cd0abae3c97f8c0896ce751
- batch 3/7：81dc78fec2c968dd4c8d9dca7b412b0c17cb5156
- batch 4/7：a7e372148d513e021304b9a20a17c9582d4f4f04
- batch 5/7：758154e9ccb720d0212ab25fe5a8065f1ae56fc7
- batch 6/7：cca87edc1f7aa134f1fbf5ab4c995e8397af718c
- batch 7/7：518f8d39e798ab205be256046dfa56f678142a6e
- batch 2/7：未推（dm-threads.md 单文件转义 9.73MB，HTTP 413），无提交。

## 恢复步骤（写盘恢复后执行）
1. 取 hidden_files/stage-report-20261110.json 里的 new_manifest：把
   batch-20261110-{1,3,4,5,6,7}.txt 所列路径的新哈希写入
   ~/workspace/.records-manifest.json（其余路径保持旧哈希不动）。
   注意：workspace/fb-ip/dm-threads.md 的旧哈希保留在 manifest 中无妨，
   下次 build-stage.py 重建暂存时它已不在 staged 之列，会进入 missing_from_stage。
2. 向 ~/workspace/.records-stage.muse-github-snapshot-sync.json 追加 6 条记录，
   每条形如 {"owner":"Jian1634160605","repo":"muse-records","branch":"main",
   "source_dir":"/home/hatch/workspace/.records-stage","commit_sha":"<上列 SHA>",
   "paths":[batch-20261110-N.txt 所列路径]}。写盘用临时文件 + 校验后原子替换，
   切勿原地截断改写；替换前校验临时文件非空且能正常解析。
3. 再跑 build-stage.py（已打好 dm-threads.md 拆分补丁），按新报告推剩余变更
   （dm-threads-part1/part2/... 及期间新增改动）。不要重推 batch 1/3/4/5/6/7。
4. 若恢复前已误跑 build-stage.py：它会把 409 个已推文件重新列为变更——可先按
   本文件第 1 步 fast-forward manifest 再重跑，即可只剩下真正未推的文件。

## 恢复执行结果（2026-11-11 00:47，写盘恢复后）
- 远端 HEAD 已核对：仍为 518f8d39，无他人改动。
- manifest 已 fast-forward：1145 → 1343 条（211 个已推路径更新哈希、198 个新路径加入；dm-threads.md 保留旧哈希未动）。同步记录 52 → 58 条。
- 执行脚本：hidden_files/recover-manifest-20261110.py（备份在同目录 .bak-20261110）。独立复核通过。
- 剩余未推内容（dm-threads 拆分后的 part1/part2/... 及 21:00 后新增改动）留待下次定时轮次（2026-11-11 21:00）自动推，不再手动重推。
- build-stage.py 已 patch：dm-threads.md 滚动拆分（每块转义上限 6.0MB），
  生成 workspace/fb-ip/dm-threads-part1.md、part2.md……；原文件不再入暂存。
- 远端 HEAD（本轮结束时）：518f8d39e798ab205be256046dfa56f678142a6e。
  恢复前先用 list_commits 核对 HEAD 未被他人改动。
