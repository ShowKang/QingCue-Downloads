# 安装说明

## 系统要求

Windows 10/11 x64。安装包内含本地运行所需的 .NET 8 运行时（0.1.17 实测 8.0.30）、
固定版 WebView2（156.0.4314.42）与流式识别模型，无需另装开发环境。
`onnxruntime.dll` 已静态链接 MSVC 运行库，**不需要**单独安装 VC++ Redistributable。

## 安装

1. 校验安装包（见 `checksums/SHA256SUMS.txt`）。
2. 双击 MSI，或：
   ```
   msiexec /i QingCue-0.1.17-r13.3-e469484-win-x64.msi
   ```
3. 默认安装到当前用户 `%LOCALAPPDATA%\Programs\QingCue`，桌面与开始菜单生成入口。

## 升级

保持 UpgradeCode 不变、递增安装修订（本包为修订 17，上一包为修订 16），
可直接覆盖升级已装版本；既有用户数据目录沿用，不另建产品身份。

## 卸载

`设置 → 应用 → 轻词 QingCue → 卸载`。卸载默认保留用户数据；如需彻底清除，手动删除 `%LOCALAPPDATA%\QingCue`。

## 第三方许可

安装目录下：

- `ThirdParty\`：sherpa-onnx 1.13.8、ONNX Runtime 1.28.2、QRCoder 1.6.0、SharpCompress 0.50.7、
  SQLitePCLRaw 3.0.5、SQLite 3.53.4 的许可原文，以及 RareUI / React Bits / Feel / Aerial
  与 NuGet 依赖的声明；逐项来源与哈希见 `ThirdParty\SOURCES.md`。
- `wwwroot\licenses\`：WebAwesome 依赖与 robot-heads 的 MIT 许可。

FontAwesome 未随包分发；页面 CSP `connect-src 'none'`，不会发起 `ka-f.fontawesome.com` 请求。


## 数据位置

- 安装版数据：`%LOCALAPPDATA%\QingCue`（稿件、设置、诊断）。
- 便携版：程序目录旁 `portable.flag` 生效，数据写入同目录 `Data`；移动前先退出程序并连同 `Data` 复制。
- 模型在设置中按需下载并校验 SHA-256；纯定速提词不需要模型。

## 注意

- 安装包未做商业代码签名，首次运行可能出现 SmartScreen 提示；不要因此关闭系统安全检查。
- 本包已完成安装/启动/卸载/重装的自动化验收，但**尚未完成真人朗读、视觉回归、
  多 DPI、实体遥控与断网验收**，仅作候选试用，见仓库 `README.md`。
