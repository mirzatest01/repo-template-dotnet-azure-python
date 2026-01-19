# Repository Copilot Instructions

## Mission
Help implement changes safely and consistently for this repository.
Priorities: Security > Correctness > Maintainability > Performance.

## Repo context (fill in)
- Product / domain: <one-liner>
- Repo type: <API / Azure Functions / worker / data pipeline / library>
- Main languages: C#/.NET, Python
- Azure runtime: <App Service / Functions / AKS / Container Apps>
- Data stores (if any): <Azure SQL/Cosmos/Storage/...>

## How to work (behavior)
- Make small, reviewable changes. Avoid large refactors unless requested.
- Prefer editing existing patterns over introducing new patterns.
- If unclear, make reasonable assumptions and state them in the PR description.
- Never commit secrets, keys, tokens, or connection strings.
- Never log sensitive data (PII/PHI/secrets). Redact when sharing logs.

## .NET conventions
- Framework: <e.g., net8.0>
- Use async/await for I/O.
- Use dependency injection and configuration via appsettings + environment variables.
- Follow existing naming and folder structure.
- Add/adjust tests for behavior changes (use the repo’s test framework).

## Python conventions
- Version: <e.g., 3.11>
- Prefer type hints for public APIs.
- Keep functions small and explicit; handle exceptions intentionally.
- Follow repo lint/format rules (ruff/black/etc.) if present.
- Add/adjust pytest tests for behavior changes.

## Local build & test commands (fill in)
### .NET
- Build: `dotnet build -c Release`
- Test: `dotnet test -c Release`

### Python
- Install: `pip install -r requirements.txt` (or `pip install -e .`)
- Test: `pytest -q`

## Azure guidance
- Prefer Managed Identity for auth to Azure services.
- Configuration should come from env vars / Key Vault references — never hardcode.
- If you change infra (Bicep/Terraform), keep changes minimal and consistent.

## Output expectations
When you propose a solution:
- Summarize what you changed and why
- List commands to build/test
- Note any risks + rollback strategy when relevant
