# Pudding

Pudding is a local-first desktop AI workspace for conversations that need more than a chat window. Work with
models, keep useful results on a shared canvas, and use browser, widget, skill, and voice capabilities without
breaking the flow of a session.

[中文说明](./README.zh-CN.md) · [Download the latest release](https://github.com/teatak/pudding/releases/latest)

> Pudding is currently an early preview. The public repository hosts product information, release downloads, and
> the starter catalog. Source code is not public yet.

## Highlights

- **Multi-session workspace**: keep independent conversations and project context available side by side.
- **Shared canvas**: preserve documents, tables, images, widgets, browser pages, and other useful results.
- **Tools that stay visible**: work with the built-in browser, terminal, camera, desktop capture, and installed apps.
- **Extensible workflows**: use widgets, skills, MCP tools, and app integrations for task-specific work.
- **Flexible model access**: connect OpenAI-compatible APIs, OpenRouter, DeepSeek, Gemini, Ollama, and other
  compatible services.
- **Optional voice features**: use dictation, voice dialogue, and speech playback when the required runtime is
  installed.

## Install

The current preview targets macOS on Apple silicon.

1. Download `Pudding-<version>-arm64.dmg` from [Releases](https://github.com/teatak/pudding/releases/latest).
2. Open the DMG and drag `Pudding.app` into **Applications**.
3. Open Pudding.

### First launch on macOS

Current preview builds are signed with a Developer ID certificate and notarized by Apple. On first launch, macOS
may ask you to confirm that you want to open an application downloaded from the internet; choose **Open**.

## Local Data

Pudding keeps application state, configuration, the local database, and installed runtime assets on your Mac:

```text
~/.pudding   # app data, configuration, database, runtime assets, and cache
~/pudding    # default workspace for user files
```

Model requests are sent to the provider you select. Provider credentials and model profiles are configured inside
Pudding.

## Voice Runtime

Voice features use optional runtime assets stored under `~/.pudding/runtime`. Pudding prompts before installing
them, so the desktop package does not need to bundle large speech models by default. Voice assets are published
separately under the `runtime-v1` release.

## Widgets and Skills

- **Widgets** are reusable canvas experiences installed from Widget Hub, imported from packages, or saved from
  canvas content.
- **Skills** provide task-specific instructions and workflows that can be reused across sessions.
- **Preview content** created during a conversation remains temporary until you choose to keep or install it.

## New-session Content

- [`catalog/starter-prompts.json`](./catalog/starter-prompts.json) contains clickable prompts that are submitted
  to the selected model when the user chooses one.
- [`catalog/user-messages.json`](./catalog/user-messages.json) contains a localized title and optional subtitle for
  the new-session screen, plus an optional external link. The content is displayed directly and is never inserted
  into the composer or sent to a model. Raw HTML is not supported.

Pudding periodically reads both public catalogs and caches them locally. It does not upload interaction data.

## Releases and Updates

- Desktop releases use tags such as `v0.1.1`.
- Runtime assets use tags such as `runtime-v1`.
- Signed preview builds can download updates in the background. Installation only starts after the user chooses
  **Restart to Update**; the latest DMG remains available as a manual fallback.

App and runtime releases remain separate so large speech assets do not need to be downloaded with every desktop
update. Previous releases remain available for rollback.

## Source and License

This repository currently provides public product information, release downloads, and catalog data. Binary
distribution terms, model asset licenses, third-party notices, and source availability will be documented as the
preview matures.
