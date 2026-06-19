---
title: Context Map
doc_kind: domain
doc_function: canonical
purpose: Canonical place for bounded contexts, upstream/downstream relations, language ownership, and business integration boundaries.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - bounded_contexts
  - context_relationships
---

# Context Map

This document describes business bounded contexts and their relationships. It does not describe runtime deployment, package layout, or service topology — it focuses on domain boundaries.

## Bounded Contexts

| Context ID | Context name | Owns language/rules | Upstream | Downstream | Must not know about |
| --- | --- | --- | --- | --- | --- |
| `CTX-01` | ContextName | What domain facts this context owns | Which contexts provide input | Which contexts consume output | Internal details it must not access |

## Context Relationships

| Relationship ID | From | Direction | To | Contract | Constraints |
| --- | --- | --- | --- | --- | --- |
| `REL-01` | `CTX-01` | → | `CTX-02` | API / event / shared kernel | What limits this relationship |

## Shared Kernel / Published Language

Terms, value objects, or policies shared across contexts:

- `SK-01` What is shared and which contexts use it.

## Boundary Rules

1. Contexts own their domain facts and public contracts.
2. Internal state changes must respect published boundaries.
3. If a technical boundary differs from the domain boundary, explain the difference in engineering architecture.

## Open Questions

- `OQ-01` Areas of unclear ownership.
- `OQ-02` Legacy coupling that needs resolution.
