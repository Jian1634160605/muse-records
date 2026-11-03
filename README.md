# Muse 工作记录存档（私有）

这是成安的 Muse 工作记录自动存档，供 AI 读取、理解历史、偏好、台账与决策。本仓库为私有，不公开。

## 目录结构（与本机路径对应）

- `home/`：本机 `~/` 下的核心记录——`MEMORY.md`（长期记忆）、`USER.md`、`AGENTS.md`（操作手册）、`PROACTIVE_PREFERENCES.md`、`SOUL.md`、`IDENTITY.md`、`TOOLS.md`
- `memory/`：本机 `~/memory/`——每日日志（`2026-XX-XX.md`）、人物档案（`people/`）、群组档案（`groups/`）
- `workspace/`：本机 `~/workspace/` 下的工作记录——FB 运营（`fb-ip/`、`fb-ops/`）、X 运营（`x-ops/`、`goals/x/`）、目标工作区（`goals/`）、交付物（`your_files/` 文本部分）、自定义技能（`custom-skills/`）等

## 入库范围与排除

- 入库：文本记录（Markdown / JSON / 文本），即 AI 可读的内容。
- 不入库：一切凭据与密钥（密码、API key、cookie、代理账号密码）、媒体与二进制文件、缓存、浏览器会话数据、运行时内部索引（`memory/bank`、`memory/index`）、备份文件（`*.bak*`）、虚拟环境。
- 打码说明：`memory/2026-10-26.md` 中一处带账号密码的代理 URL 已打码为 `http://<redacted-proxy>`，原文未改动，其他内容原样。

## 同步方式

- 每日自动同步：新增与变更的文件会追加推送；路径保留原样（含冒号等特殊字符）。
- 时间范围：2026-10-17 起。
