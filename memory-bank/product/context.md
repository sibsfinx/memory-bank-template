---
title: Product Context
doc_kind: product
doc_function: canonical
purpose: Canonical project-wide description of the product, problem space, and top-level outcomes. Read before PRDs, use cases, and feature briefs to avoid repeating the same background in each delivery unit.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - project_product_context
  - product_problem_space
  - top_level_outcomes
must_not_define:
  - domain_model
  - domain_invariants
  - implementation_sequence
  - architecture_decision
---

# Product Context

This document captures the general product context for the project. Downstream documents should reference it rather than rewriting the same background each time.

A PRD, if needed, narrows down a specific initiative relative to the already-established project-wide context.

## Boundary With PRD And Domain

- `product/context.md` — project-wide context: the product, users, key product workflows, top-level outcomes, and stable product constraints.
- `prd/PRD-XXX-short-name.md` — initiative layer: which specific product problem is being addressed now, for which users, and with what scope.
- `domain/` — domain model: language, entities, states, invariants, events, and bounded contexts that must remain true regardless of the current initiative.
- If a new document simply repeats the general project background without introducing initiative-specific scope, there is no need to create a PRD.

## Product Context

Describe the project in 2–4 short paragraphs:

- who the primary customers and users are;
- what task the product helps solve;
- why the existing solution is insufficient;
- what the product or platform boundaries are.

Example:

> The team maintains an internal SaaS platform for operational automation. Users expect predictable workflows, transparent statuses, and fast access to critical actions. Any new feature must either reduce operational load, reduce the risk of errors, or accelerate the user's path to the target outcome.

## Core Product Workflows

- `WF-01` Key user workflow number one.
- `WF-02` Key user workflow number two.
- `WF-03` Internal or operational workflow that must not be broken.

If a workflow becomes a stable canonical scenario with trigger, preconditions, main flow, and postconditions, create a separate `UC-*` in [`../use-cases/README.md`](../use-cases/README.md).

## Top-Level Outcomes

Document detailed definitions and metric ownership in [`metrics.md`](metrics.md). Here, keep only a brief executive summary.

| Metric ID | Metric | Baseline | Target | Measurement method |
| --- | --- | --- | --- | --- |
| `MET-01` | What we count as success at the product level | Current state | Desired level | How we measure |

## Product Constraints

- `PCON-01` A product, market, customer promise, or go-to-market constraint that affects downstream features.
- `PCON-02` A compliance, integration, or customer operations constraint that defines a product boundary.

Document domain-level invariants and state rules in [`../domain/rules.md`](../domain/rules.md) and [`../domain/states.md`](../domain/states.md).

## Source Documents

- Add links here to strategy docs, roadmap, customer research, analytics dashboards, or other upstream artifacts if they exist.
- If no upstream sources exist yet, state this explicitly; do not invent them.
