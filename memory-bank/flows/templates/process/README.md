---
title: "PROC-XXX: Process Documentation Index"
doc_kind: process
doc_function: template
purpose: Governed wrapper template for `processes/README.md`. Read to create a catalog of project process documents without mixing wrapper metadata with the future index document frontmatter.
derived_from:
  - ../../../dna/governance.md
  - ../../../dna/frontmatter.md
  - ../../workflows.md
status: active
audience: humans_and_agents
template_for: process
template_target_path: ../../../processes/README.md
canonical_for:
  - process_template_index
---

# PROC-XXX: Process Documentation Index

This file describes the wrapper template. The instantiated `processes/README.md` lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

The `processes/` directory is for reusable process documents that live between an ad-hoc note and a feature package. It keeps process separate from product scope: repeatable workflows, session handoffs, lifecycle protocols, and other managed action sequences belong here.

This index template is designed for navigating a three-tier process lineup:

- compact process card;
- session handoff for continuing work between sessions;
- lifecycle protocol for long delivery processes with gates and verification.

Even if the project needs only one process, keep `README.md` as the routing layer: it records which process documents exist, what they cover, and when to open them.

## Instantiated Frontmatter

```yaml
title: "Process Documentation Index"
doc_kind: process
doc_function: index
purpose: "Navigation for reusable project process documents and selection of the right template for a specific workflow."
derived_from:
  - ../flows/workflows.md
status: active
audience: humans_and_agents
```

## Instantiated Body

```markdown
# Process Documentation Index

## About This Directory

The `processes/` directory holds reusable process documents: compact process cards, session handoffs for continuing work between sessions, and lifecycle protocols for complex delivery flows with verification and gates.

## Annotated Index

- [`process-card.md`](process-card.md)
  Read when you need a compact, repeatable process without a large state machine.
  Answers the question: how to capture a short workflow that can be executed from a single card.

- [`session-handoff.md`](session-handoff.md)
  Read when work is being transferred between sessions or computers and you need to save the current state, assumptions, risks, and next checks.
  Answers the question: how to safely continue an already started process without losing context.

- [`lifecycle-protocol.md`](lifecycle-protocol.md)
  Read when the process consists of phases, human gates, verification, and rollback and must survive a long delivery cycle.
  Answers the question: how to manage the full lifecycle of a change from start to handoff or closure.
```
