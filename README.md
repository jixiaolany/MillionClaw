# MillionClaw (百万爪) - Your OpenClaw Desktop Companion

<p align="center">
  <strong>No command line needed - anyone can use OpenClaw easily</strong>
</p>

<p align="center">
  <a href="https://github.com/jixiaolany/MillionClaw/actions/workflows/build.yml"><img src="https://img.shields.io/github/actions/workflow/status/jixiaolany/MillionClaw/build.yml?branch=master&style=for-the-badge" alt="Build status"></a>
  <a href="https://github.com/jixiaolany/MillionClaw/releases"><img src="https://img.shields.io/github/v/release/jixiaolany/MillionClaw?include_prereleases&style=for-the-badge" alt="GitHub release"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
</p>

**MillionClaw (百万爪)** is a user-friendly OpenClaw desktop client that lets everyone easily install and use an AI assistant.

You can chat directly in the client, or go to Feishu, WeChat, Telegram and other IM tools to talk with your AI assistant.

---

## Features

- **Environment Check** - Auto-detect Node.js and OpenClaw CLI, auto-install if missing
- **Full OpenClaw Model Support** - Supports all OpenClaw models, also supports custom additions
- **IM Channel Plugin Integration** - Scan QR code to connect Feishu, WeChat, QQ, auto-install official plugins
- **App as Tutorial** - User-friendly operation guidance and tips
- **Dashboard** - Real-time monitoring, one-click restart, fix gateway
- **Skills Management** - Manage skills from various sources
- **Data Backup** - Auto backup and manual backup
- **Multi-Platform** - Supports macOS and Windows, ready to use
- **Auto Update** - Supports latest OpenClaw version

## Why This Project

The goal is simple: build a simple and easy-to-use OpenClaw desktop companion so everyone can easily install and use an AI assistant.

- **Lower barriers** - Turn complex configuration into simple desktop interactions
- **Break barriers** - Let everyone use great AI tools
- **Zero learning curve** - Tutorials are operations, learn by doing

## Quick Start

### Step 1: Download & Install
- Download and open MillionClaw client
  - GitHub Release: [Download latest version](https://github.com/jixiaolany/MillionClaw/releases)
- Read security notice and confirm to continue

### Step 2: Environment Preparation
- Run environment detection
  - If system detects existing OpenClaw config, import directly
- Follow prompts to prepare

### Step 3: Configure Model
- Enter AI provider screen, wait for model list to load
- Select the model you want to use

### Step 4: Connect IM (Optional)
- Enter IM channel screen
- Select your preferred platform (Feishu / DingTalk / QQ / WeChat Work)
- Follow guidance to complete

### Step 5: Start Using
- Chat directly in the client
- Or go to the IM tool you configured to test your AI assistant

> Note: Closing MillionClaw window won't affect the OpenClaw running in the background - IM channels keep working.

## Supported Environments

- macOS 11 (Big Sur)+
- Windows 10+ (x64)

## Development

### Recommended Environment
- Windows 10+ / macOS
- MillionClaw (OpenClaw)
- [Codex](https://github.com/openai/codex) or [Claude Code](https://claude.ai/code)
- Node.js 22+

### Source Installation

```bash
git clone https://github.com/jixiaolany/MillionClaw.git
cd MillionClaw
npm install
npm run dev
npm run build
```

### Common Commands

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build and package application |
| `npm test` | Run tests |

### Project Structure

```
electron/
  main/             Main process (window management, CLI invocation, IPC)
  preload/          Preload script (secure bridge)
src/
  pages/            Page components (wizard, dashboard, chat)
  components/       UI components
  lib/              Business logic (channel registration, provider registration)
  shared/           Shared modules (config flow, gateway diagnostics)
  assets/           Icons and static assets
docs/               Project documentation (architecture, changelog)
scripts/            Build and release scripts
build/              App icons and packaging resources
```

## Security Note

MillionClaw connects to real IM platforms. Please do not grant management access to others easily.

## License

Distributed under MIT license. See [`LICENSE`](LICENSE).

## Credits

Thanks to [OpenClaw](https://github.com/openclaw/openclaw) - without it there would be no MillionClaw.

Thanks to [Electron](https://www.electronjs.org/), [React](https://reactjs.org/), [Vite](https://vitejs.dev/) and many other open source projects.

---

<p align="center">
  Made with love by <a href="https://github.com/jixiaolany">jixiaolany</a>
</p>