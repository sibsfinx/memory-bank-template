---
title: FT-XXX Feature Template - Implementation Plan
doc_kind: feature
doc_function: template
purpose: Governed wrapper template for the implementation plan. Records how to instantiate the execution document without redefining canonical problem or solution facts and without mixing the wrapper with the target `implementation-plan.md`.
derived_from:
  - ../../feature-flow.md
  - ../../../dna/frontmatter.md
  - ../../../engineering/testing-policy.md
status: active
audience: humans_and_agents
template_for: feature
template_target_path: ../../../features/FT-XXX/implementation-plan.md
---

# Implementation Plan Template

This file describes the wrapper template. The instantiated `implementation-plan.md` lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

Requirements, blocker state, and acceptance criteria are defined in the sibling `brief.md`. If `brief.md` records `Design required: yes`, the selected design, accepted local decisions, and solution-level contracts are defined in the sibling `design.md` or an ADR. This document defines only the sequencing of work and execution checkpoints.

Create this document only after upstream owners are ready: sibling `brief.md` has `status: active` and, if required, sibling `design.md` has been moved to `status: active`. While the plan is still being formed, `implementation-plan.md` itself may remain in `status: draft`; before the feature transitions to `delivery_status: in_progress` the plan must reach `status: active`.

When a feature transitions to `delivery_status: done` or `delivery_status: cancelled`, `implementation-plan.md` is archived if it is no longer used as a working execution document.

The document must be executable without additional interpretation. If a step cannot be linked to canonical IDs, existing solution refs, an artifact, a check, or an explicit manual procedure, the step is insufficiently described.

The plan must be grounded in the current state of the repository: first record relevant modules, local patterns, open questions, and the execution environment, then lay out the sequencing of changes.

The plan must explicitly record which automated tests will be added or updated for the change surface, which suites must be green locally and in CI, and which gaps remain temporarily manual-only with justification and approval ref.

