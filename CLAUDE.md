# CLAUDE.md — 百万爪开发指南

你是一个经验丰富的全栈工程师，正在开发**百万爪**（MillionClaw）——一款小白友好的 OpenClaw 桌面客户端。

## 📋 项目背景

- **项目名称**：百万爪（MillionClaw）
- **GitHub**：https://github.com/jixiaolany/MillionClaw
- **定位**：Windows/macOS 桌面客户端，包装 OpenClaw CLI，让小白用户也能轻松使用
- **技术栈**：Electron + React + TypeScript + Vite + electron-builder
- **参考项目**：https://github.com/qiuzhi2046/Qclaw（功能设计参考）

## 🎯 开发目标

### 短期目标（现在）
1. 完善 GitHub Actions 构建，生成 Windows EXE
2. 创建 electron-builder 配置
3. 编写清晰的项目文档

### 中期目标
1. 开发 Electron 桌面客户端主框架
2. 实现可视化配置界面
3. IM 渠道扫码接入功能

### 长期目标
1. 发布首个可用版本
2. 建立用户社区
3. 持续迭代优化

## 🏗️ 当前架构

```
MillionClaw/
├── .github/workflows/     # GitHub Actions
│   └── build.yml          # 构建 EXE 的 CI/CD
├── docs/                  # 文档目录
│   └── assets/            # Logo 和图片资源
├── electron/              # Electron 主进程（待开发）
├── src/                   # React 前端（待开发）
├── build/                 # 打包资源（图标等）
├── package.json           # npm 配置
├── electron-builder.json  # electron-builder 配置（待创建）
├── README.md              # 项目说明
├── VISION.md              # 愿景文档
└── CLAUDE.md              # 本文件
```

## 🔧 构建流程

GitHub Actions 自动执行以下步骤：
1. Checkout 代码
2. 安装 Node.js 20
3. 安装 pnpm
4. 安装依赖
5. 执行 `pnpm run build:docker`
6. 上传构建产物

## 📝 代码规范

- 使用 TypeScript 进行开发
- 遵循 React 最佳实践
- 使用 Tailwind CSS 进行样式设计
- 组件采用 functional component + hooks

## 🐛 问题排查

### 构建失败
- 检查 Node.js 版本（需要 Node.js 20+）
- 检查 pnpm 安装是否成功
- 查看 GitHub Actions 日志

### 依赖问题
- 删除 node_modules 重新安装
- 检查 package.json 的 peerDependencies

## 🔗 相关链接

- [OpenClaw 主仓库](https://github.com/openclaw/openclaw)
- [Qclaw 参考项目](https://github.com/qiuzhi2046/Qclaw)
- [OpenClaw 文档](https://docs.openclaw.ai)
- [electron-builder 文档](https://www.electron.build/)

---

_Last updated: 2026-03-30_