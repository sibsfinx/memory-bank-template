---
title: Domain Documentation Index
doc_kind: domain
doc_function: index
purpose: Navigation for domain-level documentation. Read to capture the domain model, ubiquitous language, business rules, states, events, and bounded contexts.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Domain Documentation Index

The `memory-bank/domain/` directory stores the project's domain model: domain language, business entities, rules, states, events, and bounded contexts. This layer describes what must remain true regardless of the current product initiative or technical implementation.

Domain documents do not define market positioning, product metrics, UI design system, concurrency patterns, deployment config, or implementation sequence.

## Questions Domain Answers

- What concepts exist in the subject domain and what do they mean?
- What entities, value objects, actors, or aggregates are important for reasoning?
- What business rules and invariants must not be violated?
- What states and transitions are allowed?
- What domain events are business-significant facts?
- Where do bounded contexts and language boundaries lie?

## Boundary With `product/`

| Layer | Answers questions about | Does not answer questions about |
| --- | --- | --- |
| `product/` | Why the product exists, who it is for, what outcomes and metrics matter | What domain entities, states, invariants, and events exist |
| `domain/` | What is true in the subject domain and what rules the system must obey | Why this audience is priority, how the product is positioned, what roadmap is chosen |

Example:

- Product: "Reduce the number of manual operations for segment `SEG-01`."
- Domain: "`Invoice` cannot be marked paid without a confirmed payment event."

## Boundary With Engineering

- `domain/context-map.md` describes business bounded contexts and language ownership.
- `engineering/architecture.md` describes code/module boundaries, runtime patterns, concurrency, error handling, and configuration ownership.
- If a document answers "what business rule is true?" it belongs to `domain/`.
- If a document answers "how to implement this safely in the system?" it belongs to `engineering/`.

## Annotated Index

- [Glossary](glossary.md) — ubiquitous language, terms, prohibited ambiguities, and canonical names.
- [Domain Model](model.md) — key domain concepts, relationships, ownership, and model notes.
- [Domain Rules](rules.md) — business rules, invariants, policies, and rule ownership.
- [States](states.md) — lifecycle states, allowed transitions, and terminal states.
- [Events](events.md) — domain events as business-significant facts and their minimal contract.
- [Context Map](context-map.md) — bounded contexts, upstream/downstream relations, and language boundaries.
