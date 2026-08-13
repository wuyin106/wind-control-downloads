# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.17` 是 Windows prerelease，来自私有 main `bcbcb4fb9c4903765fa66dd00627947f2a3c12f1`。本版本修复 TikTok 分享切换期间的严格 Compact AX 瞬态空树重试，并强化手机 App/Agent 安装身份与版本内容校验。Windows 构建来自 Actions run `31685006694`，手机安装器来自 run `31684770602`。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.17-win10-x64.zip`
- Windows ZIP 大小：31,741,480 bytes
- Windows ZIP SHA-256：`542ab217c68d824efd00ed3240aea08d5c47e98e05ebfa0dc681efa51d277ed0`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.45.ipa`
- 手机 IPA 大小：4,401,634 bytes
- 手机 IPA SHA-256：`df3a17d0326d7afc2a1acc052e56c99811346740f17af4fe5d0e265659a3fa1b`
- Agent：`0.4.45`；Bootstrap：`1.4.46` / build `4046`；手机 App：`0.4.45` / build `4045`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.17
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级、熄屏保活、旧机迁移确认或 TikTok AX descendant 真实语义验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。旧 beta1、beta2、beta0.0.3 至 beta0.0.16 Release 保留不变。
