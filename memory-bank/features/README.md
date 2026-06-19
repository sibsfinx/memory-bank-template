---
title: Feature Packages Index
doc_kind: feature
doc_function: index
purpose: Navigation for instantiated feature packages. Read to find an existing delivery unit or to understand where to create a new one.
derived_from:
  - ../dna/governance.md
  - ../flows/feature-flow.md
status: active
audience: humans_and_agents
---

# Feature Packages Index

The `memory-bank/features/` directory holds instantiated feature packages of the form `FT-XXX/`.

## Rules

- Each package is created according to the rules in [`../flows/feature-flow.md`](../flows/feature-flow.md).
- A bootstrap package starts with `README.md` and `brief.md`; after `Problem Ready`, `design.md` is added if `brief.md` marks `Design required: yes`; `implementation-plan.md` appears after the relevant upstream owners are ready.
- Use the templates in [`../flows/templates/feature/`](../flows/templates/feature/) for bootstrap and downstream documents.
- If the work requires a roadmap, risk register, and multiple delivery subissues, first create or update an epic package in [`../epics/README.md`](../epics/README.md).
- By default, a feature references the shared product context from [`../product/context.md`](../product/context.md), and when changing domain rules also references the relevant documents from [`../domain/README.md`](../domain/README.md).
- If a feature implements or substantially changes a stable project scenario, it must reference the corresponding `UC-*` from [`../use-cases/README.md`](../use-cases/README.md).
- In the template repository this directory may be empty. That is normal.

## Naming

- Base format: `FT-XXX/`
- Replace `XXX` with the identifier accepted in the project: issue id, ticket id, or another stable key
- One package = one delivery unit
