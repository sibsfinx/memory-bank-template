---
title: "PRD-XXX: Product Initiative Name"
doc_kind: prd
doc_function: template
purpose: Governed wrapper template for a Product Requirements Document. Read to instantiate a lean PRD for an initiative not yet decomposed into specific feature slices.
derived_from:
  - ../../../dna/governance.md
  - ../../../dna/frontmatter.md
  - ../../../product/context.md
status: active
audience: humans_and_agents
template_for: prd
template_target_path: ../../../prd/PRD-XXX-short-name.md
---

# PRD-XXX: Product Initiative Name

This file describes the wrapper template. The instantiated PRD lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

A PRD is needed when the task lives at the level of a product initiative or capability, not a single vertical slice. Usually a PRD sits between the general context in `product/context.md` and downstream feature packages in `features/README.md`.

A PRD must NOT define implementation sequences, architecture decisions, or feature-level verification contracts.

## Instantiated Frontmatter

```yaml
title: "PRD-XXX: Product Initiative Name"
doc_kind: prd
doc_function: canonical
purpose: "Describes the product initiative, its target users, goals, scope, and success metrics."
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
# PRD-XXX: Product Initiative Name

## Problem

Describe the product problem in user/business language, not in terms of solutions. Reference upstream context from `product/context.md` rather than duplicating it.

## Users And Jobs

| Segment ID | Segment | Job To Be Done | Current Pain |
| --- | --- | --- | --- |
| `SEG-01` | Who they are | What they are trying to accomplish | What is blocking them |

## Goals

- `GOAL-01` What this initiative must achieve (mandatory).
- `GOAL-02` What else it should achieve (important but not blocking).

## Non-Goals

- `NG-01` What this initiative consciously does not address.

## Product Scope

Capabilities this initiative introduces or changes. Think at capability level, not change-set level.

- `CAP-01` What the system will be able to do after this initiative.

## UX And Business Rules

Product constraints that downstream features must respect.

- `BR-01` A rule or constraint that shapes the user experience or business process.

## Success Metrics

| Metric ID | Metric | Baseline | Target | Measurement method |
| --- | --- | --- | --- | --- |
| `MET-01` | What we measure | Current value | Desired value | How we measure |

## Risks And Open Questions

- `RISK-01` What might prevent this initiative from succeeding.
- `OQ-01` What needs to be answered before detailed design begins.

## Downstream Features

| Feature ID | Title | Status |
| --- | --- | --- |
| `FT-XXX` | Short feature name | planned |
```
