# GitHub Standards Governance

## Purpose
This repository defines **organization-wide GitHub standards** and templates.
Its goal is to ensure consistent engineering quality, security, and AI-safe
development practices across all repositories.

Unless explicitly overridden at the repository level, the standards defined
here apply to all repositories in the organization.

---

## Scope
This governance applies to:
- Community health files (Code of Conduct, Contributing, Security, Support)
- Issue forms and intake standards
- Pull request templates
- Workflow templates (CI, security scanning, deployments, releases)
- AI agent instructions (Copilot instructions, AGENTS.md)
- Labeling and routing conventions

---

## Ownership & Accountability

### Primary Owners
- **Platform Engineering** – overall ownership, CI/CD, templates, automation
- **Security Engineering** – security policies, scanning, AI guardrails

### Review Enforcement
- All changes to this repository **must be made via Pull Request**
- CODEOWNERS reviews are mandatory
- Security must review changes that affect:
  - SECURITY.md
  - workflow templates
  - AI instructions
  - authentication, permissions, or scanning

---

## Versioning Model

### Versioning Rules
We use **semantic-style versioning** for standards:

- **MAJOR** – Breaking or mandatory behavior change  
  (e.g., new required CI gate, new mandatory PR checklist item)
- **MINOR** – Backward-compatible additions  
  (e.g., new workflow template, new issue form)
- **PATCH** – Clarifications or non-functional changes  
  (e.g., wording, formatting, comments)

### Version Tracking
- Current versions are recorded in `POLICY_VERSION.md`
- All changes are documented in `CHANGELOG.md`

---

## Change Classification & Control

### Change Classes

#### Class 1 – Patch
- Typos, wording improvements
- Clarifications with no behavioral impact  
**Approval:** Platform Engineering

#### Class 2 – Minor
- New templates (issue forms, workflows)
- Optional improvements  
**Approval:** Platform Engineering  
**Security review:** If security-related

#### Class 3 – Major
- New mandatory requirements
- Changes that affect CI, security posture, or AI behavior  
**Approval:** Platform Engineering + Security  
**Additional steps:**
- Change announcement required
- Adoption window (2–4 weeks recommended)

---

## Quarterly Review Cadence

### Frequency
- **Quarterly:** Full standards review
- **Monthly:** Lightweight health check (templates still valid)
- **Ad hoc:** After major incidents or security findings

### Quarterly Review Checklist
Each quarter, owners must review:

- Community health files (still accurate?)
- Issue templates (still useful, not bloated?)
- PR template (matches SSDLC expectations?)
- Workflow templates (actions versions current?)
- AI instructions (Copilot + AGENTS still aligned with stack?)
- Labels and routing (still consistent?)

### Outputs
- Update `CHANGELOG.md`
- Update `POLICY_VERSION.md` if needed
- Publish a short internal announcement

---

## AI Governance (Critical)

### AI Usage Principles
- AI tools are **assistive**, not authoritative
- Humans remain accountable for:
  - correctness
  - security
  - compliance
- AI-generated code must meet the same quality bar as human-written code

### Instruction Hierarchy
1. Organization-level Copilot settings (global rules)
2. Repo-level `.github/copilot-instructions.md`
3. Root `AGENTS.md`
4. Nested `AGENTS.md` (folder-specific rules)

More specific instructions override general ones.

---

## Exceptions & Overrides

### When Overrides Are Allowed
Repositories may override org defaults if:
- Regulatory or contractual requirements demand it
- Legacy systems cannot comply immediately
- Specialized workloads require different tooling

### How to Request an Exception
- Open an issue in this repository
- Use label: `governance-exception`
- Provide:
  - Reason for exception
  - Scope (which repo, which rule)
  - Duration (temporary or permanent)

All exceptions must be reviewed by Platform Engineering.
Security must review security-related exceptions.

---

## Adoption Expectations

### New Repositories
- Must be created from the official **Golden Repo Template**
- Must retain:
  - PR template
  - CI workflows
  - AI instructions
  - CODEOWNERS

### Existing Repositories
- Strongly encouraged to align
- High-risk repos may be prioritized for adoption
- Automated adoption may be introduced later

---

## Communication

### Change Announcements
Major or visible changes will be communicated via:
- Engineering channel (Slack/Teams)
- Email or internal portal (if applicable)

Announcements will include:
- What changed
- Why it matters
- When it takes effect
- Any required action

---

## Final Note
This repository is not static documentation.

It is a **living control plane** for:
- engineering quality
- security posture
- AI-assisted development

Treat changes here with the same rigor as production systems.
