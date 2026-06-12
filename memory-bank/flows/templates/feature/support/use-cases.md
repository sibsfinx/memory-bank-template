---
title: "FT-XXX: Feature Use Cases Template"
doc_kind: feature-support
doc_function: template
purpose: Governed wrapper template for optional feature-local `use-cases/README.md`. Read when a feature needs review-friendly scenarios and derived test case candidates without moving canonical acceptance out of `brief.md`.
derived_from:
  - ../../../feature-flow.md
  - ../../../../dna/frontmatter.md
status: active
audience: humans_and_agents
template_for: feature-support
template_target_path: ../../../../features/FT-XXX/use-cases/README.md
canonical_for:
  - feature_support_template_use_cases
---

# FT-XXX: Feature Use Cases Template

This file describes the wrapper template. The instantiated `use-cases/README.md` lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

Canonical acceptance stays in `brief.md` (`SC-*`, `NEG-*`, `CHK-*`, `EVID-*`). This companion document provides a review-friendly projection only.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: Feature Use Cases"
doc_kind: feature-support
doc_function: reference
purpose: "Review-friendly scenario projection for FT-XXX. Derived from `brief.md`; canonical acceptance stays there."
derived_from:
  - ../brief.md
status: draft
audience: humans_and_agents
```

## Instantiated Body

```markdown
# FT-XXX: Feature Use Cases

## Happy Path Scenarios

| FUC ID | Scenario | Primary actor | Steps summary | Maps to |
| --- | --- | --- | --- | --- |
| `FUC-01` | Main scenario name | User role | Brief description | `SC-01`, `REQ-01` |

## Edge Cases

| FUC ID | Scenario | Trigger | Expected behavior | Maps to |
| --- | --- | --- | --- | --- |
| `FUC-02` | Edge scenario | What causes it | What should happen | `NEG-01` |

## Error Cases

| FUC ID | Scenario | Error trigger | Expected response | Maps to |
| --- | --- | --- | --- | --- |
| `FUC-03` | Error scenario | Error condition | Error message or fallback | `SC-02` |

## Derived Test Case Candidates

| TC ID | Scenario | Type | Priority | Maps to |
| --- | --- | --- | --- | --- |
| `TC-01` | Test description | unit / integration / e2e | high / medium / low | `SC-01`, `CHK-01` |

## Traceability Matrix

| FUC | REQ | SC / NEG | CHK |
| --- | --- | --- | --- |
| `FUC-01` | `REQ-01` | `SC-01` | `CHK-01` |

## Test Ownership

Canonical test cases are defined in `brief.md`. This document contains derived candidates only — they inform planning but do not replace `SC-*` or `CHK-*`.
```
