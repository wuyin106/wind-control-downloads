# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.20` 是 Windows prerelease，来自私有 main `762e80c2a09cee72a1a75a772bbff107ea75d0fb`。本版修复零 session 任务启动顺序：先做无 session `/status`，再创建 worker 自有 session，之后才访问 session-scoped diagnostics。Windows 构建来自 Actions run `31700359616`，手机安装器来自 run `31700097902`。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.20-win10-x64.zip`
- Windows ZIP 大小：31,741,270 bytes
- Windows ZIP SHA-256：`e10c1cd42fb5d636d8079736f5657ca75ed7575e9a2ba9218aa0aadd6cf79e6d`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.47.ipa`
- 手机 IPA 大小：4,401,754 bytes
- 手机 IPA SHA-256：`abe910d5295b33c7b622fe6d318d84f62df8a5b0c54979603f52b0422dbf7e3c`
- Agent：`0.4.47`；Bootstrap：`1.4.48` / build `4048`；手机 App：`0.4.47` / build `4047`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.20
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级、熄屏/锁屏/后台及长时间保活、旧机迁移确认或 TikTok AX descendant 真实语义验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。本版不能宣称手机端在系统挂起后可自行重建 listener。旧 beta1、beta2、beta0.0.3 至 beta0.0.19 Release 保留不变。

beta0.0.19 已被真机判定为不合格：启动任务时可能在零 session 阶段错误访问 diagnostics，请勿使用；请改用 beta0.0.20 并等待真机验收。beta0.0.17 的手机安装器启动闪退警告也继续保留。
