# 码圈输入法 MaQuanIME

码圈输入法是一款面向 Windows、Android 与 Linux 的中文输入法，统一支持形码、全拼、双拼以及“形码 + 拼音”混合输入。项目以本地优先、跨平台共享学习和可配置输入体验为核心。

官网：[https://maquan.app/](https://maquan.app/)  
隐私声明：[https://maquan.app/privacy/](https://maquan.app/privacy/)

## 正式版下载

| 平台 | 当前版本 | 下载 |
| --- | --- | --- |
| Windows | 0.1.25 | [Windows Release](https://github.com/BG5ERH/MaQuanIME/releases/tag/windows-v0.1.25) |
| Android | 0.1.24 | [Android Release](https://github.com/BG5ERH/MaQuanIME/releases/tag/android-v0.1.24) |
| Linux | 0.1.24 | [Linux Release](https://github.com/BG5ERH/MaQuanIME/releases/tag/linux-v0.1.24) |
| HarmonyOS | 应用市场发行 | 请在华为应用市场搜索“码圈输入法” |
| macOS / iOS | 开发中 | 后续开放 |

大体积安装包统一放在 GitHub Releases，不直接写入 Git 源码历史。每个 Release 均附带 SHA-256 校验信息。

## 主要能力

- 形码、全拼、自然码、小鹤等双拼方案与混合输入。
- 菜籽拼音、本地智能整句、简拼与全拼混输。
- 多平台共享个人词库、调频与标准拼音学习身份。
- Windows 码表管理、皮肤设计器与状态栏配置。
- Android 26 键、T9、全键盘模式、Emoji 与自定义布局。
- Linux 同时提供 IBus / Fcitx5 的 DEB 与 RPM 安装包。
- 输入服务本地优先；联网同步和在线资源由用户主动启用。

## 安装提示

### Windows

运行 Setup 安装程序。更新或重装后如果系统仍加载旧输入服务，请完整注销或重启 Windows。

### Android

官网直装版包含在线功能。华为应用市场版按上架要求采用离线功能组合，与官网直装包分开发布。

### Linux

根据桌面环境选择 IBus 或 Fcitx5，并选择发行版对应的 DEB 或 RPM。安装完成后请完整注销或重启系统，避免桌面环境继续加载旧进程。

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