Use stable identifiers from the taxonomy in [../../feature-flow.md#stable-identifiers](../../feature-flow.md#stable-identifiers) for references within the plan.

If an unknown changes scope, acceptance criteria, or the evidence contract, it is first escalated upstream to sibling `brief.md`. If an unknown changes the selected design, C4 architecture model, accepted local decisions, contracts, or rollout/backout semantics, it is first escalated to the required sibling `design.md` or ADR and only then reflected in the plan.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: Implementation Plan"
doc_kind: feature
doc_function: derived
purpose: "Execution plan for FT-XXX. Records discovery context, steps, risks, and test strategy without redefining canonical problem and solution facts."
derived_from:
  - brief.md
  # Required only when brief.md says "Design required: yes":
  # - design.md
  # Optional support refs:
  # - runtime-surfaces.md
  # - ui-reference/README.md
  # - use-cases/README.md
status: draft
audience: humans_and_agents
must_not_define:
  - ft_xxx_scope
  - ft_xxx_selected_design
  - ft_xxx_acceptance_criteria
  - ft_xxx_blocker_state
```

## Instantiated Body

```markdown
# Implementation Plan

## Goal Of This Plan

What delivery outcome this plan must achieve given `brief.md` and, if present, the already accepted solution.

## Grounding / Support References

Which upstream canonical and support docs are used as the execution baseline. Support docs do not redefine canonical facts: if a conflict is found, update the owner document before continuing.

| Document | Role in this plan | Facts reused | Conflict action |
| --- | --- | --- | --- |
| `brief.md` | Canonical problem / verify owner | `REQ-*`, `SC-*`, `CHK-*`, `EVID-*` | Update `brief.md` first |
| `design.md` / `none` | Conditional solution owner | `SOL-*`, `C4-*`, `SD-*`, `CTR-*`, `INV-*`, `FM-*`, `RB-*` | Update `design.md` or ADR first; if design is absent, promote new design facts before planning |
| `runtime-surfaces.md` / `none` | Optional grounding | `SURF-*`, `MAP-*`, context matrix | Promote changed design facts to `design.md` if design is required |
| `ui-reference/README.md` / `none` | Optional interface reference | `UI-*`, mockups, states | Promote changed requirements to `brief.md` or design facts to `design.md` if required |
| `use-cases/README.md` / `none` | Optional scenario companion | `FUC-*`, `TC-*` candidates | Keep canonical acceptance in `brief.md` |

## Current State / Reference Points

Which existing files, modules, commands, or documents the agent must study before making changes. This section records grounding in the current repository state and local patterns that must not be ignored.

| Path / module | Current role | Why relevant | Reuse / mirror |
| --- | --- | --- | --- |
| `path/to/module` | What this artifact already does | Why it cannot be ignored during planning | Which pattern, helper, command, or contract must be followed |

## Test Strategy

Which test surfaces must be updated as implementation proceeds. This section records expected automated coverage, required local/CI gates, and manual-only exceptions for the change surface, without redefining canonical test cases from `brief.md`.

| Test surface | Canonical refs | Existing coverage | Planned automated coverage | Required local suites / commands | Required CI suites / jobs | Manual-only gap / justification | Manual-only approval ref |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `path/or/behavior` | `REQ-01`, `SC-01`, `NEG-01`, `CHK-01`, `SOL-01 if design exists` | What is covered now | Which suite, test type, or deterministic check must be added or updated | Which commands or suites must be green locally | Which jobs or suites must be green in CI | What remains manual-only and why | `AG-01` / review link / `none` |

## Open Questions / Ambiguities

Unknowns that have not been resolved after discovery. If a question changes upstream semantics, it must not be silently resolved inside an execution step.

| Open Question ID | Question | Why unresolved | Blocks | Default action / escalation owner |
| --- | --- | --- | --- | --- |
| `OQ-01` | What exactly is unknown | Why this has not been proven yet | `STEP-02` / `WS-1` / whole plan | Default action and who decides on escalation |

## Environment Contract

Which execution environment is considered valid for the plan: setup, test commands, env vars, permissions, mocks, external dependencies, and other operational assumptions.

| Area | Contract | Used by | Failure symptom |
| --- | --- | --- | --- |
| setup | What environment preparation is required | `STEP-01`, `STEP-02` | Symptom indicating invalid environment |
| test | Which command or procedure is the reference for verification at this stage | `CHK-01` | What counts as an untrustworthy verify |
| access / network / secrets | What access, domains, keys, or sandbox assumptions are needed | `STEP-03` | When to stop and escalate |

## Preconditions

What must be ready before work begins: data, access, ADRs, environment, agreements. Each row references a canonical ref and does not paraphrase its meaning.

| Precondition ID | Canonical ref | Required state | Used by steps | Blocks start |
| --- | --- | --- | --- | --- |
| `PRE-01` | `CON-01` / `DEC-01` / `SD-01 if design exists` / ADR path / design-not-required decision | What upstream state is required to start | `STEP-01`, `STEP-02` | yes / no |

## Workstreams

Break work into independent streams with an explicit result for each.

| Workstream | Implements | Result | Owner | Dependencies |
| --- | --- | --- | --- | --- |
| `WS-1` | `REQ-01`, `SOL-01 if design exists`, `CTR-01 if design exists` | What must appear | human / agent / either | What blocks start or completion |

## Approval Gates

Which actions must not be executed without explicit human confirmation. Use this section for risky, irreversible, expensive, or externally-effective operations.

| Approval Gate ID | Trigger | Applies to | Why approval is required | Approver / evidence |
| --- | --- | --- | --- | --- |
| `AG-01` | Which step or symptom requests approval | `STEP-03` / `WS-2` | Why autonomous continuation is not allowed | Who confirms and how it is recorded |

## Work Sequence

Describe execution as atomic steps. Each step must be small enough to be verified and, if needed, rolled back or stopped without the change surface spreading.

| Step ID | Actor | Implements | Goal | Touchpoints | Artifact | Verifies | Evidence IDs | Check command / procedure | Blocked by | Needs approval | Escalate if |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `STEP-01` | human / agent / either | `REQ-01`, `SOL-01 if design exists`, `CTR-01 if design exists` | What we do at this step | Which files, services, or data we touch | What must appear after the step | `CHK-01` | `EVID-01` | How we confirm completion | `PRE-01`, `OQ-01` | `AG-01` / `none` | When autonomous continuation is not possible |

## Parallelizable Work

Which steps or workstreams can be executed in parallel without write-surface conflict.

- `PAR-01` What can proceed in parallel.
- `PAR-02` What cannot be parallelized due to shared write surface.

## Checkpoints

Which intermediate points must be passed before rollout or handoff.

| Checkpoint ID | Refs | Condition | Evidence IDs |
| --- | --- | --- | --- |
| `CP-01` | `STEP-01`, `CHK-01`, `SOL-01 if design exists` | Which intermediate state must be proven | `EVID-01` |

## Execution Risks

Which practical risks may derail timelines or require rebuilding the plan.

| Risk ID | Risk | Impact | Mitigation | Trigger |
| --- | --- | --- | --- | --- |
| `ER-01` | What might go wrong | What it breaks | What we do proactively | Which signal activates mitigation |

## Stop Conditions / Fallback

When the plan must stop or revert to a safe state.

| Stop ID | Related refs | Trigger | Immediate action | Safe fallback state |
| --- | --- | --- | --- | --- |
| `STOP-01` | `DEC-01`, `RJ-01`, `SD-01 if design exists` | Which symptom causes a stop | What to do immediately | Which state to revert to or freeze at |

## Plan-local Evidence

Which evidence artifacts belong to the execution plan itself and are not the canonical evidence contract from `brief.md`.

| Evidence ID | Artifact | Producer | Path contract | Reused by checkpoints |
| --- | --- | --- | --- | --- |
| `EVID-09` | e.g. simplify-review verdict, discovery note, or manual approval note | implementer / reviewer / human approver | Where it lives or how it is recorded | `CP-01` |

## Ready For Acceptance

Which conditions must be met to consider the plan exhausted and transition to final acceptance via the `Verify` section in sibling `brief.md`.

- All workstreams are completed or explicitly stopped via `STOP-*`.
- All checkpoints have evidence.
- Required local suites are green and CI does not contradict local verify.
- Manual-only gaps are closed via approved `AG-*` or remain blockers for `delivery_status: done`.
- Support docs, if present, do not diverge from canonical `brief.md`, existing `design.md`, ADRs, and this plan.
- Final acceptance follows `brief.md` `Verify`, not this checklist.
```
