# 码圈输入法 MaQuanIME

码圈输入法是一款面向 Windows、Android、Linux 与 HarmonyOS 的中文输入法，兼顾形码、拼音、双拼和个人词库。项目使用同一套 Rust 核心统一候选检索、排序、用户学习、码表导入与检字范围规则，各端保留适合自身平台的界面和交互。

[官方网站](https://maquan.app/) · [下载页面](https://maquan.app/download) · [GitHub Release 0.1.87](https://github.com/BG5ERH/MaQuanIME/releases/tag/v0.1.87) · [使用说明](https://maquan.app/guide) · [更新记录](https://maquan.app/changelog) · [隐私声明](https://maquan.app/privacy/)

当前公开稳定版：

- Windows / Android / Linux：`0.1.87`；HarmonyOS 开发发行版同为 `0.1.87`，应用市场实际更新以审核上架为准。
- MaQuanTableTool 码表工具：独立版本 `0.1.0`，Windows x64 便携程序。

## 本次更新

**丙午年-中秋特别版 v0.1.87**。月圆人团圆，打字更顺手，祝大家中秋快乐！

桌面端完善编码中途编辑、候选框定位与设置窗口；Windows 修复 Ctrl+Space 中英文切换和英文标点顶字。手机支持连续长句反查，逐字编码单独换行显示，展开后可滚动查看。Linux 改进安装保护与码表导入，仍按 Fcitx4、Fcitx5、IBus 分包。

详见[本版说明](release-notes/RELEASE_NOTES_0.1.87.md)、[完整使用说明](https://maquan.app/guide)、[国产 Linux 安装](https://maquan.app/guide/linux-domestic-install)和[码表工具说明](https://maquan.app/guide/table-tool)。

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
- 按码表识别合法标点码元；多字整句中的标点码元仍有已知限制
- 官方三码郑码整套键位：字顶字、一/二/三级简码与标点顶字，装上官方码表即生效，无需开关
- Linux 提供 Fcitx4 DEB、Fcitx5/IBus DEB 与 RPM，支持 APT / DNF 软件源升级
- 个人词库同步；输入法核心不上传用户的输入内容

## 下载

| 平台 | 获取方式 |
|---|---|
| Windows | [MaQuanIME 0.1.87 安装程序](https://maquan.app/download) |
| Android | [官网 APK 0.1.87](https://maquan.app/download) |
| Linux | [DEB / RPM 与软件源](https://maquan.app/download) |
| HarmonyOS | 通过华为应用市场安装；官网与本页不再提供 HAP 下载 —— 鸿蒙生产设备只接受应用市场那条分发链，别处拿到的包会提示来源不可信 |
| macOS / iOS | 开发中 |
| 码表工具 | [MaQuanTableTool 0.1.0 Windows x64](https://maquan.app/download#table-tool) |

GitHub Releases 提供 Windows 安装程序、Android APK 与 Linux 软件包（含 GPG 签名与校验文件）。HarmonyOS 走华为应用市场，不在此处提供安装包；应用市场专用的 AAB、App Pack 和签名材料同样不会公开上传。

## Linux 安装与卸载

Linux 有三个互斥前端：按当前正在运行的 Fcitx4、Fcitx5 或 IBus 选择，不能只按系统名称或桌面名称猜。Fcitx4 目前只有 DEB。当前包仅支持 x86_64/amd64，最低 glibc 2.28、Fcitx4 4.2.9.6 或 Fcitx5 5.0.21，仍须满足各包依赖。

统一安装入口（先检测，安装时会再次确认；识别不清时停止）：

```bash
curl -fsSLo install-maquan-linux.sh https://maquan.app/install-maquan-linux.sh
bash install-maquan-linux.sh --dry-run
bash install-maquan-linux.sh
# 或明确指定 --framework fcitx4 / fcitx5 / ibus
```

### Debian / Ubuntu

Fcitx4：

```bash
sudo apt install ./MaQuanIME-Linux-Fcitx4-0.1.87-amd64.deb
sudo reboot
```

IBus：

```bash
sudo apt install ./MaQuanIME-Linux-IBus-0.1.87-amd64.deb
sudo reboot
```

Fcitx5：

```bash
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.87-amd64.deb
sudo reboot
```

卸载：

```bash
sudo apt remove maquan-ime-ibus
# 或
sudo apt remove maquan-ime-fcitx5
# 或
sudo apt remove maquan-ime-fcitx4
sudo reboot
```

### Fedora / RHEL 系

IBus：

```bash
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.87-1.x86_64.rpm
sudo reboot
```

Fcitx5：

```bash
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.87-1.x86_64.rpm
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
