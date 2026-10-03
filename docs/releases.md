# Windows 1.6.27 / Android 1.0.24 / iOS 1.0.22

本次重新构建 Windows 与 Android；iOS 使用此前已构建的 1.0.22（build 23），本次未重新编译。

## 本次修复

- Android 补齐扫码库所需的 AndroidX 运行依赖，修复启动相机时提示 `ContextCompat` 类缺失的问题。这项错误与电脑端无关。
- Windows 补齐旧版 Android WebView 缺少的接口，修复连接成功后对话列表为空、提示 `replaceChildren is not a function` 的问题。
- 扫码初始化失败时返回并显示可复制的错误信息，便于进一步排查。

## 自上次公开版以来的更新

- 用户消息显示发送时间，助手回答显示生成完成时间，按手机所在时区展示。
- 权限选项与 Codex 原生对应：请求批准、帮我批准、完全访问权限；回读一致后才提示同步成功，从下一轮生效。
- 输入框底部“发送新消息”与权限文字字号统一。
- 下载直接写入 App，关闭下载列表继续下载；离开 App 时暂停，回来后手动继续，保留已下载进度。
- 已完成文件直接复用，避免重复下载；电脑端支持 Range 续传，文件变化时提示重新下载。

## 更新与验证

电脑关闭旧助手并运行 Windows 1.6.27，手机安装新版后重新连接或刷新页面。对话页面由电脑端提供，只更新 APK 无法替换旧网页。

EXE、APK 已完成构建、版本和完整性检查；已确认 AndroidX 的 ContextCompat、ActivityCompat、Fragment 类实际打入新 APK。IPA 沿用此前构建产物并再次核对版本及 SHA-256。尚未进行最新版本真机交互验证。

IPA 未签名，需要自行签名后安装。安装包校验值见同一发布页的 SHA256SUMS.txt。

## 致敬与感谢

本项目最初基于 [try2love/codex-mobile-bridge](https://github.com/try2love/codex-mobile-bridge) 扩展，感谢原作者的开源分享，也欢迎大家支持上游项目。本公开仓库仅分发安装包、说明、配图及许可证，本地程序源码保留。

## 社区推荐

最后安利一下 [LINUX DO](https://linux.do/)：**Linux.do 网站好，值得逛逛！** 欢迎去交流技术、分享经验，也欢迎把好用的工具互相推荐给有需要的朋友。
