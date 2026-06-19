---
title: "PROC-XXX: Compact Process Card"
doc_kind: process
doc_function: template
purpose: Governed wrapper template for a compact process card. Read to capture a short reusable workflow without a heavy lifecycle scaffold.
derived_from:
  - ../../../dna/governance.md
  - ../../../dna/frontmatter.md
  - ../../workflows.md
status: active
audience: humans_and_agents
template_for: process
template_target_path: ../../../processes/PROCESS-XXX-process-card.md
canonical_for:
  - process_template_card
---

# PROC-XXX: Compact Process Card

This file describes the wrapper template. The instantiated process card lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

This variant is needed when a process repeats frequently but does not require a full protocol: one trigger, a clear owner, a short list of steps, and unambiguous exit criteria.

Good candidates for this template:

- short manual workflow;
- operational routine;
- repeatable internal step without complex gates;
- a process that fits comfortably on one page.

If the process begins to require handoff state, approval gates, rollback, or explicit verification phases, that is a signal to move to `session-handoff.md` or `lifecycle-protocol.md`.

## Instantiated Frontmatter

```yaml
title: "PROC-XXX: Compact Process Card"
doc_kind: process
doc_function: canonical
purpose: "Captures a short reusable workflow with one trigger, owner, steps, and exit criteria."
derived_from:
  - README.md
status: draft
audience: humans_and_agents
must_not_define:
  - full_delivery_lifecycle
  - approval_gates
  - rollback_protocol
```

## Instantiated Body

```markdown
# PROC-XXX: Compact Process Card

## Purpose

Briefly describe why this process exists and what result it must reliably produce.

## Trigger

- What starts the process.
- Who initiates it.
- What input data is needed before starting.

## Scope

### In Scope

- What this workflow does.

### Out Of Scope

- What it deliberately does not cover.

## Steps

1. Step 1.
2. Step 2.
3. Step 3.

## Exit Criteria

- What must be true for the process to be considered complete.

## Evidence

- Which artifact, log, link, or status confirms completion.

## Escalation

- When the process must be stopped and escalated to a human.
```
