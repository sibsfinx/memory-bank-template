---
title: FT-XXX Feature README Template
doc_kind: feature
doc_function: template
purpose: Governed wrapper template for the feature-level `README.md`. Read to instantiate a bootstrap-safe routing layer for a feature without mixing wrapper metadata with the target README frontmatter.
derived_from:
  - ../../feature-flow.md
  - ../../../dna/frontmatter.md
status: active
audience: humans_and_agents
template_for: feature
template_target_path: ../../../features/FT-XXX/README.md
---

# FT-XXX Feature Template

This file describes the wrapper template itself. The instantiated feature README lives below as an embedded contract and is copied into the feature package without the wrapper frontmatter and history.

## Wrapper Notes

The `memory-bank/flows/templates/feature/` directory holds wrapper templates for a feature package: this README template, the canonical `brief.md` template, the conditional `design.md` template, and the derived `implementation-plan.md` template. New packages always use `brief.md`, and add `design.md` only when `brief.md` records `Design required: yes`.

When creating a new feature package, the embedded README must remain bootstrap-safe: initially it routes only to the instantiated `brief.md`, and `design.md`, `implementation-plan.md`, and related ADRs are added as those documents appear.

Downstream routes for a living feature package are added as lifecycle stages are passed. Typical examples of post-bootstrap routes:

- [`design.md`](design.md)
  Read when you need to: after `Problem Ready`, capture or verify the selected design, to-be C4 architecture model, accepted local decisions, contracts, and local rollout/backout semantics.
  Answers the question: how exactly the feature is implemented without mixing solution space with problem space.

- [`implementation-plan.md`](implementation-plan.md)
  Read when you need to: after upstream owners are ready, lay out implementation by steps, workstreams, checkpoints, and traceability to canonical IDs.
  Answers the question: how to execute the feature implementation from the current state to acceptance.

- `../../../adr/ADR-XXX.md`
  Read when you need to: if the feature has a related ADR, create or verify it with the correct `decision_status`.
  Answers the question: why a specific architectural or engineering decision is chosen for this feature and what stage it is at.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: Feature Package"
doc_kind: feature
doc_function: index
purpose: "Bootstrap-safe navigation for the feature documentation. Read to navigate first to the canonical `brief.md`; downstream routes are added only after the corresponding documents appear."
derived_from:
  - ../../dna/governance.md
  - brief.md
status: active
audience: humans_and_agents
```

## Instantiated Body

```markdown
# FT-XXX: Feature Package

## About This Directory

The feature package directory begins with the canonical `brief.md`. Downstream solution/execution routes are added only after the corresponding documents appear. Read `brief.md` first, then expand routing as design, implementation plan, and related ADRs appear.

## Annotated Index

- [`brief.md`](brief.md)
  Read when you need to: open the instantiated canonical feature document immediately after bootstrapping a new feature package.
  Answers the question: where the problem space, canonical verify contract, and stable IDs for this feature live.

After downstream documents appear, add routes here for `design.md`, `implementation-plan.md`, and related ADRs.
```
