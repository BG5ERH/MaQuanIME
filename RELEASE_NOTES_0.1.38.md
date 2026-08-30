# 码圈输入法 0.1.38

本版重点解决个人词库刷新与长词候选完整性，并补齐 Windows 个人词库搜索。Windows、Android、Linux 与 HarmonyOS 均从同一份共享核心重新构建。

## 主要变化

- Android 与 HarmonyOS 每次进入个人词库页、提交搜索或点击刷新时重新读取当前落盘数据，不再等待几分钟后的页面更新，也不增加常驻监听。
- Android 从键盘快捷入口进入个人词库前先完成拼音和形码会话写盘。
- Windows 词库管理新增按词条或编码搜索；应用设置后也能立即搜索当前有效方案。
- 共享拼音解码修复低频精确短词不能继续组成长词的问题，真实菜籽拼音索引已回归“青鳉鱼”。
- Debian 13 与 Fedora 44 已实装 DEB/RPM，并分别通过 IBus、Fcitx5 实际上屏“你好”。

## Linux 安装

GNOME 通常选择 IBus；KDE、Xfce 或已经使用 Fcitx5 的桌面选择 Fcitx5。两套前端不要同时安装。

```bash
# Debian / Ubuntu / Deepin / UOS
sudo apt install ./MaQuanIME-Linux-IBus-0.1.38-amd64.deb
# 或
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.38-amd64.deb

# Fedora / RHEL
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.38-1.x86_64.rpm
# 或
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.38-1.x86_64.rpm
```

安装或升级 Linux 包后请完整重启系统，再添加或测试输入法。

## 文件校验

下载同目录的 `SHA256SUMS` 后执行：

```bash
sha256sum -c SHA256SUMS
```

GitHub Release 不提供应用市场专用 AAB、HarmonyOS 安装包或签名材料。

交流反馈：QQ群 `304771624`。
