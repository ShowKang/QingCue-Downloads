<p align="center">
  <img src="./assets/brand/qingcue-logo-banner.png" alt="轻词 QingCue" width="520">
</p>

<h1 align="center">轻词 QingCue</h1>

<p align="center"><strong>让文字配合你的表达</strong></p>

<p align="center">Windows 桌面提词器：稿子在眼前，进度跟着你的语速走，声音与文字都留在本机。</p>

<p align="center">
  <a href="https://github.com/jaychou1669/QingCue-Downloads/releases/tag/v0.1.17-r13.3"><strong>下载 Windows 版</strong></a>
  &nbsp;·&nbsp; <code>0.1.17 + r13.3</code> &nbsp;·&nbsp; Windows 10 / 11 x64
</p>

<p align="center">
  <img src="./assets/brand/badge-version.png" alt="版本 v0.1.17-r13.3" height="22">
  <img src="./assets/brand/badge-platform.png" alt="Windows 10 / 11 x64" height="22">
</p>

<p align="center"><sub>0.1.17 + r13.3 为安装与分发修订版本，语音识别与跟随能力沿用 0.1.17。</sub></p>

---

## 把稿件放在眼前

<p align="center">
  <img src="./assets/screenshots/workbench.png" alt="轻词 QingCue 提词工作台" width="100%">
</p>

左侧是稿件目录与句子列表，中间是当前句与上下文，右侧是文字与画面参数，底部是进度与语速趋势。开场前三十秒，视线就已经落在该看的地方。

---

## 核心功能

<sub><strong>已实现</strong>：本节功能均可在当前版本中使用。<strong>条件支持</strong>：语音跟随需要先准备本地语音模型，首次使用需在应用内下载（约 900 MB），完成后可离线运行；模型就绪前可先用定速提词。</sub>

### 自然语音跟随 · 逐词滑动<sub>　已实现</sub>

<img src="./assets/screenshots/follow.png" alt="语音跟随进行中，高亮逐词移动" width="100%">

你按自己的节奏说，高亮以词为单位向前移动、画面连续滚动；停顿、回看或重复一句时，阅读位置通常保持稳定。

<sub>画面为回放样本驱动的真实运行截图，非真人朗读。首次使用语音跟随需在应用内下载模型，之后可离线。</sub>

### 悬浮提词<sub>　已实现</sub>

<img src="./assets/screenshots/floating-bar.png" alt="悬浮提词窗" width="100%">

独立置顶窗口，放在镜头旁边也不遮挡主要内容；位置和大小都可以自己调。

### 稿件管理<sub>　已实现</sub>

<img src="./assets/screenshots/library-folders.png" alt="稿件库与文件夹" width="100%">

稿件、文件夹与展开状态一目了然。分类只是本地整理，稿件内容不会被改写。

### 个性化设置<sub>　已实现</sub>

<img src="./assets/screenshots/preferences.png" alt="设置与本地能力" width="100%">

模型、麦克风、跟随方式集中在一处；字号、行距、段间距与画面颜色在工作台右侧随手可调。

---

## 动态演示

<p align="center">
  <img src="./assets/demos/follow-demo.gif" alt="语音跟随演示：开始、停顿、续读与下一句衔接" width="880">
</p>

<p align="center"><sub><strong>演示由回放样本驱动，非真人朗读。</strong>样本音频由本机语音合成生成，画面为真实应用连续录制，未做静态拼帧。</sub></p>

- **开始即跟随**：点击开始后，画面很快进入跟随状态，当前句随即高亮。
- **停顿续读**：停顿期间阅读位置保持不变，恢复说话后从当前位置继续推进。
- **下一句衔接**：当前句读完，高亮前移，画面滚动到下一句，底部趋势同步更新。

<sub>语音跟随属条件支持：首次使用需在应用内下载本地语音模型，完成后可离线运行。</sub>

---

## 核心技术

轻词 QingCue 是面向 Windows 的桌面提词应用。界面、语音处理与数据都在本机运行，不依赖云端服务。

