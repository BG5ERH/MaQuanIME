# 码圈输入法 0.1.83

发布日期：2026-09-12。Windows、Android、Linux、HarmonyOS 正式版同步更新。

- 整句中途输入普通逗号、句号、问号等标点，再继续打字，最后一起确认上屏；成对引号可在中间继续输入。
- 逗号选词、辅助码引导、翻页、方案合法码元和已启用的形码标点顶字仍按对应功能处理。
- 四端新增首道双拼。特殊音节：a=AA、ai=AI、an=AN、ang=AY、ao=AO、e=UE、ei=UI、en=EN、eng=UF、er=ER、o=OO、ou=OU；sh=E、ch=I、zh=V。
- 四端新增首右2.0（20,897字）和首右plus（8,070字）辅助码，首右2.0使用最新修正版，䓛=cs，无需另行导入。
- 现有模型和来源声明未改变。

## 下载与使用

[官网下载](https://maquan.app/download) · [整句输入说明](https://maquan.app/guide/smart-sentence-and-local-ai)

GitHub 附件提供 Windows 安装包、Android 正式直装 APK、Linux Fcitx5/IBus DEB/RPM、HarmonyOS 在线正式签名 HAP，以及 SHA-256、Linux 包签名与公钥。Linux 的 Fcitx5/IBus 两套包二选一。

双拼中逗号若用作辅助码引导符，按逗号后输入的字母会作为辅助码。希望用逗号分句时，请将辅助码引导符设为斜杠 `/`，无需关闭辅助码。

Windows 安装后重新打开使用输入法的应用。Android 覆盖安装需要签名一致，不要为强行覆盖而卸载丢失个人词库。HarmonyOS HAP 的安装受设备与签名授权限制；应用市场 APP 包与签名材料不公开上传。
