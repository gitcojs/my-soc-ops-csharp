# Copilot Workspace Instructions

## Mandatory Development Checklist

- Lint: run configured analyzers or lint checks; if none exist, say so
- Build: run `dotnet build SocOps/SocOps.csproj`
- Test: run `dotnet test` when test projects exist; otherwise say no tests exist

## Project Summary

Soc Ops is a Blazor WebAssembly social bingo app on .NET 10.

- `SocOps/Components`: board and screen UI
- `SocOps/Services`: gameplay state and bingo logic
- `SocOps/Models`: game data models
- `SocOps/Data`: prompt data
- `SocOps/wwwroot`: static assets and CSS utilities

## Working Rules

- Keep game logic in services, not Razor components, when possible
- Treat `BingoGameService` as the main gameplay state owner
- Match nearby Blazor and C# style
- Reuse utility classes in `SocOps/wwwroot/css/app.css` before adding custom styles

## Design Guide

The app uses a **cyberpunk + liquid glass** theme. All visual decisions must stay consistent with this aesthetic.

### Design Tokens (CSS variables in `app.css`)

| Variable | Value | Role |
|---|---|---|
| `--cyber-bg` | `#050814` | Page background |
| `--neon-cyan` | `#00f5ff` | Primary accent, borders, CTAs |
| `--neon-magenta` | `#ff2d78` | Secondary accent, bingo banner |
| `--neon-yellow` | `#f5e642` | Highlight, modal title |
| `--neon-green` | `#39ff14` | Marked/success state |
| `--glass-bg` | `rgba(5,15,40,0.55)` | Glass panel fill |
| `--glass-border` | `rgba(0,245,255,0.25)` | Glass panel border |
| `--font-cyber` | `Orbitron` | Titles, labels, buttons |
| `--font-body` | `Rajdhani` | Body text, instructions |

### Component Classes (defined in `app.css`)

- **`.cyber-glass`** — glass panel (backdrop blur + semi-transparent fill)
- **`.cyber-square`** — base bingo square; modifiers: `--marked`, `--winning`, `--free`
- **`.cyber-btn`** — primary CTA (neon cyan fill, dark text, glow shadow)
- **`.cyber-btn-ghost`** — secondary/back button (outlined, transparent)
- **`.cyber-header`** — top navigation bar
- **`.cyber-bingo-banner`** — full-width alert strip for bingo state
- **`.cyber-modal`** + **`.cyber-overlay`** — modal dialog and backdrop
- **`.cyber-title`** — glitch-animated page title
- **`.cyber-subtitle`** — uppercase magenta subheading
- **`.cyber-label`** — small uppercase section label (Orbitron)
- **`.cyber-instructions`** — instruction card with top-edge glow line
- **`.cyber-list-item`** — `▸`-prefixed instruction list item
- **`.cyber-checkmark`** — neon-green `✓` on marked squares

### Rules

- Never use light backgrounds (`bg-white`, `bg-gray-50`) on new components — the page is dark
- Use `var(--neon-cyan)` for interactive/primary elements, `var(--neon-magenta)` for alerts/wins
- All glass surfaces must use `backdrop-filter: blur(...)` + a semi-transparent dark fill
- Animations are CSS-only — no JS for visual effects
- New utility classes go in `app.css`; never write inline `style` for colors or fonts that belong to the design system

## Common Commands

```bash
dotnet build SocOps/SocOps.csproj
dotnet run --project SocOps/SocOps.csproj
dotnet test
```
