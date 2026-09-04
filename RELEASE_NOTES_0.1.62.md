码圈输入法 0.1.62。Windows、Android、Linux、HarmonyOS 同版本。

## 这一版修了什么

- **修复移动端「表情 emoji」「颜文字」开着也不出候选**：这两份词库此前没有随包发出去，
  开关是空的。现在打 `kaixin` 会在中文首选后面直接出 😄。
- **表情与颜文字固定跟在对应的中文候选后面**，不会被推到后面几屏；**英文与 IT 术语**
  则排到第 9 项之后，不跟中文抢前排。
- **英文与 IT 术语词库改为默认关闭**。此前默认开着，打 `gan` 这类拼音会先冒出一串英文
  单词。需要的话在「附加词库」里打开。
- **九宫格（T9）左列的候选拼法改为带音节分隔显示**（`hao qi e o o d`），此前是连在一起
  的一长串，几条备选肉眼难以分辨。
- 设置里的说明文字改写：不再出现只有开发者看得懂的实现细节，也修正了「附加词库总开关
  管住表情」这类与实际行为不符的描述。

## 校验

Linux 四个包的 SHA-256 见 `SHA256SUMS`（`SHA256SUMS.asc` 是它的分离签名）。RPM 经
`rpm --addsign` 就地签名，**这里的摘要是签名后的**，与本地构建产物不同，以本文件为准。

- Windows `MaQuanIME-Windows-0.1.62-Setup.exe`
  `bf02548e15d21cbfdf575ac177df55f0347d090bdd5f2eda2cf745fe7731c444`
- Android `MaQuanIME-Android-Direct-Release.apk`
  `cad5677b7406c95427b7ad30cbcc80f726666a8cf9703ccc1ec4aa10c13354ff`

发布签名公钥指纹 `DDEA0C1D 2E89 5343 3971 9927 A656 0A4A A577 299D`。

HarmonyOS 版通过华为应用市场发行，不在此处提供安装包。

官网：https://maquan.app/download
