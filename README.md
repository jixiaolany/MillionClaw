# 🦞 百万爪 — 你的 OpenClaw 桌面管家

<p align="center">
    <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/jixiaolany/MillionClaw/main/docs/assets/logo-text-dark.png">
        <img src="https://raw.githubusercontent.com/jixiaolany/MillionClaw/main/docs/assets/logo-text.png" alt="百万爪" width="400">
    </picture>
</p>

<p align="center">
  <strong>不用命令行，小白也能轻松玩转 OpenClaw</strong>
</p>

<p align="center">
  <a href="https://github.com/jixiaolany/MillionClaw/actions/workflows/build.yml"><img src="https://img.shields.io/github/actions/workflow/status/jixiaolany/MillionClaw/build.yml?branch=main&style=for-the-badge" alt="Build status"></a>
  <a href="https://github.com/jixiaolany/MillionClaw/releases"><img src="https://img.shields.io/github/v/release/jixiaolany/MillionClaw?include_prereleases&style=for-the-badge" alt="GitHub release"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
  <a href="https://discord.gg/clawd"><img src="https://img.shields.io/discord/1456350064065904867?label=Discord&logo=discord&logoColor=white&color=5865F2&style=for-the-badge" alt="Discord"></a>
</p>

**百万爪** 是一款小白友好的 OpenClaw 桌面客户端，让每个人都能轻松装上、用上 AI 助手。

你可以在客户端直接发起对话，也可以前往飞书、微信、Telegram 等 IM 工具中，与你的专属 AI 助手交流。

---

## ✨ 功能特性

<p align="center">
  <img src="docs/images/config.png" alt="可视化配置" width="280">
  <img src="docs/images/im.png" alt="多渠道接入" width="280">
  <img src="docs/images/state_management.png" alt="状态管理" width="280">
</p>
<p align="center">
  <img src="docs/images/safety.png" alt="安全防丢" width="280">
  <img src="docs/images/skills.png" alt="技能扩展" width="280">
</p>

- **环境自检** — 自动检测 Node.js 和 OpenClaw CLI，缺失时自动安装
- **支持 OpenClaw 全量模型** — 支持接入 OpenClaw 的所有模型，也支持自定义添加
- **IM 最新插件接入** — 扫码一键接入飞书、微信、企业微信、钉钉、QQ，自动安装官方插件并写入配置
- **应用即教程** — 小白友好的操作引导和提示
- **功能面板** — 实时监控网关状态、一键重启、修复网关
- **Skills 管理** — 管理各个来源的 skill
- **数据备份** — 提供自动备份和手动备份
- **多平台支持** — 支持 macOS、Windows，开箱即用
- **自动更新** — 支持 OpenClaw 最新版本

## 🎯 为什么会有这个项目

开发百万爪的初心很简单：做一个简单好用的 OpenClaw 桌面管家，让每个人都能轻松装上、用上 AI 助手。

- **降低门槛**：将复杂的配置转化为简单的桌面交互
- **打破壁垒**：让人人都能用上好用、强大的 AI 工具
- **零基础上手**——教程即操作，边看边用，快速入门

## 🚀 快速上手

### Step 1：下载安装

- 下载并打开百万爪客户端
  - GitHub Release：[下载最新版本](https://github.com/jixiaolany/MillionClaw/releases)
- 阅读安全提醒内容并确认继续

### Step 2：环境准备

- 运行环境检测
  - 如果系统检测到已有的 OpenClaw 配置，可直接导入
- 按界面提示，准备开始配置

### Step 3：配置模型

- 进入 AI 提供商界面，等待模型列表加载
- 选择你要用的模型（支持 OpenClaw 全量模型，部分模型支持 OAuth 授权）

### Step 4：接入 IM（可选）

- 进入 IM 渠道界面
- 选择你常用的平台（飞书 / 钉钉 / QQ / 企微）
- 按照界面指引完成接入

### Step 5：开始使用

- 在客户端直接发起对话
- 或者前往你刚刚配置的 IM 工具中，测试你的专属 AI 助手

> 💡 关闭百万爪窗口不会影响后台的 OpenClaw 运行，IM 渠道照常可用。

## 💻 支持环境

- macOS 11 (Big Sur)+
- Windows 10+（x64）

## 🔧 开发

### 推荐开发环境

- Windows 10+ / macOS
- 百万爪（OpenClaw）
- [Codex](https://github.com/openai/codex) 或 [Claude Code](https://claude.ai/code)
- Node.js 22+

### 源码安装

```bash
# 克隆仓库
git clone https://github.com/jixiaolany/MillionClaw.git
cd MillionClaw

# 安装依赖
npm install

# 启动开发环境
npm run dev

# 构建生产版本
npm run build
```

### 常用命令

| 命令 | 说明 |
|------|------|
| `npm run dev` | 启动开发服务器 |
| `npm run build` | 构建并打包应用 |
| `npm test` | 运行测试 |

### 项目结构

```
electron/
  main/             主进程（窗口管理、CLI 调用、IPC 处理）
  preload/          预加载脚本（安全桥接）
src/
  pages/            页面组件（向导步骤、Dashboard、聊天等）
  components/       UI 组件
  lib/              业务逻辑（渠道注册、提供商注册等）
  shared/           共享模块（配置流程、网关诊断等）
  assets/           图标与静态资源
docs/               项目相关文档（架构说明、变更日志等）
scripts/            构建与发布脚本
build/              应用图标与打包资源
```

## 🛡️ 安全说明

百万爪连接真实的即时通讯平台。请勿将管理权限随意授予他人。

## 📄 开源许可

基于 MIT 协议分发。详情参见 [`LICENSE`](LICENSE)。

## 🙏 致谢

感谢 [OpenClaw](https://github.com/openclaw/openclaw)——没有它就没有百万爪，我们只是站在巨人肩膀上搭了个小梯子。

感谢 [Electron](https://www.electronjs.org/)、[React](https://reactjs.org/)、[Vite](https://vitejs.dev/) 等众多开源项目。

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/jixiaolany">jixiaolany</a>
</p>