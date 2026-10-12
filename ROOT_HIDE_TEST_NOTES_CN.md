# VirtualCamPro 源码检查与测试说明

本包是源码修改版，不是已验证可用的 DEB。

## 已修改
- 设置页视频地址 key 从 `rtspURL` 改为 `streamURL`，与 Tweak.x 中的读取字段一致。
- 将设置页的 RTSP 默认地址清空，避免误认为适配器支持 RTSP。
- 地址标签改为 `Stream URL (HLS / HTTP)`。

## 仍需解决
- 当前工程使用 THEOS_PACKAGE_SCHEME=rootless、Architecture=iphoneos-arm64；不是原生 RootHide 包。
- 需要检查 RootHide Patcher 转换后 PreferenceLoader 注册 plist、bundle、动态库的实际路径。
- 当前相机替换 Hook 仍属实验代码，不能保证 OBS 视频能代替真实摄像头。
- AVAssetStreamAdapter.m 主要实现 HLS 和 HTTP 流路径，不要直接填 rtsp:// 地址。
- 修改后请先在测试设备上检查设置入口，遇到 Settings 闪退立即关闭 Tweak Injection 并卸载该插件。
