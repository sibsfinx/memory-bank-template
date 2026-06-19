---
title: Epics Index
doc_kind: epic
doc_function: index
purpose: "Navigation for instantiated epic packages. Read when an initiative is larger than one feature and must be executed through a roadmap and a set of related subissues."
derived_from:
  - ../dna/governance.md
  - ../flows/epic-flow.md
  - ../flows/feature-flow.md
status: active
audience: humans_and_agents
---

# Epics Index

The `memory-bank/epics/` directory holds instantiated epic packages of the form `EP-XXX/`.

## Rules

- An epic describes a large project change that cannot be safely delivered as a single feature.
- An epic owns intent, roadmap, decomposition, decision log, risks, and the subissue registry.
- An epic does not own code-level execution: implementation proceeds through separate `memory-bank/features/FT-<issue>/` packages.
- Every delivery subissue must reference the relevant epic artifacts and project-level `UC-*` if it changes a stable scenario.
- Rules for creating and maintaining epic packages live in [`../flows/epic-flow.md`](../flows/epic-flow.md).

## Naming

- Base format: `EP-XXX/`
- Replace `XXX` with a stable initiative identifier: issue id, project id, or another durable name.
- One epic = one large program or initiative with multiple delivery slices.

## Package Layers

| Layer | Files | Purpose |
| --- | --- | --- |
| Intent | `charter.md`, source refs, stakeholder channels | Why the epic exists, what is in/out of scope, which facts are already confirmed |
| Governance | `roadmap.md`, `decision-log.md`, `risks.md`, `subissues.md` | How to execute the epic, which decisions have been made, which risks and subissues are managed |
| Knowledge | `design.md`, `specs/**`, `diagrams/**`, linked `UC-*` | Normalized requirements, bounded contexts, scenarios, contracts, and audit trail |
| Execution Handoff | future `memory-bank/features/FT-<issue>/` | Concrete code changes, tests, rollout/backout for one approved delivery issue |

Knowledge files are optional. If they are created as Markdown inside an epic package they must be indexed from the package `README.md` or owner document and must follow the frontmatter rules from [`../flows/epic-flow.md`](../flows/epic-flow.md).

## Instantiated Epics

In the template repository this directory may be empty. That is normal.
