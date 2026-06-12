---
title: Customers And Users
doc_kind: product
doc_function: canonical
purpose: Canonical description of customer/user segments, jobs to be done, pains, evidence, and assumptions.
derived_from:
  - ../dna/governance.md
  - context.md
status: active
audience: humans_and_agents
canonical_for:
  - product_customers
  - user_segments
  - jobs_to_be_done
---

# Customers And Users

This document describes the people, teams, or organizations for whom the product is built. It does not define domain entities: if a customer segment shares a name with a domain concept, explicitly distinguish the product meaning from the domain meaning.

## Segments

| Segment ID | Segment | Job To Be Done | Current Pain | Success Signal | Evidence |
| --- | --- | --- | --- | --- | --- |
| `SEG-01` | Who they are | What job they are trying to accomplish | What is blocking them now | What will show improvement | Link or `unknown` |

## Users And Actors

| Actor ID | Actor | Uses product how | Decision power | Notes |
| --- | --- | --- | --- | --- |
| `ACT-01` | User role | Where and how they interact with the product | Buyer / admin / operator / end user | Important constraints |

If an actor becomes a participant in a stable scenario, record the use case in [`../use-cases/README.md`](../use-cases/README.md).

## Research Inputs

- Customer interviews, support tickets, sales notes, analytics cohorts, or usability studies.
- If no evidence exists yet, mark the assumption as `unvalidated`.

## Assumptions

- `ASM-01` An assumption about the customer or user that has not yet been confirmed.
- `ASM-02` An assumption that affects product priority or scope.

## Must Not Assume

- `NA-01` A need, segment, or behavior that must not be silently assumed without evidence.
