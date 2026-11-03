# 安装说明

## 系统要求

Windows 10/11 x64。安装包内含本地运行所需的 .NET 8 运行时、固定版 WebView2 与流式识别模型，无需另装开发环境。

## 安装

1. 校验安装包（见 `checksums/SHA256SUMS.txt`）。
2. 双击 MSI，或：
   ```
   msiexec /i QingCue-0.1.17-r13-r2-startfix-win-x64.msi
   ```
3. 默认安装到当前用户 `%LOCALAPPDATA%\Programs\QingCue`，桌面与开始菜单生成入口。

## 升级

保持 UpgradeCode 不变、递增安装修订（本包为修订 16），可直接覆盖升级已装版本；
既有用户数据目录沿用，不另建产品身份。

## 卸载

`设置 → 应用 → 轻词 QingCue → 卸载`。卸载默认保留用户数据；如需彻底清除，手动删除 `%LOCALAPPDATA%\QingCue`。

## 数据位置

- 安装版数据：`%LOCALAPPDATA%\QingCue`（稿件、设置、诊断）。
- 便携版：程序目录旁 `portable.flag` 生效，数据写入同目录 `Data`；移动前先退出程序并连同 `Data` 复制。
- 模型在设置中按需下载并校验 SHA-256；纯定速提词不需要模型。

## 注意

- 安装包未做商业代码签名，首次运行可能出现 SmartScreen 提示；不要因此关闭系统安全检查。
- 本包尚未完成全生命周期安装运行验收与真人朗读验收，仅作候选试用，见仓库 `README.md`。
