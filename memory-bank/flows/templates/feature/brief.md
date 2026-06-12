---
title: FT-XXX Brief Template
doc_kind: feature
doc_function: template
purpose: Governed wrapper template for the canonical `brief.md`. Read to instantiate problem-space intent, scope, and machine-checkable verification without mixing wrapper and target frontmatter.
derived_from:
  - ../../feature-flow.md
  - ../../../dna/frontmatter.md
  - ../../../engineering/testing-policy.md
status: active
audience: humans_and_agents
template_for: feature
template_target_path: ../../../features/FT-XXX/brief.md
---

# FT-XXX: Brief Template

This file describes the wrapper template. The instantiated `brief.md` lives below as an embedded contract and is copied into the feature package without the wrapper frontmatter and history.

## Wrapper Notes

Do not mix wrapper and target frontmatter. The instantiated `brief.md` starts as `status: draft` and `delivery_status: planned`.

When a feature changes APIs, schemas, CLI, security boundaries, or requires trade-off reasoning, set `Design required: yes` and create a sibling `design.md`.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: Feature Name"
doc_kind: feature
doc_function: canonical
purpose: "Canonical problem space for FT-XXX. Captures intent, scope, and verify contract without solution or execution details."
derived_from:
  - ../../product/context.md
status: draft
delivery_status: planned
audience: humans_and_agents
must_not_define:
  - ft_xxx_selected_design
  - ft_xxx_implementation_sequence
```

## Instantiated Body

```markdown
# FT-XXX: Feature Name

## What

### Problem

Describe the feature-specific problem this delivery unit solves. Reference upstream context; do not duplicate it.

### Outcome

| Metric ID | Metric | Baseline | Target | Measurement method |
| --- | --- | --- | --- | --- |
| `MET-01` | What we measure | Current value | Desired value | How we measure |

### Scope

- `REQ-01` What the system must be able to do after this feature.
- `REQ-02` ...

### Non-Scope

- `NS-01` What this feature consciously does not address.

### Constraints

- `CON-01` A constraint that limits the solution space.

### Assumptions

- `ASM-01` A working premise that has not yet been validated.

### Unresolved Blocking Decisions

- `DEC-01` A decision that blocks design or planning and must be resolved before Problem Ready.

## Design Requirement Decision

**Design required:** yes / no

**Reason:** (brief explanation — local change vs. contract/boundary change)

## Verify

### Exit Criteria

- `EC-01` What must be true for this feature to be considered done.

### Acceptance Scenarios

#### SC-01: Happy path description

**Given:** precondition  
**When:** action  
**Then:** expected outcome

#### SC-02: Edge case or error path

**Given:** precondition  
**When:** action  
**Then:** expected outcome

### Negative / Edge Test Cases

- `NEG-01` What must not happen or what behavior must remain unchanged.

### Traceability Matrix

| REQ | Covered by SC | Covered by NEG | Notes |
| --- | --- | --- | --- |
| `REQ-01` | `SC-01`, `SC-02` | `NEG-01` | |

### Checks

- `CHK-01` Automated: specific test suite or command that must be green.
- `CHK-02` Manual: specific procedure for verifying behavior that cannot be automated.

### Evidence Contract

| Evidence ID | Artifact | Producer | Path contract |
| --- | --- | --- | --- |
| `EVID-01` | Test run / screenshot / CI log | CI / reviewer | path/to/artifact or CI run link |
```
