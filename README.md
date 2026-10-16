<div align="center">

> [English](./README_en.md) | 简体中文

<img src="assets/logo.svg" alt="homebrew-tap" width="128">

# homebrew-tap — AgentSend 的 Homebrew Tap

**一条 `brew` 命令，把 AgentSend 装进你的 Mac 或 Linux。**

[![Homebrew](https://img.shields.io/badge/Homebrew-tap-FBB040?logo=homebrew&logoColor=white)](https://brew.sh)
[![agentsend](https://img.shields.io/github/v/release/RayMorTwinkle/agentsend?label=agentsend)](https://github.com/RayMorTwinkle/agentsend/releases)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux-blue)](#-包含的-cask)

</div>

## 这是什么

本仓库是 [AgentSend](https://github.com/RayMorTwinkle/agentsend) 的官方 Homebrew tap——一个面向 Agent 的文件传输工具，支持局域网直传、P2P 中继与异步信箱。cask 定义由 [GoReleaser](https://goreleaser.com) 在每次发版时自动生成更新，无需手工维护。

官网：<https://agentsend.raymor.top>

## 🚀 安装

```bash
brew tap RayMorTwinkle/tap
brew install --cask agentsend
```

升级与卸载：

```bash
brew upgrade --cask agentsend     # 升级到最新版本
brew uninstall --cask agentsend   # 卸载
brew untap RayMorTwinkle/tap      # 移除本 tap
```

## 📦 包含的 Cask

| Cask | 版本 | 平台 | 说明 |
|---|---|---|---|
| [`agentsend`](./Casks/agentsend.rb) | `0.3.0` | macOS (Apple Silicon / Intel)<br>Linux (arm64 / x86_64) | Agent-first 文件传输：局域网、P2P 中继与异步信箱 |

> **说明**：`agentsend` 以 cask 形式分发预编译二进制（`binary "agentsend"`）。在 macOS 上安装后，`postflight` 会自动执行 `xattr -dr com.apple.quarantine` 移除隔离属性，无需手动允许运行。

## 📄 License

本仓库仅包含 Homebrew cask 定义（由 GoReleaser 自动生成）。AgentSend 软件本身的许可见其主仓库 [RayMorTwinkle/agentsend](https://github.com/RayMorTwinkle/agentsend)。
