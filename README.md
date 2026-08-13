# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.16` 是 Windows prerelease，来自私有 main `6ba24040946972350ea7628cab330202c581362d`。本版本加入手机端版本显示与授权 session-ready 后的串行 Agent 更新协调、旧 Agent 的一次 TrollStore 确认引导、更新包安全暂存/校验，以及会话/UI deadline 回归。Windows 构建来自 Actions run `31674705672`，手机安装器来自 run `31674453718`。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.16-win10-x64.zip`
- Windows ZIP 大小：31,734,452 bytes
- Windows ZIP SHA-256：`ef56782aa12158fbfed190318e75873279cf85171a948345ebdb29b5a6facf6f`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.44.ipa`
- 手机 IPA 大小：4,394,757 bytes
- 手机 IPA SHA-256：`bd141d561403ce6eb38a0e974b647c02dd1eebb325ba0fcf3dd0c4cde14d65c2`
- Agent：`0.4.44`；Bootstrap：`1.4.45` / build `4045`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.16
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级、熄屏保活、旧机迁移确认或 TikTok/Files 全流程验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。旧 beta1、beta2、beta0.0.3 至 beta0.0.15 Release 保留不变。
