---
title: Domain Events
doc_kind: domain
doc_function: canonical
purpose: Canonical place for domain events as business-significant facts and their minimal contract.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - domain_events
---

# Domain Events

This document records domain events — business-significant facts. Events use past tense and represent facts that have already occurred. They must not express commands or requests.

## Events

| Event ID | Event name | Business meaning | Producer | Consumers | Mandatory facts |
| --- | --- | --- | --- | --- | --- |
| `EVT-01` | SomethingHappened | What business fact this represents | Which component produces it | Which systems consume it | What data it must carry |

## Rules

- Events represent facts, not commands.
- When a state transition changes, update the relevant state machine in [`states.md`](states.md).
- When responsibility shifts between contexts, reflect it in [`context-map.md`](context-map.md).

## Delivery Expectations

Capture business-level semantics here, not technical implementation details:

- Is deduplication important for this event?
- Does ordering matter?
- Retry logic and error handling belong in engineering architecture documentation.
