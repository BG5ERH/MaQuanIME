# 码圈输入法 0.1.53

本版修复双拼核心切分边界，并以同一份 0.1.53 / ABI 14 核心重建 Windows、Android、Linux 和 HarmonyOS。

- 双拼按方案的物理两键音节固定解析，不再交给全拼切分器二次拆分。
- 自然码 `hbxrpl` 现在稳定按 `hou | xuan | pai` 解析，不再短暂出现“后续安排、后序安排”。
- 精确查询、前缀查询、个人词库、补全和整句解码均遵守固定双拼边界；全拼行为不变。
- 九种双拼方案、411 个标准音节、真实完整 JDX 和性能门禁均通过。
- Windows 实装、Android 连续唤起、Debian/Fedora 真实输入及 HarmonyOS 发布签名模拟器均已回归。

官网：https://maquan.app/

QQ 群：304771624
