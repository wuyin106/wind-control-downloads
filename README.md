# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.40` 是 Windows prerelease，来自私有源码提交 `4ed7ae64633d1d1dbabc421f8a69a81ede6bff60`。本版修复只读 UI 快照超时后继续使用已关闭预检令牌恢复 worker，导致任务尚未进入业务流程便失败的问题。Windows 与手机端均采用本地构建和直接 Release 上传，不依赖 GitHub Actions artifact storage。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.40-win10-x64.zip`
- Windows ZIP 大小：67,384,139 bytes
- Windows ZIP SHA-256：`d8614f5470567b89177e00df1abfb05b1f01c4a17aa876b0060e7743af9b4236`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.50.ipa`
- 手机 IPA 大小：4,729,502 bytes
- 手机 IPA SHA-256：`91723fcf83876654ea8ac7556915fdb5202e437d2c33010be198ea1b4e3e74c7`
- Agent / 手机 App：`0.4.50` / build `4050`；Bootstrap：`1.4.51` / build `4051`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.40
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。本版未修改 Files、TikTok、音乐、标题标签、Post、清理、队列、并发或定时业务流程。
