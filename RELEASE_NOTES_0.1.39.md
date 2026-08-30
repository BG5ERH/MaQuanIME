# 码圈输入法 Android 0.1.39

本版为 Android / HarmonyOS 移动端形码功能增量；Windows 与 Linux 当前正式版继续为 0.1.38。

## 主要变化

- 形码设置新增“自由通配符 *”开关，默认关闭。
- 开启后，形码已有候选时左下角“符号”键临时显示为 `*`；按下后直接参与当前编码匹配。
- 一段形码中可以连续输入多个 `*`，首码仍必须是正常形码键；拼音、双拼和英文输入不受影响。
- 动态星号键只替换显示和派发内容，不重建键盘几何布局与触摸命中表，避免候选状态变化影响连续输入。

## 测试

- 共享配置、引擎、移动 ABI 与 Android 单元测试通过。
- HarmonyOS 桌面平价测试 180 项：166 通过，14 项因无设备桥按设计跳过，0 失败。
- 117,757 词五笔表与 426,965 词郑码表完成多次通配性能测试；最慢 P95 为 0.089 ms。
- Android 官网 APK 与 AppGallery 离线 APK/AAB 均完成三 ABI 重编、渠道权限和签名门禁。
- HarmonyOS 1.3.2 离线 App Pack 完成 ABI、32 张随包形码、离线权限与发布签名门禁；市场包不在 GitHub 公开。

## 下载与校验

本 Release 仅公开普通用户可直接安装的 Android APK。AppGallery AAB 与 HarmonyOS App Pack 仅留本地发布目录。

```text
017a5c19f76ac2e77fcac2ba331980623fe734e62bbbc12bf22763d32984bf33  MaQuanIME-Android-Direct-Release.apk
```

交流反馈：QQ群 `304771624`。
