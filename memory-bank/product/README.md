---
title: Product Documentation Index
doc_kind: product
doc_function: index
purpose: Navigation for product-level documentation. Read to understand why the product exists, who it is built for, and how success is measured.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Product Documentation Index

The `memory-bank/product/` directory stores stable product context for the project: why, users, outcomes, metrics, positioning, and roadmap. This layer prevents repeating the same product background in every PRD, use case, and feature package.

Product documents do not define the domain model, implementation architecture, feature acceptance criteria, or execution sequence.

## Questions Product Answers

- Why does the product or platform exist?
- Who is it built for: customers, users, segments, actors?
- What customer jobs, pains, and outcomes matter?
- What metrics show success at the product level?
- How is the product positioned relative to alternatives?
- What themes, bets, or roadmap horizons guide future work?

## Boundary With `domain/`

| Layer | Answers questions about | Does not answer questions about |
| --- | --- | --- |
| `product/` | Why, for whom, what outcome, how success is measured, how the product is positioned | What domain entities exist, what invariants are required, how the implementation is structured |
| `domain/` | What concepts, rules, states, events, and bounded contexts exist in the subject domain | Why this business initiative matters, which market segments are priority, which marketing channels are chosen |

Example:

- Product: "Reduce operator time on request processing and increase the share of self-service completion."
- Domain: "`Application` cannot transition to `approved` until mandatory checks have a final verdict."

## Boundary With PRD

- `product/` — project-wide and long-lived knowledge base.
- `prd/PRD-XXX-short-name.md` — initiative-specific wrapper: which product problem we are solving now, for which users, and with what scope.
- If a document only repeats general context, customers, or metrics, update `product/` rather than creating a new PRD.

## Annotated Index

- [Product Context](context.md) — overall product context, key workflows, product constraints, and source documents.
- [Vision](vision.md) — long-term product direction, strategic bets, experience principles, and non-goals.
- [Customers](customers.md) — customer/user segments, jobs to be done, pains, evidence, and assumptions.
- [Metrics](metrics.md) — product metrics, baselines, targets, measurement ownership, and instrumentation constraints.
- [Marketing](marketing.md) — positioning, messaging, channels, competitive alternatives, and launch constraints.
- [Roadmap](roadmap.md) — product themes, bets, horizons, and dependencies without turning into a feature backlog.
