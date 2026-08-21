# Pudding

<p align="center">
  <strong>桌面上的 AI 工作区。</strong><br />
  运行彼此独立的 AI 会话、处理本地项目，并让有用结果始终留在对话旁边。
</p>

<p align="center">
  <a href="https://github.com/teatak/pudding/releases/latest"><strong>下载 macOS 版本</strong></a>
  · <a href="https://x-t.top">官网</a>
  · <a href="./README.md">English</a>
</p>

<p align="center"><sub>macOS · Apple 芯片与 Intel · 早期预览</sub></p>

![Pudding 功能总览](./assets/readme/01-welcome.png)

> **早期预览：**这个公开仓库用于分发 Pudding 安装包、产品资料和公开目录数据，应用源码未在这里发布。

## 功能

### 独立会话

每个对话都是独立工作区，拥有自己的对话、项目、工具、权限和实时活动。多个任务可以同时推进，一个任务的上下文
不会悄悄混入另一个任务。

- 创建独立对话，或把对话归入项目。
- 在侧边栏搜索历史会话，并归档暂时不需要的内容。
- 从已有回答分支出新会话，探索不同方向。
- 为每个任务选择模型和推理强度。

### AI 执行过程与结果始终可见

Pudding 可以调用工具、修改文件，并把结果展示在对话旁。工具活动会出现在对话记录里，权限请求保持明确，文件变化
可以先审阅再继续。

![Pudding 创建并审阅 Markdown 文件](./assets/readme/02-agent-workflow.png)

工作区可以同时放置文件预览、差异、浏览器页面、文档、表格、图片和可复用小组件。有价值的成果不必消失在长篇
对话记录中。

### 内置浏览器与桌面工具

在对话旁打开浏览器，让研究和后续执行留在同一个会话中。得到授权后，Pudding 还可以使用本地终端工具、采集图片、
操作电脑界面并处理项目文件。

![Pudding 在 AI 会话旁打开内置浏览器](./assets/readme/03-built-in-browser.png)

- 以标签页同时保留多个工作区资源。
- 不离开当前任务即可加入网页和采集结果。
- 在专用差异视图中审阅本地文件变化。
- 任务发生变化时，可以取消仍在运行的模型输出。

### 本地项目

只有任务需要时才选择文件夹。项目文件仍保留在你选择的目录中，每个会话分别保存自己的对话和工具活动。Pudding
会明确请求能力和目录访问权限，而不是默认允许每个对话读取整台电脑。

### Apps、Skills 与 MCP

内置应用提供浏览器、画布、电脑操作、图像采集和创作工具。你可以安装 GitHub、Gmail 等可选应用，连接 MCP 服务，
或为重复工作创建可复用技能。

![Pudding 的内置应用、已安装应用和应用目录](./assets/readme/04-apps.png)

- **应用**封装可复用的集成，包括 REST、GraphQL 和 MCP 工具。
- **技能**提供面向特定任务的说明与可重复工作流。
- **小组件**是可收藏并复用的交互式工作区结果。

### 自选模型

Pudding 可连接 OpenAI、Anthropic、Google Gemini、DeepSeek、Qwen、小米 MiMo、Moonshot/Kimi、智谱 GLM、
OpenRouter、Ollama 以及自定义兼容接口。模型请求会发送到你配置的服务；Pudding 不会把云端模型包装成本地模型。

### 按需使用语音

Pudding 支持听写、语音对话和语音播放。语音资源是保存在 `~/.pudding/runtime` 下的可选下载，桌面安装包无需默认
携带体积较大的语音模型。

## 下载与安装

当前预览版本同时支持 Apple 芯片和 Intel 芯片的 macOS。

| Mac | 安装包 |
| --- | --- |
| Apple 芯片 | `Pudding-<版本>-arm64.dmg` |
| Intel | `Pudding-<版本>-x64.dmg` |

1. 从[最新 Release](https://github.com/teatak/pudding/releases/latest)下载对应的 DMG。
2. 打开安装包，将 **Pudding.app** 拖入“应用程序”。
3. 启动 Pudding。

预览版本使用 Developer ID 证书签名，并已通过 Apple 公证。首次打开时，macOS 可能会确认是否运行从互联网下载的应用。

## Local-first，以及清晰的数据边界

- Pudding 不要求注册 Pudding 账号。
- 对话、设置、本地数据库、已安装应用与技能，以及可选运行资源保存在 `~/.pudding`。
- 项目文件仍留在你选择的目录中。
- 模型请求只会发送到你配置的模型服务。
- 公开的初始目录会缓存在本机，Pudding 不上传目录交互数据。

## 仓库内容

这个仓库是 Pudding 的公开分发中心：

- 桌面版本使用 `v<版本>` 标签。
- 语音运行资源使用 `runtime-v<版本>` 标签。
- [`catalog/starter-prompts.json`](./catalog/starter-prompts.json) 保存快捷提示词，只有用户选择后才会提交给模型。
- [`catalog/user-messages.json`](./catalog/user-messages.json) 保存新会话页的多语言展示文案和可选外部链接；内容不会
  写入输入框或发送给模型，也不支持原始 HTML。

已签名的预览版本可以在后台下载更新，只有用户选择“重新启动以更新”后才会安装。最新版 DMG 仍可用于手动安装或回退。

---

<p align="center">
  <a href="https://github.com/teatak/pudding/releases/latest"><strong>下载 Pudding</strong></a>
  · <a href="https://x-t.top">x-t.top</a>
</p>
