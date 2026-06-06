# Pudding

Pudding 是一个桌面 AI 工作区，把对话、共享画布、小组件、技能和语音能力放在同一个应用里。

[English](./README.md)

## 当前状态

Pudding 目前是早期预览版本。这个公开仓库用于展示产品信息和提供发布包下载，源码暂未公开。

第一个预览版本优先支持 macOS。稳定版本之前，API、数据格式和运行资源打包方式仍可能调整。

## 你可以用 Pudding 做什么

- 使用你配置的模型服务或本地模型服务进行对话。
- 在对话旁边保留共享画布，用来沉淀表格、图表、Markdown、看板等内容。
- 通过 Blocks 创建、打开、安装和管理小组件。
- 使用技能扩展特定任务流程。
- 在输入框中引用端点、技能、小组件和工作文件。
- 使用听写、语音对话、语音播放等可选语音能力。

## 模型服务

Pudding 的对话能力由你配置的模型服务提供。你可以使用 OpenAI-compatible API、OpenRouter、DeepSeek、Gemini、Ollama 等模型来源。

模型凭据和 provider 配置在应用内完成。

## 安装

从 [Releases](https://github.com/teatak/pudding/releases) 下载最新 macOS 版本。

首次安装使用 DMG 包：

1. 下载 `Pudding_<version>_darwin_arm64.dmg`。
2. 打开 DMG。
3. 将 `Pudding.app` 拖入 Applications。
4. 启动 Pudding。

预览版本可能暂未签名或公证。如果 macOS 阻止首次启动，可以在 Finder 中右键应用，选择“打开”。

## 语音运行资源

语音功能需要额外的运行资源。首次开启听写、语音对话或语音播放时，Pudding 会提示安装所需资源，并保存到：

```text
~/.pudding/runtime
```

应用安装包默认不内置较大的语音运行资源。运行资源会通过独立的 `runtime-v1` release 分发。

## 数据目录

Pudding 主要使用两个本地目录：

```text
~/.pudding   # 应用数据、配置、数据库、运行资源、缓存
~/pudding    # 默认用户工作文件夹
```

## 小组件

Pudding 使用“小组件”承载可复用的画布体验。

- package 小组件来自 Widget Hub 安装或用户导入的小组件包。
- snapshot 小组件来自画布内容的保存快照。
- preview 小组件是对话过程中创建的临时草稿，是否安装由用户决定。

## 发布包

App 和 runtime 资源分开版本管理：

- App 使用 `v0.1.0` 这类版本 tag。
- Runtime 资源使用 `runtime-v1` 这类版本 tag。

这样可以让较大的 runtime/model 资源独立于频繁更新的 App 发布。

## 源码和许可

这个仓库目前提供发布包下载和公开产品说明，源码暂未公开。

二进制分发条款、模型资源许可和第三方组件说明会在预览版本收尾时单独补充。
