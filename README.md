# QingCue Downloads · 公开分发仓库

本仓库只承载**公开分发物**：安装包、校验文件、安装说明与变更记录。
不含源码、算法实现、训练/调教参数、用户数据库、录音、日志与私有配置。

## 内容

| 路径 | 内容 | 是否入 Git |
| --- | --- | --- |
| `releases/QingCue-0.1.17-r13.3-e469484-win-x64.msi` | 安装包，434,040,993 B | **否**（`.gitignore` 排除 `*.msi`；走 Release 附件分发） |
| `checksums/SHA256SUMS.txt` | 安装包 SHA-256 校验 | 是 |
| `docs/INSTALL.md` | 安装、升级、卸载、数据位置 | 是 |
| `CHANGELOG.md` | 变更记录 | 是 |

安装包作为未跟踪文件保留在 `releases/` 下，是为了让校验文件与安装说明进入版本历史，
同时避免 434 MB 二进制进入 Git 历史（仓库体积、克隆成本与 LFS 依赖问题）。
正式分发时以同一字节、同一 SHA-256 上传为 Release 附件。

## 技术概览

本产品是离线语音跟随提词器：音频、识别、对齐、渲染全部在本机完成。面向开发者的公开说明：

| 文档 | 内容 |
| --- | --- |
| [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) | 五层架构、各层职责与层间数据流 |
| [`docs/CAPABILITIES.md`](docs/CAPABILITIES.md) | 能力边界：能做什么、何时不保证、哪些属实验性 |
| [`docs/TECHNOLOGY.md`](docs/TECHNOLOGY.md) | 技术难点与解决思路的抽象叙述 |
| [`docs/TESTING.md`](docs/TESTING.md) | 已验证的测试结论与**未验证清单** |

这些文档只描述架构与已验证范围，不含算法实现、参数、训练资料或内部模块命名；
实现细节不随安装包与公开仓库分发。

## 校验

```
Get-FileHash .\releases\QingCue-0.1.17-r13.3-e469484-win-x64.msi -Algorithm SHA256
```

应得到 `9305BBFC7D29B4460F0C71048B7718D9EC44D02F9CB1C39230716850741014EC`
（亦可用 `certutil -hashfile <文件> SHA256`）。构建完成后已实测一致。

## 源码追溯

安装包内 `build-provenance.json` 记录：

- `sourceRevision`：`e46948411173195c310215a85f541fbac9feec60`
- `sourceTree`：`03783c028e6104ddf58c21eac119cea561e19867`
- 构建时工作区干净（`sourceWorkTreeClean=true`）

安装目录 `ThirdParty/` 与 `wwwroot/licenses/` 内含逐项许可原文；来源与哈希见
`ThirdParty/SOURCES.md`。

## 状态：**候选试用，非正式发布**

- 安装运行验收：**已完成自动化全生命周期**（卸载→安装→启动→卸载→重装，
  退出码均为 0；968 文件 / 1,035,068,039 B；卸载保留 `%LOCALAPPDATA%\QingCue`）。
  仅证明安装链路，不等于功能验收。
- 真人现场朗读：**未验证**。跟随质量与物理开口延迟无真人证据。
- 实体手机遥控、多显示器 DPI、实际断网：**未验证**。
- 本安装包**未做商业代码签名**；依赖微软运行时二进制签名核验。

因此本仓库当前只作**候选分发**用途：可交付内部试用，不得对外宣称「已发布/已验收」。

