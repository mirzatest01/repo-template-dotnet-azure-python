# .github
A .github repository is a special repo you create at the organization (or user) level named exactly .github. GitHub uses it as a central place to store organization-wide defaults—so you don’t have to copy the same “house rules” (templates/policies) into every repo.


# Golden Repository Template (.NET / Azure / Python)

This repository is the **official template** for creating new projects.

## What you get by default
- CI pipelines (build & test)
- Security scanning (CodeQL, dependency review)
- Standard PR template
- Structured issue intake
- AI guardrails (Copilot + coding agents)
- Org-compliant governance

## How to create a new repository
1. Click **Use this template**
2. Name your repository
3. Create the repo
4. Clone it
5. Run:
   ```bash
   ./scripts/create-labels.sh
