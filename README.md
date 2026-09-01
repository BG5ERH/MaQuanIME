# 码圈输入法 MaQuanIME

码圈输入法是一款面向 Windows、Android、Linux 与 HarmonyOS 的中文输入法，兼顾形码、拼音、双拼和个人词库。项目使用同一套 Rust 核心统一候选检索、排序、用户学习、码表导入与检字范围规则，各端保留适合自身平台的界面和交互。

[官方网站](https://maquan.app/) · [下载页面](https://maquan.app/download) · [GitHub Release 0.1.50](https://github.com/BG5ERH/MaQuanIME/releases/tag/v0.1.50) · [更新记录](https://maquan.app/changelog) · [隐私声明](https://maquan.app/privacy/)

当前公开稳定版：

- Windows / Linux：`0.1.49`
- Android：`0.1.50`
- HarmonyOS：请前往华为应用市场获取

## 主要功能

- 形码、全拼、双拼，以及形码＋拼音组合输入
- 五笔 86 极爽 6.0 / 4.3、小泉郑码等内置方案，并支持导入外部方案
- 全部、GB18030、通用规范汉字三档形码检字范围
- 个人词库、自造词、调频、固定排序与词频排序
- 稳定的本地 AI 基座，以及形码第 2–6 码候选落空自动清空
- 拼音附加词源、Emoji、颜文字和英文 / IT 词库
- Windows 皮肤编辑、Rime 风格配色、圆角与多字体回退
- Android / HarmonyOS 全键盘、T9、剪贴板、常用语、光标编辑和多套皮肤
- Linux 同时提供 IBus 与 Fcitx5，支持 APT / DNF 软件源升级
- 个人词库同步；输入法核心不上传用户的输入内容

## 下载

| 平台 | 获取方式 |
|---|---|
| Windows | [MaQuanIME 0.1.49 安装程序](https://maquan.app/download) |
| Android | [官网 APK 0.1.50](https://maquan.app/download) |
| Linux | [DEB / RPM 与软件源](https://maquan.app/download) |
| HarmonyOS | 华为应用市场搜索“码圈输入法” |
| macOS / iOS | 开发中 |

GitHub Releases 只提供普通用户可以直接安装的 Windows、Android APK 与 Linux 软件包。应用市场专用的 AAB、App Pack 和签名材料不会公开上传。

## Linux 安装与卸载

Linux 有两个互斥前端：使用 GNOME 等 IBus 桌面环境请选择 IBus；使用 KDE、Fcitx5 桌面环境请选择 Fcitx5。不要同时安装两个前端包。

### Debian / Ubuntu

IBus：

```bash
sudo apt install ./MaQuanIME-Linux-IBus-0.1.49-amd64.deb
sudo reboot
```

Fcitx5：

```bash
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.49-amd64.deb
sudo reboot
```

卸载：

```bash
sudo apt remove maquan-ime-ibus
# 或
sudo apt remove maquan-ime-fcitx5
sudo reboot
```

### Fedora / RHEL 系

IBus：

```bash
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.49-1.x86_64.rpm
sudo reboot
```

Fcitx5：

```bash
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.49-1.x86_64.rpm
sudo reboot
```

卸载：

```bash
sudo dnf remove maquan-ime-ibus
# 或
sudo dnf remove maquan-ime-fcitx5
sudo reboot
```

安装或覆盖更新后必须重启系统；仅卸载再安装但不重启，桌面输入法框架可能继续加载旧进程。

## 隐私

码圈输入法的输入服务本身不联网，不上传用户输入内容。官网直装版可按用户主动操作访问在线码表、最新词源与个人词库同步；应用市场离线版不包含网络权限。完整条款见 [隐私声明](https://maquan.app/privacy/)。

## 反馈

- 官网社区：[maquan.app/community](https://maquan.app/community)
- QQ 交流群：`304771624`
- 邮箱：`admin@maquan.app`

Copyright © 码圈输入法。
