# memory-bank-template

A portable documentation template for agent-driven software development projects.

## What Is This

`memory-bank` is a structured knowledge layer for software projects: versioned documents that preserve important context across sessions, participants, and code changes. Copy `./memory-bank` into your project root, then adapt it to your product, domain, engineering stack, processes, and constraints.

## Quick Start

1. Copy the `memory-bank/` directory to your project root
2. Adapt at minimum: `product/`, `domain/`, `engineering/`, and `ops/`
3. Run the audit before opening pull requests:

```bash
python3 scripts/check_memory_bank_index.py
```

## Validation

The audit script checks:
- Broken relative markdown links and orphaned documents
- Navigation reachability from entry points (default max depth: 3 hops)
- Expected README index structures

## Structure

```
memory-bank/
├── dna/          # Governance: SSoT, frontmatter schema, lifecycle rules
├── product/      # Vision, customers, metrics, marketing, roadmap
├── domain/       # Glossary, domain model, rules, states, events, context map
├── engineering/  # Architecture, testing, coding style, git workflow, autonomy
├── ops/          # Dev environment, stages, release, config, runbooks
├── flows/        # Lifecycle flows and governed document templates
├── prd/          # Instantiated Product Requirements Documents
├── epics/        # Instantiated epic packages
├── use-cases/    # Canonical use cases
├── features/     # Instantiated feature packages
├── prompts/      # Reusable prompt documents
└── adr/          # Architecture Decision Records
```
