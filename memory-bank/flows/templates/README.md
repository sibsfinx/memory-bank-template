---
title: Templates Index
doc_kind: governance
doc_function: index
purpose: Navigation for reference document templates. Read to create a PRD, use case, epic, feature, ADR, prompt, or execution document without inventing a new structure.
derived_from:
  - ../../dna/governance.md
  - prd/PRD-XXX.md
  - use-case/UC-XXX.md
  - epic/README.md
  - epic/charter.md
  - epic/roadmap.md
  - epic/decision-log.md
  - epic/subissues.md
  - epic/risks.md
  - feature/README.md
  - feature/brief.md
  - feature/design.md
  - feature/implementation-plan.md
  - feature/support/runtime-surfaces.md
  - feature/support/ui-reference.md
  - feature/support/use-cases.md
  - adr/ADR-XXX.md
  - prompt/PROMPT-XXX.md
  - process/README.md
  - process/process-card.md
  - process/session-handoff.md
  - process/lifecycle-protocol.md
status: active
audience: humans_and_agents
---

# Templates Index

The `memory-bank/flows/templates/` directory holds reference document templates. All templates live as governed wrapper documents with `doc_function: template`: the wrapper has its own purpose, and the frontmatter and body of the document to be instantiated live inside the embedded template contract.

- [PRD-XXX: Product Initiative Name](prd/PRD-XXX.md) — compact Product Requirements Document for an initiative not yet decomposed into a specific feature slice.
- [UC-XXX: Use Case Name](use-case/UC-XXX.md) — canonical use case for a stable user or operational scenario.
- [Epic Templates](epic/README.md) — index of `EP-XXX` package templates.
- [EP-XXX: Charter Template](epic/charter.md) — intent, scope, source/evidence, and stakeholder channels.
- [EP-XXX: Roadmap Template](epic/roadmap.md) — waves, dependencies, gates, and stop rules.
- [EP-XXX: Decision Log Template](epic/decision-log.md) — local epic decisions that do not require a global ADR.
- [EP-XXX: Subissues Template](epic/subissues.md) — candidate/accepted delivery subissue registry.
- [EP-XXX: Risks Template](epic/risks.md) — epic-level risk register.
- [FT-XXX Feature README Template](feature/README.md) — template for the feature directory README. Answers the question: how to format a feature-level index.
- [FT-XXX: Brief Template](feature/brief.md) — canonical problem-space template for new feature packages. Answers the question: how to capture intent, scope, and verify contract without solution/execution details.
- [FT-XXX: Design Template](feature/design.md) — canonical solution-space template for a feature package. Answers the question: how to capture selected design, rationale, contracts, failure modes, and design-pack routing.
- [FT-XXX: Implementation Plan](feature/implementation-plan.md) — template for a derived execution plan. Answers the question: how to lay out sequencing and checkpoints after upstream owners are ready.
- [FT-XXX: Runtime Surfaces Template](feature/support/runtime-surfaces.md) — optional support template for current runtime inventory, semantic mapping, context matrix, and resolution tables.
- [FT-XXX: UI Reference Template](feature/support/ui-reference.md) — optional support template for interface changes, screen map, interaction states, and mockups.
- [FT-XXX: Feature Use Cases Template](feature/support/use-cases.md) — optional support template for derived use cases, test case candidates, and `FUC -> REQ -> CHK` review mapping.
- [ADR-XXX: Short Decision Name](adr/ADR-XXX.md) — ADR template. Answers the question: how to record an architectural decision.
- [PROMPT-XXX: Reusable Prompt Name](prompt/PROMPT-XXX.md) — reusable prompt document template. Answers the question: how to save the original formulation in frontmatter and the improved prompt in a copyable body block.
- [PROC-XXX: Process Documentation Index](process/README.md) — process document index template. Answers the question: how to create a routing layer for reusable process cards, session handoff, and lifecycle protocol.
- [PROC-XXX: Compact Process Card](process/process-card.md) — short reusable workflow template. Answers the question: how to capture a process with one trigger, steps, and exit criteria.
- [PROC-XXX: Session Handoff](process/session-handoff.md) — state transfer between sessions template. Answers the question: how to continue a process without losing assumptions, risks, and next checks.
- [PROC-XXX: Lifecycle Protocol](process/lifecycle-protocol.md) — full lifecycle protocol template. Answers the question: how to manage a multi-phase process with gates, verification, and rollback.
