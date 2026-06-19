---
title: Release And Deployment
doc_kind: ops
doc_function: canonical
purpose: Template for the release process. Read when adapting versioning, changelog, deployment, and release verification to the project.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Release And Deployment

## Release Flow

Describe the actual sequence of steps for this project.

Example:

1. Bump version in `VERSION` / `package.json` / `pyproject.toml`
2. Update `CHANGELOG.md`
3. Create release branch: `release/vX.Y.Z`
4. Run release test plan (see below)
5. Merge to `main`
6. Tag: `git tag vX.Y.Z`
7. Deploy to production: `make deploy ENV=production`

## Release Commands

```bash
# Example commands:
make release VERSION=1.2.3
make deploy ENV=staging
make deploy ENV=production REQUIRES_APPROVAL=true
```

Document:

- Which environment variables are required
- Which steps require explicit approval
- Where the boundary between automated and manual steps lies

## Release Test Plan

Format: `release-v{VERSION}-test-plan.md`

Minimum structure:

- Date
- Version comparison (old → new)
- Environment
- Change overview table
- Change verification checklist
- Smoke test items:
  - [ ] Application starts
  - [ ] Health endpoint responds
  - [ ] Core user flow works
  - [ ] No new errors in error tracker

## Rollback

Document:

- The rollback unit (a deploy? a migration? a feature flag?)
- The fastest safe rollback path
- Who has authority to approve a production rollback
- Irreversible data or migration impacts
