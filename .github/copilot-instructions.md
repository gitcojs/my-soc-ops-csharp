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

## Common Commands

```bash
dotnet build SocOps/SocOps.csproj
dotnet run --project SocOps/SocOps.csproj
dotnet test
```
