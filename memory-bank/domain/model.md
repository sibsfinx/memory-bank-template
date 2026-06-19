---
title: Domain Model
doc_kind: domain
doc_function: canonical
purpose: Canonical description of key domain concepts, relationships, ownership, and model boundaries.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - domain_concepts
  - domain_relationships
---

# Domain Model

This document captures the conceptual domain model. It does not replace database schemas, API contracts, or code module layouts — it focuses on business-level modeling.

## Concepts

| Concept ID | Name | Kind | Owned by | Description | Key relationships |
| --- | --- | --- | --- | --- | --- |
| `DC-01` | ConceptName | entity / value object / aggregate / actor / policy | bounded context | What it represents | Belongs to, contains, triggers |

## Relationship Map

Business-level connections between concepts.

| From | Relationship | To | Notes |
| --- | --- | --- | --- |
| `DC-01` | belongs to / contains / triggers / depends on | `DC-02` | Why this relationship matters |

## Concept Ownership

| Concept | Owner context | Can modify | Can read via public contract |
| --- | --- | --- | --- |
| `DC-01` | Context name | Owner only | Other contexts via API/event |

## Model Boundaries

What is consciously excluded from the domain model:

- `MB-01` What is intentionally left out and why.

Legacy terms retained only for compatibility:

- `LT-01` Old term → canonical replacement.

## Related Documents

- Business rules: [`rules.md`](rules.md)
- State transitions: [`states.md`](states.md)
- Bounded contexts: [`context-map.md`](context-map.md)
