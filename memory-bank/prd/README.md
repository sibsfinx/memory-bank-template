---
title: Product Requirements Documents Index
doc_kind: prd
doc_function: index
purpose: Navigation for instantiated PRDs. Read to find an existing product requirements document or to understand when and how to create a new one.
derived_from:
  - ../dna/governance.md
  - ../flows/templates/prd/PRD-XXX.md
status: active
audience: humans_and_agents
---

# Product Requirements Documents Index

The `memory-bank/prd/` directory holds instantiated PRD documents for the project.

PRDs occupy the middle layer between the project-wide product context and downstream feature packages.

## Versus `product/context.md`

The context document remains project-wide and must not be turned into a PRD. A PRD inherits this context via `derived_from` but captures only the initiative-specific problem, users, goals, scope, and metrics.

## Versus `domain/`

Domain documents own the subject model, terminology, invariants, and bounded contexts. A PRD may reference domain materials when the initiative modifies domain rules, but must not invent new domain concepts without updating the corresponding domain document.

## When to Create a PRD

- The initiative breaks into multiple feature packages.
- Product requirements must be documented before implementation design begins.
- There is a risk of conflating product requirements with technical details.

## When to Skip

- The task fits entirely within a single `brief.md`.
- The product context is already covered by `product/context.md`.

## Naming

- File format: `PRD-XXX-short-name.md`
- Replace `XXX` with a stable project identifier such as an initiative or epic ID.
- A single PRD can be upstream for multiple feature packages.

## Template

- Use the template at [`../flows/templates/prd/PRD-XXX.md`](../flows/templates/prd/PRD-XXX.md).
