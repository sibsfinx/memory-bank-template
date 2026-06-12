---
doc_kind: governance
doc_function: canonical
purpose: Maintenance rules and sync checklist for governed documents.
derived_from:
  - governance.md
status: active
---

# Document Lifecycle

Rules that ensure consistency of governed documentation when changes occur.

## Maintenance Rules

1. **Upstream first.** When changing a fact, first find and update the canonical owner.
2. **Downstream sync.** After changing an upstream document, check its `derived_from` dependents.
3. **README sync.** When a document is added, removed, or renamed, update the parent README.
4. **Conflict = defect.** Any discrepancy within the authoritative set must be resolved immediately.
5. **Conflict = report, not fix.** An agent that discovers a discrepancy while reading records it as a finding and reports to a human. Self-correction is allowed only if the current task explicitly requires changing that document.

## Sync Checklist

Before committing changes to governed documentation:

- [ ] frontmatter is valid; for `active` non-root documents `derived_from` is set
- [ ] for the lifecycle-owning canonical `brief.md`, `delivery_status` is set; for `adr` documents, `decision_status` is set
- [ ] parent `README.md` is updated when the set of documents or reading order changes
