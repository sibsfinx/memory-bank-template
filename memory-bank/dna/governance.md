---
doc_kind: governance
doc_function: canonical
purpose: SSoT implementation and dependency tree rules. Answers the question — who owns which fact.
derived_from:
  - principles.md
status: active
---

# Document Governance

A `governed document` is a markdown file in `memory-bank/` with valid YAML frontmatter. The SSoT principle is defined in [principles.md](principles.md). This document describes the mechanism for enforcing it.

## SSoT Implementation

1. Only `active` documents are authoritative. A `draft` does not override an `active`.
2. Among documents valid by status, the upstream wins: first `canonical_for`, then the dependency tree.
3. Publication status (`status`) is separate from entity lifecycle (`delivery_status`, `decision_status`).

## Source Dependency Tree

1. The `derived_from` field lists direct upstream documents. Authority flows upstream → downstream.
2. The root document is `principles.md`, which has no `derived_from`. For every `active` non-root document, `derived_from` is required.
3. Cyclic dependencies are forbidden. Changing an upstream document may require updating downstream documents.

## Governance-specific Frontmatter Fields

Governance documents (DNA, flows) use additional fields not in the common schema (`frontmatter.md`):

| Field | Values | Purpose |
|-|-|-|
| `doc_kind` | `governance`, `project`, `product`, `domain`, `prd`, `use_case`, `epic`, `feature`, `feature-support`, `engineering`, `ops`, `adr`, `prompt`, `process` | Document type or artifact kind |
| `doc_function` | `canonical`, `index`, `template`, `derived`, `reference`, `convention`, `roadmap`, `decision_log`, `subissue_registry`, `risk_register` | Role: canonical owner of a fact, navigation index, template, downstream artifact, reference companion, convention, or specialized epic owner |

These fields are required for governance documents and recommended for product/domain/ops/engineering/project documents so that agents can distinguish the knowledge layer and role of a file.
