# 码圈输入法 0.1.81

Windows、Android、Linux、HarmonyOS 四端正式更新。

- 修复双拼自造词最后一个音节只输入声母时的平翘舌混入：自然码 `xmz` 不再错误召回「鲜制」，`xmc`、`xms` 同样区分 ch、sh。
- 正确的翘舌键和完整编码仍可找到自造词，例如自然码 `xmv`、`xmvi` 可找「鲜制」。不删除个人词，不改变全拼简拼补全。
- 保留形码全识别/两码整句、编码自动分割、自定义词组、Linux 双拼辅助码，以及 Android 副字符编辑和长候选换行。
- 模型文件和模型信息保持不变。

[官网下载](https://maquan.app/download) · [整句输入说明](https://maquan.app/guide/smart-sentence-and-local-ai)

正式包包括 Windows 安装器、Android 官网在线 APK、Linux IBus/Fcitx5 的 DEB/RPM，以及 HarmonyOS 在线正式签名 HAP。鸿蒙 HAP 安装受设备系统与分发范围限制，不保证可在所有设备直接侧载。

建议升级前备份个人词库。Windows/Linux 更新后重启系统或完整退出旧输入法进程；手机更新后重新打开键盘。

SHA256SUMS 覆盖七个客户端安装包，配套 `.asc` 为签名。Linux 发行公钥指纹：DDEA0C1D2E89534339719927A6560A4AA577299D。
