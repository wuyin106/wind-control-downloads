# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.10` 是 Windows prerelease，修复 Files 清理 exact folder/ZIP 逐项选择确认：选择模式不再错误要求不存在的 Downloads 标题或图片 Select All 契约，而是绑定原始 Files 行集合签名，并兼容 Select All/Deselect All 两种真实状态；身份、顺序、几何或控件证据歧义时 fail closed，不重复点击目标或 Delete。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.10-win10-x64.zip`
- Windows ZIP 大小：27,299,818 bytes
- Windows ZIP SHA-256：`78d0f6d0eb47e02fcfb59561294c8014b96dab80985163d2bb440cce97e23537`
- Agent：`0.4.39`；Bootstrap：`1.4.39` / build `4039`
- schema 7 / atomicUITap=true
- 资源元数据：`windows-bootstrap-resource.json`
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.10
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级或 Files 清理流程验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。旧 beta1、beta2、beta0.0.3 至 beta0.0.9 Release 保留不变。
