---
title: Use Cases Index
doc_kind: use_case
doc_function: index
purpose: Navigation for instantiated project use cases. Read to find a canonical product scenario or to register a new one.
derived_from:
  - ../dna/governance.md
  - ../flows/templates/use-case/UC-XXX.md
status: active
audience: humans_and_agents
---

# Use Cases Index

The `memory-bank/use-cases/` directory holds canonical user and operational scenarios for the project.

A use case is needed for a scenario that lives at the product level, recurs over time, and can be upstream for multiple feature packages. It is not a replacement for `SC-*` inside `brief.md`: `SC-*` describes acceptance scenarios for a delivery unit, while `UC-*` describes stable system behavior at the project level.

A use case normally inherits the shared product context from [`../product/context.md`](../product/context.md). If the scenario depends on domain rules, states, or events, it must also reference the relevant documents from [`../domain/README.md`](../domain/README.md).

## When to Create a Use Case

- A new stable user or operational scenario emerges.
- Multiple features implement or modify the same flow.
- A canonical owner is needed for trigger, preconditions, main flow, and postconditions.

## When a Use Case Is Not Needed

- The scenario is one-time only and lives inside a single feature.
- It is an implementation detail, not a product or operational flow.
- It is sufficient to describe it via `SC-*` in `brief.md`.

## Registry

| UC ID | Title | Status | Primary actor | Upstream PRD | Implemented by | Last updated |
| --- | --- | --- | --- | --- | --- | --- |
| `UC-XXX` | Scenario name | `draft` / `active` / `archived` | Who triggers the flow | `PRD-XXX` / `none` | `FT-XXX` | YYYY-MM-DD |

## Naming

- File format: `UC-XXX-short-name.md`
- Replace `XXX` with a stable project identifier.
- One use case may be upstream for multiple feature packages.

## Template

- Use the template at [`../flows/templates/use-case/UC-XXX.md`](../flows/templates/use-case/UC-XXX.md).
