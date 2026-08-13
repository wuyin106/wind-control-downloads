# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.15` 是 Windows prerelease，来自私有 main `b517737d4384b792f24e444081bf230fb8bb731a`。本版本修复了持久控制会话在初始/后续电源续租期间被阻塞或误断开的问题，并统一要求新鲜 heartbeat 才显示“可控制”；同时保留 Photo 后同一健康会话内瞬时 UI 快照重试和真实断线的独立重连门禁。Windows 构建来自 Actions run `31664246078`，手机安装器来自 run `31664060552`。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.15-win10-x64.zip`
- Windows ZIP 大小：31,684,495 bytes
- Windows ZIP SHA-256：`84cc7f9e605967e26d2cda19bde09e748c5e74a06c606d8f3e5e5e30131d518f`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.43.ipa`
- 手机 IPA 大小：4,363,724 bytes
- 手机 IPA SHA-256：`de0f43fcf05a53856f26041d780bcc443a5e6564a1a6f0488c5c0d7bbe6de094`
- Agent：`0.4.43`；Bootstrap：`1.4.44` / build `4044`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.15
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级或 TikTok/Files 全流程验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。旧 beta1、beta2、beta0.0.3 至 beta0.0.14 Release 保留不变。
