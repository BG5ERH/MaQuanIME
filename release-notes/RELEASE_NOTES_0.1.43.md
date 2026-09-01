# 码圈输入法 0.1.43

0.1.43 是四端专项审计后的统一稳定版。Windows、Android 与 Linux 在本页直接下载；HarmonyOS
请从华为应用市场获取。应用市场 AAB、HarmonyOS App Pack 和源码不公开上传。

## 修复与加固

- Android JNI 改用标准 UTF-8，扩展汉字与 Emoji 不再被 Modified UTF-8 拒绝。
- Android 三种 ABI 原生库增加清空旧输出、ABI 版本戳和 SHA-256 批次门禁。
- Linux IBus/Fcitx5 增加运行时核心 ABI 自检，DEB/RPM 打包阶段再次校验实际共享库。
- HarmonyOS 异步打开拼音会话时，在同一工作线程读取并带回失败原因。
- Android、Linux、HarmonyOS 的长错误文本按需要扩容，不再受固定 1 KiB 缓冲限制。
- Windows 修复超长模块路径可能被静默截断并写入注册表的问题。
- 中文码表文件名获得稳定内部 ID，不再统一退化成 `table`、`table-2`。

## 验证

- 共享核心全量测试、`cargo fmt`、Clippy `-D warnings` 全部通过。
- 正式词库全拼和自然码逐键平均低于 1 ms；短码最慢路径约 5.12 ms。
- Windows x64/x86 构建、签名、静默安装及 COM/TSF 注册通过。
- Android Lint、三 ABI、渠道权限、Android 15 冷安装与崩溃日志检查通过。
- Debian 13 与 Fedora 44 的 IBus、Fcitx5 均完成安装和真实“你好”输入。
- HarmonyOS 在线 HAP 与市场离线 App Pack 完成双架构 ABI 13 的 Release 签名构建。

## Linux 选择

- GNOME 等 IBus 桌面：安装 `MaQuanIME-Linux-IBus-0.1.43-*`。
- KDE 或已使用 Fcitx5：安装 `MaQuanIME-Linux-Fcitx5-0.1.43-*`。
- 两套前端不要同时安装；升级后请完整重启系统。

交流反馈：QQ 群 `304771624`。
