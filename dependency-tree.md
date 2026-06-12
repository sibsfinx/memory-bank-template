---
title: Document Dependency Tree
purpose: Current dependency map of documents inside `memory-bank/`. Placed at the repository root as a reference note to avoid cluttering the template DNA.
status: active
derived_from:
  - memory-bank/dna/governance.md
---

# Document Dependency Tree

This document records the current dependency map of documents in `memory-bank/`.

Important: the structure here is not a strict tree but a directed acyclic graph. The `derived_from` field defines direct upstream dependencies, so some documents have multiple parents. Below is a compressed tree followed by a list of additional cross-edges.

This file lives at the repository root and is not considered part of the `memory-bank/` tree; it only references it as an external reference note.

## Roots

- Navigation root: [`README.md`](README.md). This is the entry point for reading the repository, but not the authority root of the template.
- Semantic root: [`memory-bank/dna/principles.md`](memory-bank/dna/principles.md). This is the root of the governance tree from which downstream rules inherit.

## Compressed Tree

```text
memory-bank/README.md

memory-bank/dna/principles.md
├── memory-bank/dna/README.md
├── memory-bank/dna/cross-references.md
└── memory-bank/dna/governance.md
    ├── memory-bank/dna/frontmatter.md
    ├── memory-bank/dna/lifecycle.md
    ├── memory-bank/product/README.md
    ├── memory-bank/product/context.md
    ├── memory-bank/product/customers.md
    ├── memory-bank/product/marketing.md
    ├── memory-bank/product/metrics.md
    ├── memory-bank/product/roadmap.md
    ├── memory-bank/product/vision.md
    ├── memory-bank/domain/README.md
    ├── memory-bank/domain/context-map.md
    ├── memory-bank/domain/events.md
    ├── memory-bank/domain/glossary.md
    ├── memory-bank/domain/model.md
    ├── memory-bank/domain/rules.md
    ├── memory-bank/domain/states.md
    ├── memory-bank/engineering/README.md
    ├── memory-bank/engineering/architecture.md
    ├── memory-bank/engineering/autonomy-boundaries.md
    ├── memory-bank/engineering/coding-style.md
    ├── memory-bank/engineering/frontend.md
    ├── memory-bank/engineering/git-workflow.md
    ├── memory-bank/engineering/testing-policy.md
    ├── memory-bank/features/README.md
    ├── memory-bank/flows/README.md
    ├── memory-bank/flows/feature-flow.md
    ├── memory-bank/flows/templates/README.md
    ├── memory-bank/flows/templates/adr/ADR-XXX.md
    ├── memory-bank/flows/templates/prd/PRD-XXX.md
    ├── memory-bank/flows/templates/use-case/UC-XXX.md
    ├── memory-bank/flows/workflows.md
    ├── memory-bank/ops/README.md
    ├── memory-bank/ops/config.md
    ├── memory-bank/ops/development.md
    ├── memory-bank/ops/release.md
    ├── memory-bank/ops/runbooks/README.md
    ├── memory-bank/ops/stages.md
    ├── memory-bank/prd/README.md
    ├── memory-bank/use-cases/README.md
    └── memory-bank/adr/README.md
```

## Additional Dependency Edges

These connections are not visible in the compressed tree above but exist in `derived_from` and matter for authority flow.

### DNA and Flows

- This `dependency-tree.md` file depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) but intentionally lives outside `memory-bank/`.
- [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md) depends on both [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md).
- [`memory-bank/flows/workflows.md`](memory-bank/flows/workflows.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md).
- [`memory-bank/flows/README.md`](memory-bank/flows/README.md) depends simultaneously on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md), [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md), [`memory-bank/flows/workflows.md`](memory-bank/flows/workflows.md), and [`memory-bank/flows/templates/README.md`](memory-bank/flows/templates/README.md).

### Feature-related Docs

