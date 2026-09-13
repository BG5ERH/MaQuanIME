# 码圈输入法 MaQuanIME

码圈输入法是一款面向 Windows、Android、Linux 与 HarmonyOS 的中文输入法，兼顾形码、拼音、双拼和个人词库。项目使用同一套 Rust 核心统一候选检索、排序、用户学习、码表导入与检字范围规则，各端保留适合自身平台的界面和交互。

[官方网站](https://maquan.app/) · [下载页面](https://maquan.app/download) · [GitHub Release 0.1.84](https://github.com/BG5ERH/MaQuanIME/releases/tag/v0.1.84) · [使用说明](https://maquan.app/guide) · [更新记录](https://maquan.app/changelog) · [隐私声明](https://maquan.app/privacy/)

当前公开稳定版：

- Windows / Android / Linux / HarmonyOS：`0.1.84`

## 本次更新

四端同步直接辅助码、词组联想和整句性能优化。双拼可选择直接或间接辅助码；直接模式每字自由补 0、1 或 2 位辅助码，自造词及简码参与识别。词组联想在上屏后显示后续文字，拼音、形码独立开关，默认关闭。

优化全拼、双拼和形码的整句查询、冷启动及缓存复用；鸿蒙调整面板和输入会话生命周期。保留快符、个人词库按方案导入导出、首道双拼、首右辅助码与整句标点等功能，模型及模型信息不变。

详见[本版说明](release-notes/RELEASE_NOTES_0.1.84.md)、[整句输入说明](https://maquan.app/guide/smart-sentence-and-local-ai)和[个人词库说明](https://maquan.app/guide/auto-phrase-and-personal-dictionary)。

## 主要功能

- 形码、全拼、双拼，以及形码＋拼音组合输入
- 五笔、郑码、仓颉、宇浩等常见形码，也可以导入自己的码表
- 全部、GB18030、通用规范汉字三档形码检字范围
- 个人词库、自造词、调频、固定排序与词频排序
- 本地 AI 候选预测：一口气打完整句再看候选，判断全在本机完成
- 形码智能整句（实验）：全识别支持 2 / 3 / 4 码混合连打；两码模式保留每字前两码连打，编码按识别边界分组显示
- 拼音附加词源、Emoji、颜文字和英文 / IT 词库
- Windows 皮肤编辑、Rime 风格配色、圆角与多字体回退
- Android / HarmonyOS 全键盘、T9、剪贴板、常用语、光标编辑和多套皮肤
- 26 键与 30 键布局都支持；另有一套带独立 `; , . /` 键的皮肤，双拼与 30 键形码可直接使用
- 使用 30 键方案时，先在形码设置里打开对应的 30 键开关
- 官方三码郑码整套键位：字顶字、一/二/三级简码与标点顶字，装上官方码表即生效，无需开关
- Linux 同时提供 IBus 与 Fcitx5，支持 APT / DNF 软件源升级
- 个人词库同步；输入法核心不上传用户的输入内容

## 下载

| 平台 | 获取方式 |
|---|---|
| Windows | [MaQuanIME 0.1.84 安装程序](https://maquan.app/download) |
| Android | [官网 APK 0.1.84](https://maquan.app/download) |
| Linux | [DEB / RPM 与软件源](https://maquan.app/download) |
| HarmonyOS | [0.1.84 在线正式签名 HAP](https://maquan.app/download)，安装受设备及签名授权范围限制；也可关注华为应用市场 |
| macOS / iOS | 开发中 |

GitHub Releases 提供 Windows、Android APK、Linux 软件包与 HarmonyOS 在线正式签名 HAP。HAP 是否可安装取决于设备及签名授权，不保证所有设备均可直接侧载。应用市场专用的 AAB、App Pack 和签名材料不会公开上传。

## Linux 安装与卸载

Linux 有两个互斥前端：使用 GNOME 等 IBus 桌面环境请选择 IBus；使用 KDE、Fcitx5 桌面环境请选择 Fcitx5。不要同时安装两个前端包。

### Debian / Ubuntu

IBus：

```bash
sudo apt install ./MaQuanIME-Linux-IBus-0.1.84-amd64.deb
sudo reboot
```

Fcitx5：

```bash
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.84-amd64.deb
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
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.84-1.x86_64.rpm
sudo reboot
```

Fcitx5：

```bash
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.84-1.x86_64.rpm
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
