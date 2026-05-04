🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

<div align="center">

# 🎯 Soc Ops — Social Bingo

**Break the ice, make connections, win at networking!**

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WebAssembly](https://img.shields.io/badge/Blazor-WebAssembly-512BD4?logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-222?logo=github)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[🎮 **Play Now**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/) · [📚 **Lab Guide**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/) · [🗂️ **Offline Guide**](workshop/GUIDE.md)

</div>

---

Soc Ops is an interactive social bingo game built for in-person mixers, team events, and conferences. Players get a unique randomized card and race to find people who match the prompts — first to 5 in a row wins!

This repo also doubles as a **hands-on GitHub Copilot Agent workshop** where you'll transform the app using AI-powered agentic workflows in VS Code.

---

## ✨ Features

- 🎲 **Randomized boards** — Every player gets a unique card arrangement
- 💾 **Auto-save progress** — Resume your game right where you left off
- 🏆 **Bingo detection** — Automatic win detection across rows, columns, and diagonals
- 🎉 **Celebration screen** — Confetti-worthy victory modal
- 📱 **Mobile-first** — Designed to work great on phones at events

---

## 🚀 Quick Start

### Prerequisites

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) or higher

### Run Locally

```bash
cd SocOps
dotnet run
# Open http://localhost:5166
```

### Build

```bash
dotnet build SocOps/SocOps.csproj
```

### Open in GitHub Codespaces

Use this template, then:

1. Click **Code** → **Codespaces** → **Create codespace on main**
2. Wait for the devcontainer to finish setup
3. Run `dotnet run --project SocOps/SocOps.csproj`

---

## 🎓 Workshop — VS Code Copilot Agent Lab

> **Duration:** ~1 hour · **Level:** Intermediate · **Stack:** C# / .NET 10 / Blazor

Transform this app using VS Code's Agent Mode with GitHub Copilot. You'll practice real agentic workflows from context engineering to multi-agent TDD.

### What You'll Learn

| # | Skill | Description |
|---|-------|-------------|
| 1 | **Context Engineering** | Teach AI about your codebase with custom instructions |
| 2 | **Agentic Primitives** | Use background agents, cloud agents, and custom workflows |
| 3 | **Design-First Development** | Let AI iterate on UI while you guide the vision |
| 4 | **Test-Driven Development** | Use TDD agents for reliable, well-tested features |

### Lab Parts

| Part | Title | Time |
|------|-------|------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Overview & Checklist | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Setup & Context Engineering | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Design-First Frontend | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Custom Quiz Master | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Multi-Agent Development | 20 min |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## 🎨 Customize Your Game

Edit `SocOps/Data/Questions.cs` to swap in your own icebreaker prompts:

```csharp
public static readonly List<string> QuestionsList = new()
{
    "has a pet",
    "speaks more than 2 languages",
    "your custom prompt here",
    // ... add 24+ prompts for a full board
};
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Blazor WebAssembly (.NET 10) |
| Styling | Custom CSS utilities (Tailwind-inspired) |
| State | Scoped services with `localStorage` persistence |
| Deployment | GitHub Pages via GitHub Actions |

## 📁 Project Structure

```
SocOps/
├── Components/     # BingoBoard, BingoSquare, modals
├── Models/         # Game state & data models
├── Services/       # Game logic & state management
├── Data/           # Question bank
└── wwwroot/        # Static assets & CSS utilities
```

---

## 🚢 Deployment

Pushes to `main` automatically deploy to GitHub Pages:

```
https://{username}.github.io/{repo-name}
```

---

## 📄 License

MIT — use it for your next event!
