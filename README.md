# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.6` 是 prerelease 文件夹进入判定修复版。附件包括 Windows ZIP、ZIP 的 SHA-256、复用且已验证的 `WindControl-Bootstrap-Generic-0.4.39.ipa`、IPA 校验文件和 0.4.39 资源元数据。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.6-win10-x64.zip`
- Windows ZIP 大小：27,291,854 bytes
- Windows ZIP SHA-256：`f0808e1c09990ffd20a5062c32aa66ba87a689d4bc05190c8bb03a5574b7766c`
- Agent：`0.4.39`；Bootstrap：`1.4.39` / build `4039`
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.6
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

这是测试版自动更新清单，不代表 Windows 真机首次安装、运行和升级验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。
