---
title: Engineering Documentation Index
doc_kind: engineering
doc_function: index
purpose: Navigation for engineering-level documentation. Read to set architecture patterns, frontend rules, testing policy, coding style, git workflow, and agent autonomy boundaries.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Engineering Documentation Index

The `memory-bank/engineering/` directory contains engineering rules that typically need to be adapted to a specific repository after copying the template.

- [Engineering Architecture Patterns](architecture.md) — code/module boundaries, runtime patterns, concurrency, error handling, and configuration ownership. Domain bounded contexts live separately in [`../domain/context-map.md`](../domain/context-map.md).
- [Frontend Engineering](frontend.md) — UI surfaces, frontend stack, component boundaries, design system integration, and i18n.
- [Testing Policy](testing-policy.md) — testing rules, required automated tests, sufficient coverage. Answers the question: when must a feature have test cases and when is manual-only verify acceptable.
- [Autonomy Boundaries](autonomy-boundaries.md) — agent autonomy boundaries: autopilot, supervision, escalation. Answers the question: what an agent can do independently and where it must stop and ask.
- [Coding Style](coding-style.md) — code formatting conventions, tooling, and local complexity rules.
- [Git Workflow](git-workflow.md) — git conventions: commits, branches, PRs, and optional worktrees.
- [ADR](../adr/README.md) — instantiated Architecture Decision Records for the project.
