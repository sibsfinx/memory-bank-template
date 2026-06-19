---
title: Domain States
doc_kind: domain
doc_function: canonical
purpose: Canonical place for lifecycle states, allowed transitions, terminal states, and state-related invariants.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - domain_states
  - state_transitions
---

# Domain States

This document records business-level lifecycle states. Keep only business-visible states here; technical runtime states belong in architecture documentation.

## State Machines

| State Machine ID | Concept | Lifecycle owner | Notes |
| --- | --- | --- | --- |
| `SM-01` | Which concept has a lifecycle | What document owns it | Any important notes |

## States

| State ID | State Machine | State name | Meaning | Entry conditions | Exit conditions | Terminal |
| --- | --- | --- | --- | --- | --- | --- |
| `ST-01` | `SM-01` | stateName | What this state means | How we enter it | How we leave it | yes / no |

## Transitions

| Transition ID | From state | To state | Trigger | Preconditions |
| --- | --- | --- | --- | --- |
| `TR-01` | `ST-01` | `ST-02` | What causes the transition | What must be true before it can happen |

## State Invariants

Business rules that hold across states.

| Invariant ID | Invariant | Applies to states | Rationale |
| --- | --- | --- | --- |
| `SI-01` | What must remain true | Which states | Why this matters |
