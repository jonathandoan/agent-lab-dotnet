# GitHub Copilot instructions (condensed)

## Mandatory development checklist (run before commit/PR)
- Lint: `dotnet format --verify-no-changes` (install `dotnet tool install -g dotnet-format` if needed)
- Build: `dotnet build SocOps/SocOps.csproj`
- Test: `dotnet test`

## Quick start
- Install .NET 10 SDK and verify: `dotnet --version`
- Build & run: `dotnet run --project SocOps/SocOps.csproj`
- App: http://localhost:5166

## Layout (short)
- `SocOps/`: Blazor app (Components, Services, Models, wwwroot)
- `workshop/`: agent examples and exercises
- `.github/agents/`: custom agent definitions

## Conventions & agents
- Use VS Code task `dotnet: run` for development.
- Keep component CSS scoped in `.razor.css` files.
- Agent definitions live in `.github/agents/` — follow their frontmatter for subagent/playwright instructions.

## Design note
- Prefer CSS variables in `wwwroot/css/app.css` for theme tokens; add colors/typography to this file when updating UI.

## Quick prompts
- "Run build and tests, report failures." — automation
- "Review `StartScreen.razor` for accessibility issues." — UI review

