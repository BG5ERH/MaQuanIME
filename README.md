# 码圈输入法 MaQuanIME

码圈输入法是一款面向 Windows、Android 与 Linux 的中文输入法，统一支持形码、全拼、双拼以及“形码 + 拼音”混合输入。项目以本地优先、跨平台共享学习和可配置输入体验为核心。

官网：[https://maquan.app/](https://maquan.app/)  
隐私声明：[https://maquan.app/privacy/](https://maquan.app/privacy/)

## 正式版下载

| 平台 | 当前版本 | 下载 |
| --- | --- | --- |
| Windows | 0.1.32 | [统一正式版](https://github.com/BG5ERH/MaQuanIME/releases/tag/v0.1.32) |
| Android | 0.1.32 | [统一正式版](https://github.com/BG5ERH/MaQuanIME/releases/tag/v0.1.32) |
| Linux | 0.1.32 | [统一正式版](https://github.com/BG5ERH/MaQuanIME/releases/tag/v0.1.32) |
| HarmonyOS | 应用市场发行 | 请在华为应用市场搜索“码圈输入法” |
| macOS / iOS | 开发中 | 后续开放 |

大体积安装包统一放在 GitHub Releases，不直接写入 Git 源码历史。每个 Release 均附带 SHA-256 校验信息。

## 主要能力

- 形码、全拼、自然码、小鹤等双拼方案与混合输入。
- 菜籽拼音、本地智能整句、简拼与全拼混输。
- 多平台共享个人词库、调频与标准拼音学习身份。
- Windows 码表管理、皮肤设计器与状态栏配置。
- 形码候选与后续编码提示可选择固定顺序或按词频排序。
- Android 26 键、T9、全键盘模式、Emoji 与自定义布局。
- Linux 同时提供 IBus / Fcitx5 的 DEB 与 RPM 安装包。
- 输入服务本地优先；联网同步和在线资源由用户主动启用。

## 安装提示

### Windows

运行 Setup 安装程序。更新或重装后如果系统仍加载旧输入服务，请完整注销或重启 Windows。

### Android

官网直装版包含在线功能。华为应用市场版按上架要求采用离线功能组合，与官网直装包分开发布。

### Linux

Linux 版分为两种输入法框架：GNOME 默认通常选择 **IBus**；KDE、Xfce 或已经使用 Fcitx5 的桌面选择 **Fcitx5**。两套前端不要同时安装。

Debian / Ubuntu / Deepin / UOS：

```bash
# IBus 版
sudo apt install ./MaQuanIME-Linux-IBus-0.1.32-amd64.deb

# Fcitx5 版
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.32-amd64.deb
```

Fedora / RHEL 系：

```bash
# IBus 版
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.32-1.x86_64.rpm

# Fcitx5 版
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.32-1.x86_64.rpm
```

0.1.27 起安装包会同时安装码圈官方签名公钥与专用软件源。后续版本可随系统更新：

```bash
sudo apt update && sudo apt upgrade   # Debian / Ubuntu
sudo dnf upgrade                      # Fedora / RHEL
```

这不是把 `maquan.app` 整站加入信任。APT 使用独立的 `Signed-By` 公钥，DNF 同时校验 RPM 与仓库
元数据签名，只接受码圈 Linux 发布密钥签署的包。需要无人值守更新时，可按发行版策略启用
`unattended-upgrades` 或 `dnf-automatic`。

安装或升级后请**完整重启系统**。重启后，IBus 用户在“设置 → 键盘 → 输入源 → 中文”添加“码圈输入法”；Fcitx5 用户运行 `fcitx5-configtool`，把“码圈输入法”加入当前输入法列表。

卸载：

```bash
# Debian / Ubuntu，按实际安装版本选择一个
sudo apt remove maquan-ime-ibus
sudo apt remove maquan-ime-fcitx5

# Fedora / RHEL，按实际安装版本选择一个
sudo dnf remove maquan-ime-ibus
sudo dnf remove maquan-ime-fcitx5
```

卸载默认保留 `~/.local/share/jdime` 中的个人设置和词库，便于以后重装恢复。

## 校验下载文件

Windows PowerShell：

```powershell
Get-FileHash .\MaQuanIME-* -Algorithm SHA256
```

Linux / macOS：

```bash
sha256sum MaQuanIME-*
```

## 反馈

请在 [Issues](https://github.com/BG5ERH/MaQuanIME/issues) 提交可复现的问题，并注明平台、系统版本、码圈输入法版本、输入方案和复现步骤。涉及隐私的数据请先脱敏。

输入法作者：菰城菜籽  
联系邮箱：admin@maquan.app
