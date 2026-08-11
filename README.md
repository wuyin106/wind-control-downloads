# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta.2` 是 prerelease。附件包括 Windows ZIP、ZIP 的 SHA-256、
重新验证的 `WindControl-Bootstrap-Generic-0.4.37.ipa`、IPA 校验文件和
0.4.37 资源元数据。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta.2-win10-x64.zip`
- Windows ZIP 大小：27,286,228 bytes
- Windows ZIP SHA-256：`f3b9cab113c2e15bcb86cb8a716dd0693fdd186e7a92675869c6649a482bfb09`
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta.2

Windows 真机首次安装、运行和升级验收尚未完成，因此本仓库暂不提供稳定
`latest.json`；完成真实验收后才会更新稳定清单。
