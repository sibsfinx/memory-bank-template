---
title: Domain Rules
doc_kind: domain
doc_function: canonical
purpose: Canonical place for business rules, invariants, policies, and rule ownership.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - domain_invariants
  - domain_policies
---

# Domain Rules

This document records business rules that any implementation must comply with. UI behavior and technical exception handling belong here only when directly tied to business logic.

## Invariants

Conditions that must always be true.

| Invariant ID | Invariant | Context | Rationale | Source |
| --- | --- | --- | --- | --- |
| `INV-01` | What must always be true | Where it applies | Why it matters | Reference |

## Policies

Decision-making processes with inputs, verdicts, and accountability.

| Policy ID | Policy | Inputs | Verdict | Owner |
| --- | --- | --- | --- | --- |
| `POL-01` | What decision is made | What information is needed | Possible outcomes | Who is accountable |

## Cross-Context Rules

Requirements spanning multiple bounded contexts.

| Rule ID | Rule | Contexts involved | Contract |
| --- | --- | --- | --- |
| `CCR-01` | What must hold across contexts | Which contexts participate | Mandatory API/event usage |

## Change Policy

- Documentation must be updated when a domain invariant is modified.
- Feature-scoped rules stay in delivery packages until they achieve shared status.
- Architectural rules are referenced via Architecture Decision Records (ADRs).
