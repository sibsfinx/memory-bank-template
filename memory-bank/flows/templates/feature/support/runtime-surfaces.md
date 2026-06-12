---
title: "FT-XXX: Runtime Surfaces Template"
doc_kind: feature-support
doc_function: template
purpose: Governed wrapper template for optional `runtime-surfaces.md`. Read when a feature requires clarity on current entrypoints, concrete surfaces, semantic mappings, context variants, and fallback/error paths.
derived_from:
  - ../../../feature-flow.md
  - ../../../../dna/frontmatter.md
status: active
audience: humans_and_agents
template_for: feature-support
template_target_path: ../../../../features/FT-XXX/runtime-surfaces.md
canonical_for:
  - feature_support_template_runtime_surfaces
---

# FT-XXX: Runtime Surfaces Template

This file describes the wrapper template. The instantiated `runtime-surfaces.md` lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

`runtime-surfaces.md` must NOT define:

- Feature scope (belongs to `brief.md`)
- Selected design decisions (belongs to `design.md`)
- Acceptance criteria (belongs to `brief.md`)
- Implementation sequence (belongs to `implementation-plan.md`)

If this document reveals a changed design fact, update the canonical owner first.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: Runtime Surfaces"
doc_kind: feature-support
doc_function: reference
purpose: "Current runtime surface inventory for FT-XXX: entrypoints, semantic mappings, context matrix, and resolution tables."
derived_from:
  - brief.md
  # - design.md  # add if design.md exists
status: draft
audience: humans_and_agents
```

## Instantiated Body

```markdown
# FT-XXX: Runtime Surfaces

## Current Surface Inventory

| Surface ID | Surface | Trigger | Concrete route/handler | Guaranteed context |
| --- | --- | --- | --- | --- |
| `SURF-01` | Name of the surface | What triggers it | File path or handler name | What data is always available |

## Adjacent Out-of-Scope Surfaces

| Surface | Why out of scope |
| --- | --- |
| `adjacent-surface` | Reason it is excluded from this feature |

## Semantic Mapping

| Map ID | Business unit | Reachable via surfaces | Notes |
| --- | --- | --- | --- |
| `MAP-01` | What business concept | `SURF-01`, `SURF-02` | Semantic notes |

## Target Mapping Reference

Post-change ownership and responsibility.

| Surface ID | New owner / handler | Change summary |
| --- | --- | --- |
| `SURF-01` | New handler path | What changes |

## Context Matrix

| Context item | Always available | Optional | Must never assume |
| --- | --- | --- | --- |
| User ID | yes | — | — |
| Tenant context | — | yes | — |
| Request origin | — | — | yes |

## Resolution / Decision Table

| Condition | Decision | Outcome | Observability hook |
| --- | --- | --- | --- |
| Condition at runtime | What the system decides | Result | Log / metric / trace |
```
