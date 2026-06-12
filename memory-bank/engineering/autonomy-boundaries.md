---
title: Autonomy Boundaries
doc_kind: engineering
doc_function: canonical
purpose: Agent autonomy boundaries: autopilot, supervision, escalation. Answers the question — what an agent can do independently and where it must stop and ask.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Autonomy Boundaries

This document establishes three operational tiers for agent decision-making.

## Autonomous Actions (No Approval Needed)

Agents may independently:

- Edit code within task scope
- Run local tests and linters
- Create branches and commits
- Access logs and metrics
- Maintain internal documentation

## Supervised Actions (Checkpoint Required)

Activities requiring human visibility before execution:

- Architectural decisions affecting multiple modules
- Database schema changes
- Deleting code or files
- Pull requests to main branches
- Configuration modifications in non-local environments
- Task decomposition plans that change scope

## Escalation Required (Stop And Ask)

Critical situations demanding human input:

- Ambiguous or contradictory business requirements
- Choosing between equivalent approaches with different trade-offs
- Any production actions or live data modifications
- User-facing communications
- Changes to payment or security-sensitive integrations

## Key Escalation Rule

When issues persist after 2–3 iterations without converging, the root cause likely stems from upstream requirements or environmental constraints rather than implementation details. Return to earlier planning stages rather than retrying the same approach.
