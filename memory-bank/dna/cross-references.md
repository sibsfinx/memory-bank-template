---
doc_kind: governance
doc_function: canonical
purpose: Rules for bidirectional navigation between code and docs.
derived_from:
  - governance.md
status: active
---

# Cross-references (code ↔ docs)

This document establishes bidirectional navigation rules between code and documentation.

## Code → Docs

Modules implementing documented logic must include a comment-link to the canonical document, specifying:

1. Relative path from the repository root
2. An annotation explaining which documentation aspect applies

## Docs → Code

Documentation may reference code files and line numbers once an implementation exists. Each link requires an annotation indicating what readers will find there and why it matters.

The goal is to maintain traceability so developers can navigate from implementation to specifications and vice versa.
