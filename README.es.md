<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎯 Soc Ops — Social Bingo

**¡Rompe el hielo, haz conexiones y gana en el networking!**

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WebAssembly](https://img.shields.io/badge/Blazor-WebAssembly-512BD4?logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-222?logo=github)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[🎮 **Jugar ahora**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/) · [📚 **Guía del Lab**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/) · [🗂️ **Guía Offline**](workshop/es/GUIDE.md)

</div>

---

Soc Ops es un juego de bingo social interactivo diseñado para eventos presenciales, reuniones de equipo y conferencias. Los jugadores reciben una tarjeta aleatoria única y compiten por encontrar personas que coincidan con las preguntas — ¡el primero en conseguir 5 en fila gana!

Este repositorio también funciona como un **taller práctico de GitHub Copilot Agent** donde transformarás la app usando flujos de trabajo agénticos con IA en VS Code.

---

## ✨ Características

- 🎲 **Tableros aleatorios** — Cada jugador obtiene una disposición única
- 💾 **Guardado automático** — Retoma tu juego donde lo dejaste
- 🏆 **Detección de bingo** — Detección automática de victorias en filas, columnas y diagonales
- 🎉 **Pantalla de celebración** — Modal de victoria digna de confeti
- 📱 **Mobile-first** — Diseñado para funcionar bien en teléfonos durante eventos

---

## 🚀 Inicio Rápido

### Requisitos Previos

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) o superior

### Ejecutar Localmente

```bash
cd SocOps
dotnet run
# Abrir http://localhost:5166
```

### Compilar

```bash
dotnet build SocOps/SocOps.csproj
```

### Abrir en GitHub Codespaces

Usa esta plantilla y luego:

1. Haz clic en **Code** → **Codespaces** → **Create codespace on main**
2. Espera a que el devcontainer termine de configurarse
3. Ejecuta `dotnet run --project SocOps/SocOps.csproj`

---

## 🎓 Taller — VS Code Copilot Agent Lab

> **Duración:** ~1 hora · **Nivel:** Intermedio · **Stack:** C# / .NET 10 / Blazor

Transforma esta app usando el Modo Agente de VS Code con GitHub Copilot. Practicarás flujos de trabajo agénticos reales desde la ingeniería de contexto hasta TDD multi-agente.

### Lo que Aprenderás

| # | Habilidad | Descripción |
|---|-----------|-------------|
| 1 | **Ingeniería de Contexto** | Enseña a la IA sobre tu código con instrucciones personalizadas |
| 2 | **Primitivos Agénticos** | Usa agentes en segundo plano, agentes en la nube y flujos personalizados |
| 3 | **Desarrollo Design-First** | Deja que la IA itere en la UI mientras tú guías la visión |
| 4 | **Desarrollo Guiado por Tests** | Usa agentes TDD para funcionalidades robustas y bien probadas |

### Partes del Lab

| Parte | Título | Tiempo |
|-------|--------|--------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Descripción General & Lista Rápida | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Configuración & Ingeniería de Contexto | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Frontend Design-First | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Desarrollo Multi-Agent | 20 min |

> 📝 Las guías del lab también están disponibles en la carpeta [`workshop/es/`](workshop/es/) para lectura offline.

---

## 🎨 Personaliza Tu Juego

Edita `SocOps/Data/Questions.cs` para usar tus propias preguntas rompehielos:

```csharp
public static readonly List<string> QuestionsList = new()
{
    "tiene una mascota",
    "habla más de 2 idiomas",
    "tu pregunta personalizada aquí",
    // ... agrega 24+ preguntas para un tablero completo
};
```

---

## 🛠️ Stack Tecnológico

| Capa | Tecnología |
|------|-----------|
| Framework | Blazor WebAssembly (.NET 10) |
| Estilos | Utilidades CSS personalizadas (inspiradas en Tailwind) |
| Estado | Servicios con persistencia en `localStorage` |
| Despliegue | GitHub Pages mediante GitHub Actions |

## 📁 Estructura del Proyecto

```
SocOps/
├── Components/     # BingoBoard, BingoSquare, modales
├── Models/         # Estado del juego y modelos de datos
├── Services/       # Lógica del juego y gestión de estado
├── Data/           # Banco de preguntas
└── wwwroot/        # Assets estáticos y utilidades CSS
```

---

## 🚢 Despliegue

Los pushes a `main` se despliegan automáticamente en GitHub Pages:

```
https://{usuario}.github.io/{nombre-repo}
```

---

## 📄 Licencia

MIT — ¡úsalo en tu próximo evento!