- **桌面应用**：安装后即可使用，可与常见录制、直播工具并行运行。
- **本地语音处理**：语音识别在本机完成，音频不上传。
- **实时文本同步**：把正在说的话与稿件中的位置对应起来，让画面跟得上真实表达。
- **连续阅读呈现**：以连续的视觉移动代替整页切换，阅读位置稳定、过渡自然。
- **本地数据管理**：稿件、设置与使用数据保存在本机，由用户自行管理。

<sub>以上只说明产品方向与工程取舍，不涉及具体实现、参数或内部流程。</sub>

---

## 使用场景

- `短视频口播`　一条接一条地录，稿子跟得上语速，重录次数更少。
- `视频录制`　面对镜头不用低头找词，视线留在镜头上。
- `日常演讲`　把悬浮窗放在视线边缘，台上不用背稿。
- `内容创作`　边想边录，稿件按文件夹收好，下一次接着写、接着录。

---

## 下载与安装

- 版本：`0.1.17 + r13.3`（Release tag `v0.1.17-r13.3`）
- 系统：Windows 10 / Windows 11，x64
- 安装包：[Windows MSI 安装包](https://github.com/jaychou1669/QingCue-Downloads/releases/tag/v0.1.17-r13.3)（434,040,993 B）
- 校验文件：[SHA256SUMS.txt](https://github.com/jaychou1669/QingCue-Downloads/releases/download/v0.1.17-r13.3/SHA256SUMS.txt)

安装包 SHA-256：

```
9305BBFC7D29B4460F0C71048B7718D9EC44D02F9CB1C39230716850741014EC
```

安装：双击 MSI，按向导完成。安装包尚未做商业代码签名，Windows 可能弹出 SmartScreen 提示；请确认文件来自本仓库并核对 SHA-256，再结合系统提示与自身判断决定是否继续。

首次使用语音跟随时，按界面提示在应用内下载本地语音模型（约 900 MB，实际大小与耗时取决于网络与下载源）。下载完成后识别在本机运行，可离线使用。

卸载：Windows 设置 → 应用 → 已安装的应用 → 轻词 QingCue → 卸载。卸载会保留 `%LOCALAPPDATA%\QingCue` 下的稿件、设置与本地模型，彻底清理可在卸载后手动删除该目录。

> 0.1.17 + r13.3 为安装与分发修订版本，核心语音识别与跟随能力未变。安装生命周期已完成自动化验证，仅代表安装链路；真人朗读与视觉验收范围见 [TESTING.md](docs/TESTING.md)。

---

## 技术文档与常见问题

- [ARCHITECTURE.md](docs/ARCHITECTURE.md)：整体架构与隐私设计
- [CAPABILITIES.md](docs/CAPABILITIES.md)：能力边界与适用场景
- [TECHNOLOGY.md](docs/TECHNOLOGY.md)：技术难点与本地运行要求
- [INSTALL.md](docs/INSTALL.md)：安装、升级与卸载说明
- [TESTING.md](docs/TESTING.md)：已验证结论与未验证清单

**麦克风没有反应？** 在 Windows「设置 → 隐私和安全性 → 麦克风」中允许桌面应用访问，并在应用内选择正确的输入设备。

**一定要下载模型吗？** 普通定速提词不需要模型；语音跟随需要本地语音模型，安装包不含默认识别模型，首次使用需在应用内下载（约 900 MB），完成后即可离线运行，也可在「设置」中导入已有模型。

**模型有多大？要多久？** 下载约 900 MB，耗时取决于网络与下载源；下载完成后解压到本机，之后不再需要联网。

**卸载后还有残留？** 卸载会保留 `%LOCALAPPDATA%\QingCue`，需要彻底清理时手动删除该目录。

**怎么反馈问题？** 通过 [Issues](https://github.com/jaychou1669/QingCue-Downloads/issues) 反馈，附版本号、Windows 版本与复现步骤；请勿上传包含个人信息的稿件或录音。

---

<p align="center"><sub>轻词 QingCue · 0.1.17 + r13.3 · 2026</sub></p>
