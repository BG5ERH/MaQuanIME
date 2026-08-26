# 码圈输入法 0.1.28

发布日期：2026-08-26

本版修复拼音同音词跨页候选排序。旧逻辑会在首屏后先插入大量首音节单字，使第六个及后续
同码完整词被推到很后面；每页候选较少的 Windows 上尤其明显。

修复后，从第二页开始每页最多保留两个逐字候选，其余位置继续按原词频展示完整词。完整词与
单字任一侧耗尽后，由另一侧自然补齐页面。该规则位于共享 Rust 核心，覆盖全拼和全部双拼，
没有针对 `yizhi` 或“移植”硬编码。

## 验证范围

- Windows：x64/x86 Win7 兼容构建、签名 Setup、覆盖安装、TSF 注册和设置中心回归。
- Android：三 ABI 正式核心、官网直装 APK、AppGallery 离线包；模拟器真实自绘键盘输入。
- Linux：Debian 13 与 Fedora 44；IBus、Fcitx5；DEB/RPM 实装、签名和真实 GTK 上屏。

## 安装提示

- Windows 更新后建议注销或重启，确保所有宿主进程加载新 TSF DLL。
- Android 官网用户安装 APK 覆盖升级；应用市场包由市场渠道更新。
- Linux 用户运行 `sudo apt upgrade` 或 `sudo dnf upgrade`，升级后完整重启系统。

官网：<https://maquan.app/download>  
更新记录：<https://maquan.app/changelog>
