# Pudding

<p align="center">
  <strong>The desktop AI workspace for leading models.</strong><br />
  Separate sessions, a built-in browser and tools, Studio documents and tables, scheduled tasks, and plugins — powered by an open-source core.
</p>

<p align="center">
  <a href="https://github.com/teatak/pudding/releases/latest"><strong>Download</strong></a>
  · <a href="https://teatak.com/products/pudding/">Website</a>
  · <a href="https://github.com/teatak/pudding-core">Core source</a>
  · <a href="./README.zh-CN.md">中文</a>
</p>

<p align="center"><sub>Free for personal and commercial use · Available for macOS (Apple silicon and Intel)</sub></p>

![Pudding workspace](./assets/readme/workspace.png)

> This repository distributes Pudding releases, product information, and public catalog data. The local Agent
> backend is open source under Apache-2.0 in [`teatak/pudding-core`](https://github.com/teatak/pudding-core). The
> desktop UI, Electron shell, native helpers, and packaging are maintained in the private `pudding-desktop`
> repository. Starting with 0.3.5, Pudding Desktop is free for personal and commercial use under its proprietary
> license; earlier builds keep their original license notices.

## Features

### Leading models, ready out of the box

Built-in presets cover OpenAI, Anthropic, Google Gemini, DeepSeek, Qwen, Xiaomi MiMo, Moonshot Kimi, Zhipu GLM,
OpenRouter, Buzz, and Ollama, plus any compatible endpoint. Add an API key and start.

- Choose the model and reasoning effort for each task.
- Use local models through Ollama, or connect a team gateway through [Buzz](https://teatak.com/products/buzz/).
- Model requests go only to the providers you configure.

![Choosing a model in Pudding](./assets/readme/models.png)

### Separate sessions and projects

Each task has its own conversation, model, tools, and permissions, so several tasks can run side by side.

- Start a new chat from any answer to explore a different direction.
- Link a project folder when a task needs one; files stay where they are.
- Set approvals per project: Ask, Auto, or Full access.
- Pin, search, and archive sessions from the sidebar.

### Workspace and tools

Pudding gives models file, command, and code-understanding tools. The workspace keeps file previews, diffs,
browser pages, Studio items, and images open as tabs beside the conversation.

- Read, search, and edit project files, and review every change in a diff view.
- Run commands; stop a running turn at any time and retry a failed one.
- Find definitions and references and check diagnostics for Go and TypeScript.

### Built-in browser and computer use

Browser tabs sit beside the conversation, so research and follow-up work stay in one session.

- Open pages, click, type, capture screenshots, and read page content.
- With your permission, view and operate apps on your computer.
- Capture images from the screen or camera when you ask.

### Studio: documents, tables, and widgets

Documents, tables, and widgets are kept together in Studio, ready to review and revise.

- Markdown documents and typed tables with autosave.
- Select text, cells, or columns and send them to a session for revision.
- Every edit, yours or a session's, is saved as a version you can compare and restore.
- Build interactive widgets from editable React source and preview them with plugin data.
- Import and export CSV, export Markdown, and restore archived items within 30 days.

![A Studio document and its version history](./assets/readme/studio.png)

### Scheduled tasks and collaboration

- Schedule tasks daily or weekly. They run in the original conversation and keep a run history.
- Let the main conversation delegate subtasks, track their progress, and combine the results.
- Get a system notification when a task finishes or needs your approval.

![Scheduled tasks in Pudding](./assets/readme/scheduled-tasks.png)

### Plugins, skills, and MCP

- Built-in plugins provide the browser, collaboration, computer use, image capture, and widget, skill, and plugin
  authoring.
- Install plugins for services such as GitHub and Gmail, or add MCP plugins from an `mcpServers` configuration.
- Turn routine work into reusable skills.

![Built-in and installed plugins](./assets/readme/plugins.png)

### Voice input

Dictate messages with local speech recognition. Voice assets are an optional download, so the installer stays small.

## Download and install

Pudding is currently available for macOS.

| Mac | Minimum macOS | Download |
| --- | --- | --- |
| Apple silicon | 14.0 | [`Pudding-<version>-arm64.dmg`](https://teatak.com/download/pudding/mac-arm64) |
| Intel | 15.5 | [`Pudding-<version>-x64.dmg`](https://teatak.com/download/pudding/mac-x64) |

1. Download the DMG for your Mac. The links above always point to the latest release.
2. Open it and drag **Pudding.app** into **Applications**.
3. Launch Pudding.

Official builds are signed with a Developer ID certificate and notarized by Apple. On first launch, macOS may ask
you to confirm that you want to open an application downloaded from the internet.

Pudding checks for updates in the background. Install updates from the in-app update controls, or download the
latest DMG from [Releases](https://github.com/teatak/pudding/releases/latest).

## Data and privacy

- No Pudding account is required.
- Conversations, settings, the local database, installed plugins and skills, and optional runtime assets stay in
  the `.pudding` folder in your home directory.
- Project files stay in the folders you choose.
- Pudding asks before it accesses folders or operates your apps, and temporary permissions can be reviewed and
  revoked.
- Model requests go only to the providers you configure.
- Public starter catalogs are cached locally, and Pudding does not upload catalog interaction data.

## Repository contents

This repository is the public distribution hub for Pudding:

- Desktop releases use `v<version>` tags; voice runtime assets use `runtime-v<version>` tags.
- [`releases/`](./releases) contains a manifest for each published version: its tag, channel, the desktop and core
  commits it was built from, and its release notes.
- [`catalog/starter-prompts.json`](./catalog/starter-prompts.json) contains clickable prompts that are submitted only
  after the user chooses one.
- [`catalog/user-messages.json`](./catalog/user-messages.json) contains localized, display-only new-session copy and
  an optional external link. It is never inserted into the composer or sent to a model. Raw HTML is not supported.
- [`assets/product/`](./assets/product) contains product launch artwork.
- The open-source Agent backend lives in [`teatak/pudding-core`](https://github.com/teatak/pudding-core).

---

<p align="center">
  <a href="https://github.com/teatak/pudding/releases/latest"><strong>Download Pudding</strong></a>
  · <a href="https://teatak.com/products/pudding/">teatak.com</a>
</p>
