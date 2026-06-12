---
title: "UC-XXX: Use Case Name"
doc_kind: use_case
doc_function: template
purpose: Governed wrapper template for a canonical use case. Read to instantiate a stable user or operational scenario without mixing wrapper metadata with the future use case frontmatter.
derived_from:
  - ../../../dna/governance.md
  - ../../../dna/frontmatter.md
  - ../../../product/context.md
status: active
audience: humans_and_agents
template_for: use_case
template_target_path: ../../../use-cases/UC-XXX-short-name.md
---

# UC-XXX: Use Case Name

This file describes the wrapper template. The instantiated use case lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

A use case captures a persistent project scenario. It describes trigger, preconditions, main flow, alternatives, and postconditions, but does not define implementation sequence, architecture, or feature-level verification.

## Instantiated Frontmatter

```yaml
title: "UC-XXX: Use Case Name"
doc_kind: use_case
doc_function: canonical
purpose: "Canonical use case for [scenario description]."
derived_from:
  - ../product/context.md
status: draft
audience: humans_and_agents
must_not_define:
  - implementation_sequence
  - architecture_decision
  - feature_level_test_matrix
```

## Instantiated Body

```markdown
# UC-XXX: Use Case Name

## Goal

What outcome the primary actor achieves by executing this use case.

## Primary Actor

Who initiates the scenario.

## Trigger

What event or condition starts this use case.

## Preconditions

What must be true before the use case begins.

- `PRE-01` ...

## Main Flow

1. Actor does X.
2. System responds with Y.
3. Actor confirms Z.
4. System completes the action.

## Alternate Flows / Exceptions

- `ALT-01` If condition A occurs at step 2, then ...
- `EXC-01` If system cannot complete step 4, then ...

## Postconditions

What is true after the use case completes successfully.

- `POST-01` ...

## Business Rules

References to domain rules that apply during this scenario.

- `INV-01` from `domain/rules.md`

## Traceability

| Upstream | Reference |
| --- | --- |
| PRD | `PRD-XXX` / none |
| Implemented by | `FT-XXX`, `FT-YYY` |
| Related ADR | `ADR-XXX` / none |
```
