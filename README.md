# 通用控制 Windows 发布

这里仅用于公开分发“通用控制”Windows 安装包、手机端通用安装器和经过 Ed25519 数字签名的更新清单。

- 本仓库不包含源代码、手机连接密钥、设备资料或更新签名私钥。
- Windows 客户端会先验证 `latest.json.sig`，再校验更新包的大小和 SHA-256；任何一项不匹配都会拒绝安装。
- 公开下载不代表开放源代码或授权他人重新打包、转售。

源代码保存在独立的私有仓库中。

## 当前发布

`v0.8.0-beta0.0.14` 是 Windows prerelease，来自私有 main `62d458e35a550db8d75f89cc89303717802391a1`。本版本修复了 TikTok 编辑页同一健康会话中的瞬时 UI 快照异常处理，并保留真实断线的独立重连门禁；Windows 构建来自 Actions run `31660673991`，手机安装器来自 run `31660472364`。

- Windows ZIP：`wind-control-Windows-v0.8.0-beta0.0.14-win10-x64.zip`
- Windows ZIP 大小：31,675,786 bytes
- Windows ZIP SHA-256：`d607baf37df34076c11849b40f8b4d3c96d7ed12380553dc6408b5953cad7e9a`
- 手机 IPA：`WindControl-Bootstrap-Generic-0.4.42.ipa`
- 手机 IPA 大小：4,357,301 bytes
- 手机 IPA SHA-256：`63ff516cd003ace24ce3afe3fac309be443b1d092522118d7553229a7b2c93e2`
- Agent：`0.4.42`；Bootstrap：`1.4.43` / build `4043`
- schema 7 / atomicUITap=true
- Release：https://github.com/wuyin106/wind-control-downloads/releases/tag/v0.8.0-beta0.0.14
- 自动更新清单：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json
- 自动更新签名：https://raw.githubusercontent.com/wuyin106/wind-control-downloads/main/latest.json.sig

本 Release 为 prerelease，不代表 Windows 真机首次安装、运行、升级或 TikTok/Files 全流程验收已完成；客户端仍须验证 Ed25519 签名、HTTPS、大小和 SHA-256，并由用户确认后才安装。旧 beta1、beta2、beta0.0.3 至 beta0.0.13 Release 保留不变。
