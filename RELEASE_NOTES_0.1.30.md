# 码圈输入法 0.1.30

本版继续统一 Windows、Android 与 Linux 的形码能力，重点完成“第 N 码首选自动上屏”和 Android
本地码表导入收口。

## 主要变化

- 形码新增“第 N 码首选自动上屏”，0 表示关闭、1–16 可配置；拼音与双拼不受影响。
- Android 的极点 `.mb`、冰凌文本、Rime 静态词典导入统一进入共享 Rust 核心，不在客户端复制
  解析与排序规则。
- Rime `sort: original / by_weight`、整数／百分比权重、冰凌权重与原生 `.mb` 顺序均有回归覆盖。
- 导入文件选定后可修改显示名称；当前码表、列表和快捷切换使用同一名称。
- Android 形码候选支持后续编码提示，余码紧跟候选字并使用对应候选字的皮肤颜色。
- 三端重新构建 0.1.30 共享核心；Android AppGallery AAB 仅供应用市场上传，不在本 Release 提供。

## Linux 安装

GNOME 通常选择 IBus；KDE、Xfce 或已经使用 Fcitx5 的桌面选择 Fcitx5。两套前端不要同时安装。

```bash
# Debian / Ubuntu / Deepin / UOS
sudo apt install ./MaQuanIME-Linux-IBus-0.1.30-amd64.deb
# 或
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.30-amd64.deb

# Fedora / RHEL
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.30-1.x86_64.rpm
# 或
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.30-1.x86_64.rpm
```

安装或升级 Linux 包后请完整重启系统，再添加或测试输入法。

## 文件校验

下载同目录的 `SHA256SUMS` 后执行：

```bash
sha256sum -c SHA256SUMS
```
