# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.11` 是 Windows prerelease，来自私有 main `975438a54ab990e63e15b35d914bce22b6b98938`。本版本包含 TikTok 音乐候选延迟加载/过渡树处理和手机安装器正式 bundle identity 修复；Windows 构建来自 Actions run `31590742287`，手机安装器来自 run `31590391308`。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.11-win10-x64.zip`
- Windows ZIP 大小：27,307,005 bytes
- Windows ZIP SHA-256：`15031f7bbf038b207f03d5f4552f5b1377d703eb54f3b6223a841356578e1446`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.39.ipa`
- 手机 IPA 大小：4,355,858 bytes
- 手机 IPA SHA-256：`11a2a0e029961a26d24edcf7dc83b6e36c44339354af02662ba17b6b06b11c6c`
- Agent：`0.4.39`；Bootstrap：`1.4.40` / build `4040`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.11
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级或 TikTok/Files 全流程验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。旧 beta1、beta2、beta0.0.3 至 beta0.0.10 Release 保留不变。
