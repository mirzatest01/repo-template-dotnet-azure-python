# Instructions for Coding Agents

## Goal
Make minimal, correct changes that pass tests and comply with security requirements.

## Quickstart (local)
### .NET
- Restore/build:
  - `dotnet restore`
  - `dotnet build -c Release`
- Test:
  - `dotnet test -c Release`

### Python
- Create venv:
  - `python -m venv .venv`
  - Activate venv (platform-specific)
- Install:
  - `pip install -r requirements.txt` (or `pip install -e .`)
- Test:
  - `pytest -q`

## Required checks before proposing a PR
- All unit tests pass (.NET + Python)
- Lint/format (if configured) is respected
- No secrets, tokens, or connection strings added
- No logging of sensitive data
- PR includes a clear summary + rollback plan if risky

## Architectural boundaries
- Do not introduce cross-layer dependencies (e.g., presentation -> data direct calls) unless existing pattern does.
- Follow existing repo structure and conventions.
- Prefer configuration via environment variables and Azure Managed Identity.

## Dependency policy
- Avoid new packages unless necessary.
- If adding a dependency:
  - Explain rationale
  - Prefer well-maintained, widely-used libraries
  - Pin versions where the repo expects it (requirements.txt / lockfiles)

## Documentation
- Update README or docs when behavior or setup changes.
- Add run/test commands for new components.

## “Stop conditions”
If any of these are true, stop and ask for guidance:
- Unclear target architecture pattern
- Conflicting conventions in repo
- Security-sensitive change (auth, crypto, secrets, RBAC)
- Production incident/hotfix context missing
