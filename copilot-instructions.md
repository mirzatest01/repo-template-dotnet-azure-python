# Copilot Instructions (Repo-wide)

## Project context
- This repository contains: [describe briefly: API/worker/functions/data pipeline]
- Primary languages: C#/.NET and Python
- Cloud platform: Microsoft Azure
- Priorities (in order): Security > Correctness > Maintainability > Performance

## General coding standards
- Prefer small, reviewable changes. Avoid mega-PRs.
- Keep code readable; avoid cleverness.
- Do not add new dependencies unless necessary. Explain why.
- Never commit secrets, keys, tokens, or connection strings.
- Avoid logging PII/credentials. Use structured logging and safe redaction.

## .NET conventions
- Target framework: [e.g., net8.0]
- Use DI (Microsoft.Extensions.DependencyInjection) and config via appsettings + environment variables.
- Prefer async/await for I/O.
- Use nullable reference types; avoid null surprises.
- Follow existing folder structure and naming patterns.
- Validation: prefer explicit validation and clear errors.

## Python conventions
- Python version: [e.g., 3.11]
- Prefer type hints for public functions/modules.
- Keep functions small; avoid heavy classes unless needed.
- Use pathlib, logging module, and explicit exception handling.
- Follow repo linting/formatting config (black/ruff/flake8 if present).

## Testing requirements
- Any behavior change should include tests (or explain why not).
- .NET: xUnit/NUnit/MSTest (use what repo uses); keep tests deterministic.
- Python: pytest; prefer fixtures; avoid network calls in unit tests.

## Azure guidance
- Use Managed Identity where possible.
- Configuration should come from env vars / Key Vault references; no embedded secrets.
- If adding infra changes (Bicep/Terraform), keep them minimal and consistent.

## When generating code
- First, summarize the intended change and the files you plan to touch.
- Ask clarifying questions only if blocked; otherwise make reasonable assumptions and note them.
- Produce code that compiles/runs with the repo’s standard commands.
- Include commands to run locally and in CI.

## Prohibited output
- Do not output or suggest real secrets.
- Do not propose disabling security checks, tests, or code scanning to “make it work”.
