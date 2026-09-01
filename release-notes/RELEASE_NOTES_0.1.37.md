# 码圈输入法 0.1.37

本版完成四端共享核心升级，新增社区实验 AI 基座与形码空码控制，并集中清理在线码表污染数据。

## 主要变化

- Windows、Android、Linux 与 HarmonyOS 接入 `compact-v2-lccc-20260829-r1` 社区实验模型。模型校验失败、用户关闭功能或运行条件不满足时，自动回退既有候选路径。
- 形码新增“第 N 码候选落空时清空输入”，默认关闭，可选第 2 至第 6 码；只影响形码，拼音与双拼不受影响。
- 091、092 在线码表移除 `z` 前缀扩展区中的网址、个人主页、店铺名、快捷命令和个人文本。原始来源文件不改，清理规则固化在可重复执行的构建脚本与测试中。
- Android 应用市场离线包与 HarmonyOS 离线包统一使用最新 32 表目录，构建时逐表核对大小与 SHA-256。
- 完成 Windows 安装、Android 包资源、Debian 13/Fedora 44 IBus 与 Fcitx5 真输入、HarmonyOS 7.0 模拟器设置返回与形码空码功能回归。

## Linux 安装

GNOME 通常选择 IBus；KDE、Xfce 或已经使用 Fcitx5 的桌面选择 Fcitx5。两套前端不要同时安装。

```bash
# Debian / Ubuntu / Deepin / UOS
sudo apt install ./MaQuanIME-Linux-IBus-0.1.37-amd64.deb
# 或
sudo apt install ./MaQuanIME-Linux-Fcitx5-0.1.37-amd64.deb

# Fedora / RHEL
sudo dnf install ./MaQuanIME-Linux-IBus-0.1.37-1.x86_64.rpm
# 或
sudo dnf install ./MaQuanIME-Linux-Fcitx5-0.1.37-1.x86_64.rpm
```

安装或升级 Linux 包后请完整重启系统，再添加或测试输入法。

## 文件校验

下载同目录的 `SHA256SUMS` 后执行：

```bash
sha256sum -c SHA256SUMS
```

GitHub Release 不提供应用市场专用 AAB、HarmonyOS 安装包或签名材料。
