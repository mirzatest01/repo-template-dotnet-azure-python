# AGENTS.md — Instructions for Coding Agents

## Goal
Make minimal, correct changes that pass CI and align with security/compliance.

## Golden rules
- Do not commit secrets, keys, tokens, or credentials.
- Do not weaken security checks, disable scanning, or bypass reviews.
- Keep changes small; split into multiple PRs if needed.
- Prefer existing patterns and libraries already in the repo.
- If a change touches auth/RBAC/crypto/data access, flag it as **security-sensitive**.

## Setup & test (required before marking ready)
### .NET
- `dotnet restore`
- `dotnet build -c Release`
- `dotnet test -c Release`

### Python
- `python -m venv .venv`
- `pip install -r requirements.txt` (or `pip install -e .`)
- `pytest -q`

## Definition of Done (DoD)
- Tests added/updated for behavior changes (or explain why not)
- No secrets or sensitive logs
- PR includes: What/Why, testing evidence, risk, rollback (if applicable)
- Docs/runbooks updated if behavior/setup changes

## Repo boundaries (fill in)
- Allowed: <list main modules/services>
- Avoid: <forbidden patterns, e.g., direct DB calls from controllers, cross-layer refs>

## Stop conditions (ask for guidance)
Stop and ask if:
- The architecture/conventions are unclear or conflicting
- The change is security-sensitive (auth/RBAC/crypto/PII)
- CI requires external secrets/tools you can’t access
- The repo lacks a clear build/test path
