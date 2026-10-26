# Hi Hysteria — Hysteria v1 分支

hy1 版本的一键安装脚本，仅作维护：不新增功能，只同步上游地址变更。

主分支是 Hysteria2（`hy2.sh`）。本分支保留 Hysteria v1 的 `hihy` 脚本，供仍在使用 v1 内核的机器使用。

## 安装

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/kaecho/Hi_Hysteria/refs/heads/v1/server/install.sh)
```

安装后运行 `hihy` 调出菜单，`hihy 1` 直接安装。

## 本分支相对原 emptysuns 仓库的变更

1. 内核下载地址改为 `HyNetworks/hysteria`（原 `apernet/hysteria` 组织改名，旧地址靠 301 跳转才能用）
2. 仓库地址改为 `kaecho/Hi_Hysteria` 的 `v1` 分支：自更新、卸载、重装脚本不再走已失效的 `git.io` 短链
3. 内核版本固定为 `HY1_CORE_VERSION`（当前 `v1.3.5`）。`releases/latest` 现在指向 v2，v1 已无新版本，原先每次运行都发起的版本探测已移除
4. 修复卸载脚本清理 crontab 时 `${n}` 未展开、重启任务残留的问题

## 文件

| 文件 | 用途 |
|---|---|
| `server/install.sh` | 主脚本（安装 / 菜单 / 内核更新 / 客户端配置） |
| `server/uninstall.sh` | 卸载 |
| `server/reinstall.sh` | 卸载后重装 |

## 说明

Hysteria v1 已停止更新，上游只接受安全修复。新部署建议使用主分支的 Hysteria2。
