---
title: Template Documentation Index
doc_kind: project
doc_function: index
purpose: Root navigation for the template memory-bank. Read first to understand the structure and adaptation points for a specific project.
derived_from:
  - dna/principles.md
  - dna/governance.md
status: active
audience: humans_and_agents
---

# Documentation Index

The `memory-bank/` directory contains a portable project documentation template for software development. After copying to a downstream repository, adapt `product/`, `domain/`, `engineering/`, and `ops/` to the real product, domain, stack, processes, and constraints of the project.

## Annotated Index

- [`product/README.md`](product/README.md)
  Read when you need to: capture product context, vision, customers, metrics, marketing, and roadmap.

- [`domain/README.md`](domain/README.md)
  Read when you need to: capture glossary, domain model, rules, states, events, and bounded contexts.

- [`prd/README.md`](prd/README.md)
  Read when you need to: describe a product initiative between the overall product context and downstream feature packages.

- [`epics/README.md`](epics/README.md)
  Read when you need to: manage a large initiative through roadmap, decision log, risks, and a set of related delivery subissues.

- [`use-cases/README.md`](use-cases/README.md)
  Read when you need to: register a stable user or operational scenario for the project.

- [`prompts/README.md`](prompts/README.md)
  Read when you need to: find or create a reusable prompt document with the original formulation and a copyable improved version.

- [`ops/README.md`](ops/README.md)
  Read when you need to: describe local development, environments, releases, configuration, and runbooks.

- [`engineering/README.md`](engineering/README.md)
  Read when you need to: define architecture patterns, frontend rules, testing policy, coding style, git workflow, and agent autonomy boundaries.

- [`dna/README.md`](dna/README.md)
  Read when you need to: check SSoT rules, frontmatter contract, and documentation governance rules.

- [`flows/README.md`](flows/README.md)
  Read when you need to: create an epic or feature package, advance an initiative through lifecycle gates, or use a template.

- [`adr/README.md`](adr/README.md)
  Read when you need to: find or create an Architecture Decision Record.

- [`features/README.md`](features/README.md)
  Read when you need to: understand where instantiated feature packages live.
