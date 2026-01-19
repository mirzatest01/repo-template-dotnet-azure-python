# Agent Instructions — Infra

## Scope
Applies only to `infra/` and pipeline files.

## Infra rules
- Prefer least-privilege RBAC.
- Prefer Managed Identity; avoid secrets.
- Any change to networking (VNet/Private Endpoint/DNS) must be explicitly called out.
- Keep IaC changes minimal; avoid unrelated refactors.

## Validation
- If Terraform: run `terraform fmt` and `terraform validate` (if repo supports it)
- If Bicep: run `az bicep build` (if repo supports it)

## Safety
- Never output credentials or secret values in logs.
- Treat prod changes as high risk; ensure rollback plan is documented.
