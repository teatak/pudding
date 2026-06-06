# Pudding

Pudding is a desktop AI workspace that brings chat, a shared canvas, widgets, skills, and voice features into one app.

[中文说明](./README.zh-CN.md)

## Status

Pudding is currently an early preview. The public repository is used for product information and release downloads. Source code is not publicly available yet.

The first preview release focuses on macOS. APIs, data formats, and runtime packaging may still change before a stable release.

## What You Can Do

- Chat with configured model providers and local model services.
- Keep useful results on a shared canvas while the conversation continues.
- Create, open, install, and manage widgets from Blocks.
- Use skills to extend Pudding with task-specific workflows.
- Reference endpoints, skills, widgets, and workspace files from the composer.
- Use optional voice features such as dictation, voice dialogue, and speech playback.

## Model Providers

Pudding uses the model providers you configure, including OpenAI-compatible APIs, OpenRouter, DeepSeek, Gemini, Ollama, and other compatible services.

Model credentials and provider settings are configured inside the app.

## Install

Download the latest macOS build from [Releases](https://github.com/teatak/pudding/releases).

For first-time installation, use the DMG package:

1. Download `Pudding_<version>_darwin_arm64.dmg`.
2. Open the DMG.
3. Drag `Pudding.app` into Applications.
4. Launch Pudding.

The preview build may not be signed or notarized yet. If macOS blocks the first launch, open it from Finder with Right Click -> Open.

## Voice Runtime

Voice features require additional runtime assets. When you first enable dictation, voice dialogue, or speech playback, Pudding will prompt you to install the required resources under:

```text
~/.pudding/runtime
```

The app package does not bundle large voice runtime assets by default. Runtime assets are distributed separately through the `runtime-v1` release.

## Data Locations

Pudding uses two main local locations:

```text
~/.pudding   # app data, configs, database, runtime assets, cache
~/pudding    # default user workspace for files created or used with Pudding
```

## Widgets

Pudding uses “widgets” for reusable canvas experiences.

- Package widgets are installed from Widget Hub or imported from a widget package.
- Snapshot widgets are saved from content created in the canvas.
- Preview widgets are temporary drafts created during a conversation and can be installed by the user.

## Releases

App and runtime assets are versioned separately:

- App releases use tags such as `v0.1.0`.
- Runtime assets use tags such as `runtime-v1`.

This keeps large runtime/model assets independent from frequent app updates.

## Source and License

This repository currently provides release downloads and public product information. Source code is not publicly available yet.

Binary distribution terms, model asset licenses, and third-party notices will be documented separately as the preview release is finalized.
