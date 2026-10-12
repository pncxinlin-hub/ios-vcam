# VCAM 编译排错版 0.2.0（未经真机验证）

这是从用户上传的旧 ZIP 修改的**测试版本**，不是已验证可用的摄像头替换工具。

修改：从编译目标暂时移除 AntiDetection.x / RuntimeProtection.x（原文件保留），移除全局 NSObject 照片 Hook，取消反调试检查与系统级隐藏 Hook；统一设置页的 streamURL 与 MJPEG 默认地址；修正 example-config.plist；移除冒充 Apple 的包信息。

注意：原始摄像头代理逻辑仍有运行风险；未在 Theos/macOS 上实际编译。GitHub Actions 成功不等于 iPhone RootHide 兼容，且本包并非 IPA。请先在测试设备上验证，避免在关键应用中使用。OBS 输入源与 FFmpeg 监听配置仍需单独搭建和核实；默认脚本不提供 RTMP 服务器。

GitHub 上传：Code -> Add file -> Upload files（覆盖文件时建议本地 git 提交），或使用 git clone 后复制这些文件并 git push。Actions 自动构建后下载 Artifacts 中的 .deb。失败时提供 Build 中第一个 error。
