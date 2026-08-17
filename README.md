# Pudding

<p align="center">
  <strong>Your AI workspace. On your desktop.</strong><br />
  Independent sessions, a shared canvas, browser and terminal tools, and your choice of model.
</p>

<p align="center">
  <a href="https://github.com/teatak/pudding/releases/latest"><strong>Download for macOS</strong></a>
  · <a href="https://x-t.top">Website</a>
  · <a href="./README.zh-CN.md">中文</a>
</p>

<p align="center"><sub>macOS · Apple silicon and Intel · Early preview</sub></p>

> **Early preview:** this public repository distributes Pudding releases, product information, and public catalog
> data. The application source code is not published here.

## AI work should leave something useful behind

Chat is good for thinking, but real work quickly spreads across browser tabs, terminal windows, files, and long
transcripts. Pudding keeps the conversation, tools, and results together in one desktop workspace.

| 1. Research | 2. Work | 3. Keep the result |
| --- | --- | --- |
| Browse the web without losing the task context. | Use local terminal tools, projects, and connected apps. | Turn useful output into documents, tables, images, and reusable widgets on the canvas. |

Each session keeps its own context, so one task does not silently become another task's memory.

## What Pudding gives you

- **Independent AI sessions** — separate conversations, projects, tools, and context.
- **A canvas beside the chat** — keep documents, tables, images, browser pages, and interactive widgets visible.
- **Desktop tools** — work with the built-in browser, terminal, image capture, voice, and installed apps.
- **Local projects** — let a session work with folders you explicitly choose.
- **Bring your own model** — connect the provider and model that fit the task.
- **Extensible workflows** — add apps, widgets, skills, and MCP tools without turning every task into a new product.

## Download and install

The current preview supports macOS on both Apple silicon and Intel.

| Mac | Download |
| --- | --- |
| Apple silicon | `Pudding-<version>-arm64.dmg` |
| Intel | `Pudding-<version>-x64.dmg` |

1. Download the right DMG from [the latest release](https://github.com/teatak/pudding/releases/latest).
2. Open it and drag **Pudding.app** into **Applications**.
3. Launch Pudding.

Preview builds are signed with a Developer ID certificate and notarized by Apple. On first launch, macOS may ask
you to confirm that you want to open an application downloaded from the internet.

## Local-first, with clear boundaries

- Pudding does not require a Pudding account.
- Conversations, settings, the local database, installed apps and skills, and optional runtime assets live under
  `~/.pudding`.
- Project files stay in the folders you choose.
- Model requests go to the provider you configure; Pudding does not pretend cloud models run locally.
- Public starter catalogs are cached locally, and Pudding does not upload catalog interaction data.

## Models and extensions

<details>
  <summary><strong>Model providers</strong></summary>

Pudding can connect to OpenAI, Anthropic, Google Gemini, DeepSeek, Qwen, Xiaomi MiMo, Moonshot/Kimi, Zhipu GLM,
OpenRouter, Ollama, and custom compatible endpoints.

</details>

- **Apps** package reusable integrations, including REST, GraphQL, and MCP tools.
- **Widgets** are interactive canvas results that can be saved as favorites and reused.
- **Skills** provide task-specific instructions and repeatable workflows.

## Optional voice runtime

Dictation, voice dialogue, and speech playback use optional assets stored under `~/.pudding/runtime`. Pudding asks
before installing them, so the desktop download does not need to bundle large speech models. Voice assets are
published separately under the `runtime-v1` release.

## Repository contents

This repository is the public distribution hub for Pudding:

- Desktop releases use `v<version>` tags.
- Voice runtime assets use `runtime-v<version>` tags.
- [`catalog/starter-prompts.json`](./catalog/starter-prompts.json) contains clickable prompts submitted only after
  the user chooses one.
- [`catalog/user-messages.json`](./catalog/user-messages.json) contains localized, display-only new-session copy and
  an optional external link. It is never inserted into the composer or sent to a model. Raw HTML is not supported.

Signed preview builds can download updates in the background. Installation starts only after the user chooses
**Restart to Update**, and the latest DMG remains available for manual installation or rollback.

---

<p align="center">
  <a href="https://github.com/teatak/pudding/releases/latest"><strong>Download Pudding</strong></a>
  · <a href="https://x-t.top">x-t.top</a>
</p>
