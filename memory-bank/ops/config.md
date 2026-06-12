---
title: Configuration Guide
doc_kind: ops
doc_function: canonical
purpose: Template for the configuration ownership model. Read when describing the env contract, naming conventions, and config sources for the project.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Configuration Guide

This document does not enumerate every environment variable. Its purpose is to explain where the canonical configuration schema lives and how the downstream project documents important settings.

## Configuration Architecture

Describe the actual configuration model for the project.

Examples:

- Typed config class
- `.env` + runtime env vars
- YAML/JSON/TOML files with environment overlays
- Secret manager
- Helm values / Terraform variables / deployment manifests

### File Layout

```text
config/
├── application.yml
├── environments/
├── secrets/
└── ...
```

### Ownership Rules

Record:

1. Which file or module owns the configuration schema
2. Where defaults are set
3. Where environment-specific overrides live
4. How secrets are documented without exposing values

```ruby
# Example configuration access API:
Config.database_url
Settings.feature_flags.checkout_v2
ENV.fetch("APP_PORT")
```

## Naming Convention For Env Vars

| YAML structure | Env variable |
| --- | --- |
| `database.url` | `APP_DATABASE__URL` |
| `feature_checkout_v2` | `APP_FEATURE_CHECKOUT_V2` |
| `smtp.password` | `APP_SMTP__PASSWORD` |
| `storage.bucket` | `APP_STORAGE__BUCKET` |

Rules:

- Choose one canonical prefix or explicitly document that there is no prefix.
- If nesting is used, document the separator.
- List rules for lists, booleans, and secrets.
- If the project prohibits interpolation inside config files, state this explicitly.

## Documenting Important Variables

If the project needs a reference for key variables, do not list everything — focus on significant runtime contracts.

| Variable | Description | Default | Owner |
| --- | --- | --- | --- |
| `APP_DATABASE__URL` | Primary database connection | none | platform |
| `APP_REDIS__URL` | Cache or queue | `redis://localhost:6379/0` | platform |
| `APP_PUBLIC_BASE_URL` | Base URL for link generation | `http://localhost:3000` | product/platform |
| `APP_FEATURE_X_ENABLED` | Feature flag | `false` | owning team |

## Secrets

- Never put real secret values in the repository.
- Document only the storage method, provisioning, and rotation policy.
- If part of the configuration comes from a secret manager, state this explicitly.

## Adoption Checklist

- [ ] Configuration schema owner described
- [ ] Naming convention documented
- [ ] Key runtime/env contracts listed
- [ ] Secret handling described
- [ ] References to non-existent downstream references removed
