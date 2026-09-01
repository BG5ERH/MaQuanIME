# 码圈输入法 0.1.31

本版修复三端共用的极点 4.3 内置码表异常：旧式单字注释和动态宏不再被显示为普通候选。

## 主要变化

- 清理“同(同)”“是(是)”一类旧式单字注释，候选只保留实际汉字。
- 过滤以 `$` 开头的动态宏，避免静音开关等脚本文本进入候选框。
- 归一化后按编码与词条去重，同时保留原始固定词序。
- 极爽 6.0 的动态宏同步过滤；小泉郑码保持现有数据结构。
- Windows、Android、Linux 重新构建，三端内置极点 4.3 文件摘要一致。
- AppGallery AAB 仅保留在本地市场发布目录，不在官网或 GitHub Release 公开。
- Windows 候选框圆角改用分层抗锯齿绘制，修复圆角与较粗边框组合时的锯齿和错位。
- Windows 皮肤模板新增分组后的 Rime 配色，默认候选字号为 22、边框粗细为 2。
- Windows 和 Android 正式包已在 2026-08-28 从当前源码重新构建并替换同版本旧产物。

## Linux 安装

GNOME 通常选择 IBus；KDE、Xfce 或已经使用 Fcitx5 的桌面选择 Fcitx5。两套前端不要同时安装。

```bash
# Debian / Ubuntu / Deepin / UOS
sudo apt install ./MaQuanIME-Linux-IBus-0.1.31-amd64.deb
# 或
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.31-amd64.deb

# Fedora / RHEL
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.31-1.x86_64.rpm
# 或
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.31-1.x86_64.rpm
```

安装或升级 Linux 包后请完整重启系统，再添加或测试输入法。

## 文件校验

下载同目录的 `SHA256SUMS` 后执行：

```bash
sha256sum -c SHA256SUMS
```
