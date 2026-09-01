# 码圈输入法 0.1.32

本版重点改进全拼与双拼的简拼逻辑，并把行为固化到多端共享核心。

## 主要变化

- 全拼继续默认支持主词库、附加词库和用户个人词库简拼。
- 双拼新增两个独立设置：公共词库简拼默认关闭，用户自定义简拼默认开启。
- 用户可为长词设置 `dhgf` 一类自定义短码；候选编码保持用户实际保存的短码。
- 同一自定义短码可对应多个词，所有匹配词均进入候选，不互相覆盖。
- Windows、Android、Linux 使用同一份检索逻辑；鸿蒙只需接入相同配置字段，不另写候选算法。
- AppGallery AAB 仍只保留在本地市场发布目录，不在官网或 GitHub Release 公开。

## Linux 安装

GNOME 通常选择 IBus；KDE、Xfce 或已经使用 Fcitx5 的桌面选择 Fcitx5。两套前端不要同时安装。

```bash
# Debian / Ubuntu / Deepin / UOS
sudo apt install ./MaQuanIME-Linux-IBus-0.1.32-amd64.deb
# 或
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.32-amd64.deb

# Fedora / RHEL
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.32-1.x86_64.rpm
# 或
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.32-1.x86_64.rpm
```

安装或升级 Linux 包后请完整重启系统，再添加或测试输入法。

## 文件校验

下载同目录的 `SHA256SUMS` 后执行：

```bash
sha256sum -c SHA256SUMS
```
