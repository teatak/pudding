# Pudding

[![Pudding — your AI workspace on the desktop](./assets/product/hero.png)](https://github.com/teatak/pudding/releases/latest)

**Research with the browser, run terminal tasks, and keep useful results on a shared canvas—all inside independent
AI sessions that keep their own context.** Bring your own model provider and keep your workspace data on your Mac.

[**Download for macOS →**](https://github.com/teatak/pudding/releases/latest) ·
[See a real workflow](#one-workflow-one-workspace) · [中文说明](./README.zh-CN.md)

> Pudding is currently an early preview. The public repository hosts product information, release downloads, and
> the starter catalog. Source code is not public yet.

## One workflow, one workspace

Ask Pudding to research a topic with the built-in browser, use the terminal when needed, and turn the useful
results into documents, tables, images, or widgets on the canvas. The work stays visible beside the conversation
instead of disappearing into another tab or transcript.

![A Pudding session producing a launch checklist and comparison table on the shared canvas](./assets/product/workspace-overview.jpg)

## Highlights

- **Multi-session workspace**: keep independent conversations and project context available side by side.
- **Shared canvas**: preserve documents, tables, images, widgets, browser pages, and other useful results.
- **Tools that stay visible**: work with the built-in browser, terminal, camera, desktop capture, and installed apps.
- **Extensible workflows**: use widgets, skills, MCP tools, and app integrations for task-specific work.
- **Flexible model access**: connect OpenAI, Anthropic, Gemini, DeepSeek, Qwen, MiMo, Moonshot/Kimi, Zhipu GLM,
  OpenRouter, Ollama, and custom compatible endpoints.
- **Optional voice features**: use dictation, voice dialogue, and speech playback when the required runtime is
  installed.

## Install

The current preview supports macOS on Apple silicon and Intel.

1. Download the DMG for your Mac from [Releases](https://github.com/teatak/pudding/releases/latest):
   - Apple silicon: `Pudding-<version>-arm64.dmg`
   - Intel: `Pudding-<version>-x64.dmg`
2. Open the DMG and drag `Pudding.app` into **Applications**.
3. Open Pudding.

### First launch on macOS

Current preview builds are signed with a Developer ID certificate and notarized by Apple. On first launch, macOS
may ask you to confirm that you want to open an application downloaded from the internet; choose **Open**.

## Local Data

Pudding keeps application state, configuration, the local database, installed apps and skills, and optional
runtime assets under:

```text
~/.pudding
```

Project files stay in the directories you choose; Pudding no longer assumes a fixed `~/pudding` workspace. Model
requests are sent to the provider you select, and provider credentials and model profiles are configured inside
Pudding.

## Voice Runtime

Voice features use optional runtime assets stored under `~/.pudding/runtime`. Pudding prompts before installing
them, so the desktop package does not need to bundle large speech models by default. Voice assets are published
separately under the `runtime-v1` release.

## Apps, Widgets, and Skills

- **Apps** package reusable integrations, including REST, GraphQL, and MCP tools.
- **Widgets** are interactive canvas results that can be kept in your favorites and reused across sessions.
- **Skills** provide task-specific instructions and workflows that can be reused across sessions.

## New-session Content

- [`catalog/starter-prompts.json`](./catalog/starter-prompts.json) contains clickable prompts that are submitted
  to the selected model when the user chooses one.
- [`catalog/user-messages.json`](./catalog/user-messages.json) contains a localized title and optional subtitle for
  the new-session screen, plus an optional external link. The content is displayed directly and is never inserted
  into the composer or sent to a model. Raw HTML is not supported.

Pudding periodically reads both public catalogs and caches them locally. It does not upload interaction data.

## Releases and Updates

- Desktop releases use `v<version>` tags.
- Runtime assets use `runtime-v<version>` tags.
- Signed preview builds can download updates in the background. Installation only starts after the user chooses
  **Restart to Update**; the latest DMG remains available as a manual fallback.

App and runtime releases remain separate so large speech assets do not need to be downloaded with every desktop
update. Previous releases remain available for rollback.

## Source and Distribution

This repository contains public product information, release metadata, downloads, and catalog data. Pudding's
source code is not published in this repository.
