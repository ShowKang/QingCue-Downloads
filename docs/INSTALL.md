# 安装说明

## 系统要求

- Windows 10 / 11，64 位
- x64 架构
- MSI 安装包

安装包自包含 .NET 8 运行时与 WebView2，无需另行安装；VC++ 运行库无需单独安装。

语音跟随需要本地语音模型。安装包不含默认识别模型，首次使用需在应用内下载（约 900 MB），下载完成后可离线运行。

## 安装

1. 从 [Release 页面](https://github.com/jaychou1669/QingCue-Downloads/releases/tag/v0.1.17-r13.3) 下载 MSI 与 `SHA256SUMS.txt`。
2. 校验安装包（见 `SHA256SUMS.txt`，或按 [README](../README.md) 中的 `certutil` 命令）。
3. 双击 MSI，按安装向导完成；也可在命令行执行：

   ```
   msiexec /i <下载的 MSI 文件名>
   ```

4. 默认安装到当前用户 `%LOCALAPPDATA%\Programs\QingCue`，并在桌面与开始菜单创建入口。

## 升级

保持升级标识不变、递增安装修订，可直接覆盖已安装版本；既有用户数据目录沿用。

## 卸载

Windows「设置 → 应用 → 已安装的应用」中找到轻词 QingCue，选择卸载。

卸载默认保留 `%LOCALAPPDATA%\QingCue`（稿件、设置与本地模型）；如需彻底清除，请在卸载后手动删除该目录。

## 数据位置

- 安装版：`%LOCALAPPDATA%\QingCue`（稿件、设置、诊断与本地模型）。
- 便携版：程序目录旁 `portable.flag` 生效，数据写入同目录 `Data`；移动前请先退出程序，并连同 `Data` 一起复制。
- 语音模型：在应用内按需下载，保存在上述数据目录；纯定速提词不需要模型。

## 第三方许可

安装目录下提供第三方组件的许可原文与版权说明：

- `ThirdParty\`：随包组件的许可原文、来源与校验信息（逐项见 `ThirdParty\SOURCES.md`）。
- `wwwroot\licenses\`：界面组件的许可声明。

许可文本覆盖实际打包组件，随安装包分发。

## 注意

- 安装包未做商业代码签名，首次运行可能出现 SmartScreen 提示；请核对来源与 SHA-256 后再决定是否继续，不要关闭系统安全检查。
- 安装与卸载的自动化验证已完成；真人朗读、视觉回归、多 DPI、外设与断网验收尚未完成，范围见 [TESTING.md](TESTING.md)。
- 首次下载模型需要网络；下载完成后可离线使用。
