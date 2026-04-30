<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎯 Soc Ops — Social Bingo

**Quebre o gelo, faça conexões e vença no networking!**

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WebAssembly](https://img.shields.io/badge/Blazor-WebAssembly-512BD4?logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-222?logo=github)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[🎮 **Jogar agora**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/) · [📚 **Guia do Lab**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/) · [🗂️ **Guia Offline**](workshop/pt_BR/GUIDE.md)

</div>

---

Soc Ops é um jogo de bingo social interativo projetado para encontros presenciais, eventos de equipe e conferências. Os jogadores recebem uma cartela aleatória única e competem para encontrar pessoas que correspondam às perguntas — quem conseguir 5 em uma fileira primeiro vence!

Este repositório também funciona como um **workshop prático de GitHub Copilot Agent** onde você vai transformar o app usando fluxos de trabalho agênticos com IA no VS Code.

---

## ✨ Funcionalidades

- 🎲 **Cartelas aleatórias** — Cada jogador recebe uma disposição única
- 💾 **Salvamento automático** — Continue seu jogo de onde parou
- 🏆 **Detecção de bingo** — Detecção automática de vitórias em linhas, colunas e diagonais
- 🎉 **Tela de celebração** — Modal de vitória digna de confetes
- 📱 **Mobile-first** — Funciona ótimo em celulares durante eventos

---

## 🚀 Início Rápido

### Pré-requisitos

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) ou superior

### Executar Localmente

```bash
cd SocOps
dotnet run
# Abrir http://localhost:5166
```

### Compilar

```bash
dotnet build SocOps/SocOps.csproj
```

### Abrir no GitHub Codespaces

Use este template e depois:

1. Clique em **Code** → **Codespaces** → **Create codespace on main**
2. Aguarde o devcontainer terminar a configuração
3. Execute `dotnet run --project SocOps/SocOps.csproj`

---

## 🎓 Workshop — VS Code Copilot Agent Lab

> **Duração:** ~1 hora · **Nível:** Intermediário · **Stack:** C# / .NET 10 / Blazor

Transforme este app usando o Modo Agente do VS Code com GitHub Copilot. Você vai praticar fluxos de trabalho agênticos reais, desde engenharia de contexto até TDD multi-agente.

### O Que Você Vai Aprender

| # | Habilidade | Descrição |
|---|-----------|-----------|
| 1 | **Engenharia de Contexto** | Ensine a IA sobre seu código com instruções personalizadas |
| 2 | **Primitivos Agênticos** | Use agentes em segundo plano, agentes na nuvem e fluxos personalizados |
| 3 | **Desenvolvimento Design-First** | Deixe a IA iterar na UI enquanto você guia a visão |
| 4 | **Desenvolvimento Guiado por Testes** | Use agentes TDD para funcionalidades robustas e bem testadas |

### Partes do Lab

| Parte | Título | Tempo |
|-------|--------|-------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Visão Geral & Lista Rápida | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Configuração & Engenharia de Contexto | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Frontend Design-First | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Desenvolvimento Multi-Agent | 20 min |

> 📝 Os guias do lab também estão disponíveis na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## 🎨 Personalize Seu Jogo

Edite `SocOps/Data/Questions.cs` para usar suas próprias perguntas quebra-gelo:

```csharp
public static readonly List<string> QuestionsList = new()
{
    "tem um animal de estimação",
    "fala mais de 2 idiomas",
    "sua pergunta personalizada aqui",
    // ... adicione 24+ perguntas para uma cartela completa
};
```

---

## 🛠️ Stack Tecnológico

| Camada | Tecnologia |
|--------|-----------|
| Framework | Blazor WebAssembly (.NET 10) |
| Estilos | Utilitários CSS personalizados (inspirados no Tailwind) |
| Estado | Serviços com persistência em `localStorage` |
| Deploy | GitHub Pages via GitHub Actions |

## 📁 Estrutura do Projeto

```
SocOps/
├── Components/     # BingoBoard, BingoSquare, modais
├── Models/         # Estado do jogo e modelos de dados
├── Services/       # Lógica do jogo e gerenciamento de estado
├── Data/           # Banco de perguntas
└── wwwroot/        # Assets estáticos e utilitários CSS
```

---

## 🚢 Deploy

Pushes para `main` fazem deploy automático no GitHub Pages:

```
https://{usuario}.github.io/{nome-repo}
```

---

## 📄 Licença

MIT — use no seu próximo evento!
