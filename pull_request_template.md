## Summary
- What does this PR change? Why?

## Type of change
- [ ] Bug fix
- [ ] Feature
- [ ] Refactor / tech debt
- [ ] Security hardening
- [ ] CI/CD / infrastructure
- [ ] Documentation

## Related work
- Issue/Work Item: #
- ADR (if applicable): #

## How to test
### .NET
- [ ] `dotnet restore`
- [ ] `dotnet build -c Release`
- [ ] `dotnet test -c Release`

### Python
- [ ] `python -m venv .venv` (if needed)
- [ ] `pip install -r requirements.txt` (or `pip install -e .`)
- [ ] `pytest -q`

## Evidence
- Logs/output (redact secrets):
- Screenshots (if UI):
- Performance impact (if relevant):

## Azure impact (if applicable)
- [ ] App Service / Functions changes
- [ ] Key Vault / secrets (no secrets committed)
- [ ] Storage / Cosmos / SQL changes
- [ ] IAM/RBAC changes
- [ ] Network changes (VNet/Private Endpoints)
- [ ] Terraform/Bicep/ARM changes

## Risk & rollback
- Risk level: [Low/Med/High]
- Rollback plan:
- Feature flag / safe rollout: [Yes/No]

## Security & compliance
- [ ] No secrets/keys/connection strings committed
- [ ] Sensitive logging avoided (PII/PHI)
- [ ] Dependency changes reviewed (nuget/pip)
- [ ] Threat model / security review needed (high-risk only)

## AI usage (required)
- [ ] AI-assisted code (Copilot/agent) was reviewed and understood by the author
- [ ] Generated code was adapted to project conventions and includes tests where needed
