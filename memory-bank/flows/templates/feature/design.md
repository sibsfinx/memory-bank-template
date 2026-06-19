---
title: FT-XXX Design Template
doc_kind: feature
doc_function: template
purpose: Governed wrapper template for the canonical `design.md`. Read to instantiate the solution-space document without mixing wrapper metadata with the target design document frontmatter.
derived_from:
  - ../../feature-flow.md
  - ../../../dna/frontmatter.md
status: active
audience: humans_and_agents
template_for: feature
template_target_path: ../../../features/FT-XXX/design.md
---

# FT-XXX: Design Template

This file describes the wrapper template. The instantiated `design.md` lives below as an embedded contract and is copied into the feature package without the wrapper frontmatter and history.

## Wrapper Notes

`design.md` owns solution space only. It does not redefine business requirements, scope, acceptance criteria, or execution sequencing — those belong to sibling `brief.md` and `implementation-plan.md`.

Create `design.md` only after `brief.md` records `Design required: yes` and has `status: active`.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: Design"
doc_kind: feature
doc_function: canonical
purpose: "Solution space for FT-XXX. Captures selected design, rationale, contracts, failure modes, and design-pack routing."
derived_from:
  - brief.md
status: draft
audience: humans_and_agents
must_not_define:
  - ft_xxx_scope
  - ft_xxx_acceptance_criteria
  - ft_xxx_implementation_sequence
```

## Instantiated Body

```markdown
# FT-XXX: Design

## Design Pack

List all design artifacts for this feature and their canonical owners.

| Artifact | Owner | Location |
| --- | --- | --- |
| This document | Solution space | `design.md` |
| C4 diagram | Architecture boundary | `design.md#c4-applicability` |
| ADR reference | Architecture decision | `../../../adr/ADR-XXX.md` |

## C4 Applicability Decision

**C4 required:** yes / no (record as `C4-00: not required` with reason if no)

**Minimum level required:** C1 / C2 / C3 / C4

**Reason:** (what boundary is changing or why C4 is not needed)

### C4 Diagram

```
(Insert Mermaid, PlantUML, Structurizr DSL, image, or markdown table here)
```

**C4-01:** System Context — [describe what changes]

## Selected Design

- `SOL-01` The chosen approach and why it was selected.
- `SOL-02` Key structural decision.

## Considered Alternatives

| Alt ID | Option | Pros | Cons | Reason not chosen |
| --- | --- | --- | --- | --- |
| `ALT-01` | Alternative approach | What it offers | Its limitations | Why we chose differently |

## Trade-offs

- `TRD-01` Trade-off explicitly accepted with this design.

## Accepted Feature-local Decisions

- `SD-01` A local decision accepted for this feature (not requiring a global ADR).

## Contracts

- `CTR-01` API, event, schema, or integration contract introduced or changed.

## Invariants

- `INV-01` A system invariant that the solution must preserve.

## Failure Modes

- `FM-01` What can go wrong and how we handle it.

## Rollout / Backout

- `RB-01` Rollout stage: how we deploy safely.
- `RB-02` Backout stage: how we revert if needed.

## Traceability

| Requirement | Design element | ADR / decision |
| --- | --- | --- |
| `REQ-01` from `brief.md` | `SOL-01`, `CTR-01` | `SD-01` |
```
