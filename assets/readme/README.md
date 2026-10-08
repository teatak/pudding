# Pudding 可复用产品图片

README、产品介绍和宣传页面复用下列中英文 PNG。原图已经保存并纳入本仓库的 Git 版本管理，
直接引用版本化归档即可，无需重复截图、重新设计或另存一套同名副本。

## 当前使用

素材修订：**0.5.0 · 2026-10-08**。全部为 **2560 × 1440、16:9 PNG**，沿用 Pudding 现有 Logo。

| 用途 | 中文 | English |
| --- | --- | --- |
| 首页首图、产品总览 | [把想法变成成果](../store/v0.5.0/2026-10-08/zh-cn/01-overview.png) | [Turn ideas into results](../store/v0.5.0/2026-10-08/en-us/01-overview.png) |
| Studio 文档与表格 | [从对话到文档](../store/v0.5.0/2026-10-08/zh-cn/02-studio.png) | [From conversation to creation](../store/v0.5.0/2026-10-08/en-us/02-studio.png) |
| 本地项目与上下文 | [让 AI 理解你的项目](../store/v0.5.0/2026-10-08/zh-cn/03-local-projects.png) | [Bring your project into the conversation](../store/v0.5.0/2026-10-08/en-us/03-local-projects.png) |
| 定时任务与运行记录 | [重复工作交给定时任务](../store/v0.5.0/2026-10-08/zh-cn/04-scheduled-tasks.png) | [Put repeat work on a schedule](../store/v0.5.0/2026-10-08/en-us/04-scheduled-tasks.png) |

## 来源与复用

- [素材来源](../store/v0.5.0/2026-10-08/README.md)记录候选构建、截图环境与演示内容说明。
- [图片清单](../store/v0.5.0/2026-10-08/image-manifest.json)记录文件大小、尺寸、SHA-256 及原始截图校验值。
- 画面来自 Windows 11 ARM64 上的真实 0.5.0 候选程序，使用隔离演示数据，不是真实用户聊天。
  使用时保留演示说明，不把候选界面当作某个平台当前已上架版本的证明。
- 在本仓库中用相对路径引用；供其他网站引用时，可使用公开仓库的版本化路径，例如：

  ```text
  https://raw.githubusercontent.com/teatak/pudding/main/assets/store/v0.5.0/2026-10-08/en-us/01-overview.png
  ```

- 官网需要随构建保存压缩或裁剪副本时，记录原图路径和处理方式，遵循[产物管理约定](../../docs/artifact-management.md)。
- 不覆盖已归档图片。日常发版继续沿用，只有用户明确要求时才制作或更换；新素材另建版本/日期修订。

本目录原有 `workspace.png`、`models.png`、`studio.png`、`scheduled-tasks.png`、`plugins.png` 是早期 README 截图，
保留供历史引用，不作为当前首页主图。Product Hunt 素材另见 [`assets/product/`](../product/README.md)。
