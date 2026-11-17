# ixBrowser Local API V2.0 驱动

给以后在用户 Windows 电脑上跑 10 个 FB/IG 账号的浏览器操作用。
驱动封装官方 Python SDK（`ixbrowser-local-api`，实测版本 1.2.9），
方法名与签名以已安装的 SDK 实测为准（见 `test_connect.py` 自检）。

## 架构（重要）

```
┌──────────────────────────────┐   本机直连（127.0.0.1:53200）
│ 用户 Windows 电脑            │   ┌─────────────────────┐
│  ixBrowser 客户端（开着）    │◄──│ 本驱动（Python）    │
│  Local API 开关已开          │   │ + Playwright（CDP） │
│  10 个 profile（每号一个）   │   └─────────────────────┘
└──────────────────────────────┘
```

- **驱动必须贴着浏览器跑**：ixBrowser Local API 默认只听 `127.0.0.1:53200`，
  `open_profile` 返回的 CDP `debugging_address`（如 `127.0.0.1:9222`）同样只听本机。
  所以驱动进程要跑在 ixBrowser 所在的那台机器上（用户 Windows 电脑），
  不能从另一台机器直接连。
- **跨机器联通方案（二选一，待实测）**：
  1. **Tailscale**：本机（Muse 服务器）加入用户 tailnet 后，试连用户电脑的
     tailnet IP `:53200`。如果 ixBrowser 只绑了 `127.0.0.1`，这条路不通，
     就走方案 2。
  2. **用户电脑上放一个小转发/常驻服务**：在用户电脑本机跑一个小程序，
     一头接 `127.0.0.1:53200` 和 CDP 端口，一头通过 Tailscale 对外提供
     高层指令接口（开 profile、打开页面、截图……），浏览器操作全在本机完成。
- **不要把账号密码写进代码或配置文件**。登录态全部留在 ixBrowser profile 里，
  驱动只调接口开 profile、接 CDP，不碰凭据。

## 安装

```bash
cd ~/workspace/ixbrowser-driver
python3 -m venv .venv
.venv/bin/pip install -r requirements.txt
.venv/bin/python -m playwright install chromium   # CDP 接入本身不需要本机再起浏览器，但备用
```

系统 Python 是 externally managed（PEP 668），必须用虚拟环境，
不要用 `pip install --break-system-packages`。

## 自检

```bash
# 只做本地自检：SDK import + 连通性。没开 ixBrowser 时应报“连不上”，退出码 2。
.venv/bin/python test_connect.py

# 指向远程地址（Tailscale/转发通了以后）
.venv/bin/python test_connect.py --target 100.x.x.x --port 53200

# 连通后列出全部 profile（只打印 profile_id 和 name）
.venv/bin/python test_connect.py --list

# 打开指定 profile 做开/关测试（打开后随即关闭，不留浏览器开着）
.venv/bin/python test_connect.py --profile <profile_id>
```

退出码：0 正常；1 参数/操作失败；2 连不上 ixBrowser Local API。

## 模块用法（`ixbrowser_driver.py`）

```python
from ixbrowser_driver import IxBrowserDriver

# 默认连 127.0.0.1:53200；跨机器时传 target/port
with IxBrowserDriver() as driver:
    ok, msg = driver.check_connection()
    print(msg)  # 不 ok 时 msg 会说明“客户端没开或 Local API 未开启”

    profiles = driver.list_profiles()          # 全部 profile（自动翻页）
    opened = driver.list_opened_profiles()     # 当前已开的 profile

    info = driver.open_profile("PROFILE_ID")   # 返回 {"webdriver": ..., "debugging_address": "127.0.0.1:9222"}
    driver.close_profile("PROFILE_ID")

    # 打开 profile + Playwright 接入，退出时自动断开（不关 profile）
    with driver.attach_session("PROFILE_ID") as (browser, page):
        from ixbrowser_driver import goto_facebook, get_logged_in_account_name, screenshot
        goto_facebook(page)
        print(get_logged_in_account_name(page))  # 读不到返回 None，不编造
        screenshot(page, "/tmp/fb-home.png")
```

主要函数：

| 函数 | 说明 |
| --- | --- |
| `IxBrowserDriver(target, port, timeout)` | 驱动，默认 `127.0.0.1:53200`，超时 `(2, 60)`（开 profile 很慢，读超时放 60 秒） |
| `check_connection()` | 连通性检查，返回 `(ok, 说明)`；连不上时说明里写清“客户端没开或 Local API 未开启” |
| `list_profiles(keyword, group_id, limit)` | 列全部 profile（自动翻页） |
| `list_opened_profiles()` | 列当前已开 profile |
| `open_profile(profile_id, ...)` | 开 profile，返回含 `webdriver` / `debugging_address` 的字典 |
| `close_profile(profile_id)` | 关 profile |
| `reset_profile_open_state(profile_id)` | 重置“显示已开但实际已关”的状态 |
| `get_profile_cookie(profile_id)` | 读 profile cookie（原样返回，不解析） |
| `attach_playwright(debugging_address)` | Playwright 经 CDP 接入，返回 `(playwright, browser)` |
| `attach_session(profile_id)` | 上下文管理器：开 profile + 接入，退出自动断开 |
| `goto_facebook(page)` | 打开 facebook.com，等网络空闲 |
| `get_logged_in_account_name(page)` | 尽力读当前登录账号显示名，读不到返回 `None` |
| `screenshot(page, path)` / `get_page_title(page)` | 截图 / 读标题 |
| `env_target()` | 从环境变量 `IXBROWSER_TARGET` / `IXBROWSER_PORT` 读地址 |

错误处理：所有失败都抛 `IxBrowserError`，消息是中文；SDK 返回 `None`
时取 `client.code` / `client.message` 原样附上。连不上服务时明确区分，
不把“服务没开”说成别的错。

官方参考：
- Local API 文档：https://www.ixbrowser.com/doc/v2/local-api/en
- SDK：https://github.com/ixspyinc/ixbrowser-local-api-python
  （方法索引见 `docs/api-reference.md`；本驱动用到的签名已对 SDK 1.2.9 实测核对）

## 待办（等用户电脑连通后再实测）

1. 用户电脑装 Tailscale（或放转发），Muse 服务器能摸到用户电脑后，
   用 `test_connect.py --target <用户电脑地址>` 实测连通。
2. 实测 `--list` 列出 10 个 profile，核对 profile_id 与账号的对应关系
   （用户在 ixBrowser 里给 profile 起名/分组后提供）。
3. 实测 `--profile <id>` 开/关一个 profile，核对返回的 `debugging_address`，
   再用 `attach_session` 接入并打开 facebook.com、截图、读账号名，
   确认 CDP 链路全通。
4. 若 Tailscale 直连 `:53200` 不通（只绑了 127.0.0.1），改走“用户电脑本机常驻服务”方案，
   再补一个常驻服务脚本。
5. 在此之前不要碰任何账号密码，不要猜 ixBrowser 账号信息。
