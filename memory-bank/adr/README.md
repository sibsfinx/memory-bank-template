---
title: Architecture Decision Records Index
doc_kind: adr
doc_function: index
purpose: Navigation for project ADRs. Read to find existing accepted decisions or create a new ADR from the template.
derived_from:
  - ../dna/governance.md
  - ../flows/templates/adr/ADR-XXX.md
status: active
audience: humans_and_agents
---

# Architecture Decision Records Index

The `memory-bank/adr/` directory holds instantiated project ADRs.

- Create a new ADR from the template at [`../flows/templates/adr/ADR-XXX.md`](../flows/templates/adr/ADR-XXX.md).
- Keep only real decision records in this directory — not notes or draft research.
- If no ADRs exist yet, this index remains empty and serves as the designated location for future decisions.

## Naming

- File format: `ADR-XXX-short-decision-name.md`
- Numbering is monotonic and is never reused.
- The file title must match the `title` field in frontmatter.

## Statuses

- `proposed` — decision is formulated but not yet accepted
- `accepted` — decision is accepted and considered canonical input for downstream documents
- `superseded` — decision has been replaced by another ADR
- `rejected` — decision was reviewed and declined
