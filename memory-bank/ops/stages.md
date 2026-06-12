---
title: Stages And Non-Local Environments
doc_kind: ops
doc_function: canonical
purpose: Template for documenting access to production-like environments. Read when adapting access rights, smoke checks, logs, and runtime operations to the project.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Stages And Non-Local Environments

Describe here not only production but also stage, beta, preview, sandbox, or other non-local environments if they exist.

## Environment Inventory

| Environment | Purpose | Access path | Notes |
| --- | --- | --- | --- |
| `production` | Real users and live traffic | Command, jump host, or UI | Strictest restrictions |
| `staging` | Pre-release verification | Command, URL, or namespace | May be used for smoke checks |
| `sandbox` | Integration testing and unsafe experiments | Optional | If it exists |

## Common Operations

List only actually permitted operations and their canonical entrypoints.

```bash
# Examples:
make console ENV=staging
make logs ENV=production
kubectl -n staging logs deploy/app
ssh <bastion>
psql "$DATABASE_URL"
```

For each operation record:

- who has the right to run it;
- what approval gates are required;
- where the boundary between read-only and mutating access lies.

## Credentials And Access

Describe:

- where secrets are stored;
- how access rights are granted;
- which env vars or secret stores are used;
- what constitutes an unacceptable bypass of the access procedure.

Never store real production credentials in the template.

## Version And Health Checks

Document safe ways to check:

- the currently deployed version;
- the health endpoint;
- the smoke URL;
- basic operational dashboards.

Example:

```bash
curl -fsS https://<stage-host>/health
kubectl -n <namespace> get deploy <app>
```

## Logs And Observability

Describe canonical paths to:

- application logs;
- metrics;
- traces;
- error tracker;
- dashboards for main services.

## Test Data And Smoke Targets

If the project uses staging/demo tenants, seed users, or test accounts, list them here together with usage rules.

## Adoption Checklist

- [ ] All non-local environments listed
- [ ] Canonical access paths specified
- [ ] Safe health/version checks described
- [ ] Observability entrypoints listed
- [ ] Fake or irrelevant examples removed
