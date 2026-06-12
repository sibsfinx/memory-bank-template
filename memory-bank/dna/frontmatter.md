---
doc_kind: governance
doc_function: canonical
purpose: Schema of required and conditional YAML frontmatter fields.
derived_from:
  - governance.md
status: active
---

# Frontmatter Schema

## Required

| Field | Type | Description |
|---|---|---|
| `status` | enum | `draft` / `active` / `archived` |

## Conditionally Required

| Field | When | Description |
|---|---|---|
| `derived_from` | Upstream document exists | Direct upstream dependencies. Each element is a string (path) or an object `{path, fit}` where `fit` explains the scope of the dependency |
| `delivery_status` | Lifecycle-owning canonical `brief.md` | `planned` / `in_progress` / `done` / `cancelled` |
| `decision_status` | ADR documents | `proposed` / `accepted` / `superseded` / `rejected` |

## Additional Fields

Governed documents may contain additional fields not described in this schema. Additional fields do not need to be registered here and are interpreted at the level of a specific `doc_kind` or flow.

For `doc_kind: feature`, the lifecycle owner remains the canonical `brief.md` of the problem-space document. Feature-level `README.md`, conditional `design.md`, and `implementation-plan.md` use the same `doc_kind` but are not required to have `delivery_status` if they do not own the delivery lifecycle.

For `doc_kind: feature-support`, the document is a reference or companion inside a feature package and does not own `delivery_status`, canonical requirements, the selected solution, or execution sequencing.

## Examples

```yaml
---
derived_from:
  - ../../product/context.md
status: active
delivery_status: planned
---
```

```yaml
---
derived_from:
  - ../brief.md
  - path: ../../../adr/ADR-001-model-stack.md
    fit: "only the selected models and VRAM constraints are used"
status: active
---
```
