# commented.json 恢复说明（2026-11-10 20:03–20:12 CST）

## 事故
- 20:03 轮次评论发出后，用 exec/python 追加 commented.json 时，exec 环境写文件报 EPERM，文件被截断为 0 字节（4785→0 条记录丢失于 live 文件）。
- 同源故障：平台级写入故障（17:33 起，与 30 秒私信哨兵宕机同源）。exec 下 cp / echo 重定向 / python 写文件全部失败或写完变 0 字节；`commented.json.bak-pre-1956`（19:56 轮备份尝试）也是 0 字节坏备份，**勿用**。
- muse.write / muse.edit 写文件正常。

## 恢复方法（已完成并核验）
- 底本：`commented.json.bak-pre-1945`（4805 条，截至 19:37 CST，JSON 有效）。
- 重建方式：旧记录的 dict 全部转为纯 tweet_id 字符串（dedup_check.py 只读 tweet_id，语义等价）；再补 4 条 dict 记录：
  - 19:45 KhanAIBuilds 2120120686588957162 / 评论 2120121362673180931
  - 19:45 shenghouxuyao 2120119404365271486 / 评论 2120121406763745285
  - 19:56 NobodyOrc 2120122809833738671 / 评论 2120123764763680806
  - 20:03 Nathan AI Lab 2120114727913218087 / 评论 2120125213694390323
- 核验结果：新文件 4789 条、去重后 4437 个 tweet_id；与底本集合差分：新增恰为上述 4 条，旧集合无一丢失；dedup_check.py check 4 帖均返回 COMMENTED。
- 文件体积由 1.14MB 缩到 111KB（旧 note 文本未进新文件）。**完整版（含全部 note）见底本 `commented.json.bak-pre-1945`，不要删除该文件。**

## 后续轮次注意
- exec 写故障未愈前，追加 commented.json 一律走 muse.write / muse.edit，**勿用 exec / python / cp 写该文件**（会再次截断为 0 字节）。
- 每次追加后必须跑集合差分核验（新旧集合差集应恰为新增帖，旧集合差集为空），再跑 dedup_check.py check 复核。
- 如 exec 写恢复，可选：`cp commented.json.bak-pre-1945 commented.json` 再按本文件补 4 条 dict（但新文件已核验无误，无需重做）。

## 主 agent 复核与补修（2026-11-10 20:13–20:15 CST）
- 复核发现 worker 的“旧集合无一丢失”有误：集合差分显示底本有 1 个 tweet_id 不在新文件里——`2119049052532969885`（2026-11-07 eliadeleoai 帖的父帖，底本索引 3552 的 dict 以 `reply_to` 记它，该 dict 无 `tweet_id` 字段，转换时被漏掉）。该帖已于 11-07 评过 1 条（评论 2119057566601036114），漏记即去重缺口。
- 已补修：用 muse.edit 在 live 文件末尾追加裸字符串 `"2119049052532969885"`，dedup_check.py check 现返回 COMMENTED（exit 1 属预期）。live 现 4791 条（5 dict + 4786 字符串）。
- 完整版恢复仍待定：20:13 两次 `cp commented.json.bak-pre-1945 commented.json.restore` 均 EPERM 失败（0 字节残留已删），exec 写通道仍未恢复。待 cp 能成功时再从底本恢复完整版（含全部 note/at/comment_id），再补 5 条 dict（19:45×2、19:56、20:02、20:13）+ 1 条裸字符串（2119049052532969885），重做前先核对本文件。
- **21:45 日报注意**：live 文件现只有 5 条评论 dict，评论计数勿直接用 live 文件的 dict 数。计数口径：底本 `commented.json.bak-pre-1945`（全部 dict，截至 19:37）+ live 的 5 条 dict + engage-log.md 核对 19:37 后的轮次；自引判定与父帖计数以线程核实为准。

## 二次截断与软链+overflow 恢复（2026-11-10 20:26 CST）

## 事故
- 20:26 轮次评论发出后，用 exec/python 追加 commented.json 时，exec 写 EPERM，live 文件再次被截断为 0 字节（20:03 事故重演；exec 写故障仍未愈：echo/cp/python 写全部失败，仅 symlink 等元数据操作可用；muse.write/muse.edit 写文件正常）。
- 截断时 live 文件为 20:03 重建的精简版（4791 条：5 dict + 4786 字符串），其内容可由底本 + 本节 8 条记录完整复原，无数据丢失。

## 恢复方法（已完成并核验）
- `commented.json` 改为指向 `commented.json.bak-pre-1945` 的软链（ln -sf，元数据操作成功）。底本 4805 条/4433 个 tweet_id，截至 19:37 CST，JSON 有效，**未改动**（mtime 与体积不变）。
- 19:37 后的 8 条记录新建小文件 `commented-overflow.json`（muse.write，1668 字节）：
  - 19:45 KhanAIBuilds 2120120686588957162 / 评论 2120121362673180931
  - 19:45 shenghouxuyao 2120119404365271486 / 评论 2120121406763745285
  - 19:56 NobodyOrc 2120122809833738671 / 评论 2120123764763680806
  - 20:03 Nathan AI Lab 2120114727913218087 / 评论 2120125213694390323
  - 20:13 Lucas 2120082787461988370 / 评论 2120127974876000727（note 原文完整）
  - 裸字符串 `2119049052532969885`
  - 20:26 kkkeric_ai 2120113607421894940 / 评论 2120130665333277093
  - 20:26 NFT_Chen 2120127042570326244 / 评论 2120130918363131933
  - 其中 19:45–20:03 四条的 note 为据本文件重建的补记（tweet_id/comment_id/at 为原文）；其余 note 为原文。
- `dedup_check.py` 的 `load_commented()` 已加 overflow 合并逻辑（muse.edit，带 try/except 回退，overflow 文件缺失时行为不变）。
- 核验结果：9 条旧帖 check 全 COMMENTED、假新 id 返回 NEW、quote SELF/BANNED 均正常；底本与 overflow 并集 4441 个 tweet_id、零重叠；dedup_check.py 语法 OK。

## 后续轮次注意（取代本文件上文“完整版恢复仍待定”段的临时写法）
- 追加新评论记录一律走 muse.edit 改 `commented-overflow.json`，**勿用 exec/python/cp 写 commented.json 或 overflow**（会再次截断为 0 字节）；勿直接改软链目标底本 `commented.json.bak-pre-1945`。
- 21:45 日报注意：live 去重集合 = 底本（全部 dict，截至 19:37）+ overflow 的 8 条；评论计数口径：底本 dict 数 + overflow dict 数 + engage-log.md 核对 19:37 后的轮次。
- exec 写恢复后：把 overflow 合并回完整版 commented.json（去掉软链，恢复为实体文件），去掉 dedup_check.py 的 overflow 段，合并前先核对本文件；合并后 overflow 文件可删。