- [`memory-bank/engineering/testing-policy.md`](memory-bank/engineering/testing-policy.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md).
- [`memory-bank/features/README.md`](memory-bank/features/README.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md).
- [`memory-bank/flows/templates/feature/README.md`](memory-bank/flows/templates/feature/README.md) depends on [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md) and [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md).
- [`memory-bank/flows/templates/feature/brief.md`](memory-bank/flows/templates/feature/brief.md) depends on [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md), [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md), and [`memory-bank/engineering/testing-policy.md`](memory-bank/engineering/testing-policy.md).
- [`memory-bank/flows/templates/feature/design.md`](memory-bank/flows/templates/feature/design.md) depends on [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md) and [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md).
- [`memory-bank/flows/templates/feature/implementation-plan.md`](memory-bank/flows/templates/feature/implementation-plan.md) depends on [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md), [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md), and [`memory-bank/engineering/testing-policy.md`](memory-bank/engineering/testing-policy.md).
- Feature support templates [`runtime-surfaces.md`](memory-bank/flows/templates/feature/support/runtime-surfaces.md), [`ui-reference.md`](memory-bank/flows/templates/feature/support/ui-reference.md), and [`use-cases.md`](memory-bank/flows/templates/feature/support/use-cases.md) depend on [`memory-bank/flows/feature-flow.md`](memory-bank/flows/feature-flow.md) and [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md).

### Product And Domain Docs

- [`memory-bank/product/context.md`](memory-bank/product/context.md), [`memory-bank/product/vision.md`](memory-bank/product/vision.md), [`memory-bank/product/customers.md`](memory-bank/product/customers.md), [`memory-bank/product/metrics.md`](memory-bank/product/metrics.md), [`memory-bank/product/marketing.md`](memory-bank/product/marketing.md), and [`memory-bank/product/roadmap.md`](memory-bank/product/roadmap.md) depend on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and the product upstream documents listed in their `derived_from`.
- [`memory-bank/domain/glossary.md`](memory-bank/domain/glossary.md), [`memory-bank/domain/model.md`](memory-bank/domain/model.md), [`memory-bank/domain/rules.md`](memory-bank/domain/rules.md), [`memory-bank/domain/states.md`](memory-bank/domain/states.md), [`memory-bank/domain/events.md`](memory-bank/domain/events.md), and [`memory-bank/domain/context-map.md`](memory-bank/domain/context-map.md) depend on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and the domain upstream documents listed in their `derived_from`.
- [`memory-bank/engineering/architecture.md`](memory-bank/engineering/architecture.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/domain/context-map.md`](memory-bank/domain/context-map.md).
- [`memory-bank/engineering/frontend.md`](memory-bank/engineering/frontend.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/product/context.md`](memory-bank/product/context.md).
- [`memory-bank/flows/templates/prd/PRD-XXX.md`](memory-bank/flows/templates/prd/PRD-XXX.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md), [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md), and [`memory-bank/product/context.md`](memory-bank/product/context.md).
- [`memory-bank/flows/templates/use-case/UC-XXX.md`](memory-bank/flows/templates/use-case/UC-XXX.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md), [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md), and [`memory-bank/product/context.md`](memory-bank/product/context.md).
- [`memory-bank/prd/README.md`](memory-bank/prd/README.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/flows/templates/prd/PRD-XXX.md`](memory-bank/flows/templates/prd/PRD-XXX.md).
- [`memory-bank/use-cases/README.md`](memory-bank/use-cases/README.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/flows/templates/use-case/UC-XXX.md`](memory-bank/flows/templates/use-case/UC-XXX.md).

### ADR and Template Indexes

- [`memory-bank/flows/templates/adr/ADR-XXX.md`](memory-bank/flows/templates/adr/ADR-XXX.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md).
- [`memory-bank/adr/README.md`](memory-bank/adr/README.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and [`memory-bank/flows/templates/adr/ADR-XXX.md`](memory-bank/flows/templates/adr/ADR-XXX.md).
- [`memory-bank/flows/templates/README.md`](memory-bank/flows/templates/README.md) depends on [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md) and all template documents in the `flows/templates/` directory.

## Reading Order

To quickly enter the template top-down, read in this order:

1. [`memory-bank/dna/principles.md`](memory-bank/dna/principles.md)
2. [`memory-bank/dna/governance.md`](memory-bank/dna/governance.md)
3. [`memory-bank/dna/frontmatter.md`](memory-bank/dna/frontmatter.md)
4. Product layer: [`memory-bank/product/README.md`](memory-bank/product/README.md)
5. Domain layer: [`memory-bank/domain/README.md`](memory-bank/domain/README.md)
6. Delivery flow: [`memory-bank/flows/README.md`](memory-bank/flows/README.md)
7. Engineering rules: [`memory-bank/engineering/README.md`](memory-bank/engineering/README.md)
8. Ops context: [`memory-bank/ops/README.md`](memory-bank/ops/README.md)
