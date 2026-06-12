---
title: "PROC-XXX: Session Handoff"
doc_kind: process
doc_function: template
purpose: Governed wrapper template for a session handoff. Read to save process state between sessions without losing assumptions, risks, and next checks.
derived_from:
  - ../../../dna/governance.md
  - ../../../dna/frontmatter.md
  - ../../workflows.md
status: active
audience: humans_and_agents
template_for: process
template_target_path: ../../../processes/PROCESS-XXX-session-handoff.md
canonical_for:
  - process_template_session_handoff
---

# PROC-XXX: Session Handoff

This file describes the wrapper template. The instantiated session handoff lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

This template is for cases when work is interrupted and must be continued later: a new session, a different computer, a different operator, or a long-running workflow with pauses between steps.

The key idea: the handoff captures only what is genuinely needed for safe continuation — not every detail indiscriminately.

Always record:

- what has already been completed;
- the current step where work stopped;
- working assumptions;
- open risks;
- next checks;
- the next concrete action.

If the process begins to require formal gates, rollback, and multi-phase verification, use `lifecycle-protocol.md`.

## Instantiated Frontmatter

```yaml
title: "PROC-XXX: Session Handoff"
doc_kind: process
doc_function: canonical
purpose: "Records the state of an incomplete process so the next session can continue without losing context."
derived_from:
  - README.md
status: draft
audience: humans_and_agents
must_not_define:
  - long_term_project_policy
  - product_scope
```

## Instantiated Body

```markdown
# PROC-XXX: Session Handoff

## Current State

- What has already been done.
- Exactly where work stopped.
- Which artifact is current.

## Completed

- List of completed steps or checks.

## Current Step

- One specific step that is in progress now or must be done next.

## Assumptions

- Which assumptions were made during the work.

## Open Risks

- Which risks have not yet been resolved.

## Next Checks

- What must be verified before continuing.

## Evidence Log

| Time | Fact / action | Evidence |
|---|---|---|
| `<yyyy-mm-dd hh:mm>` | `<fact-or-action>` | `<source-or-command-output-ref>` |

## Next Action

- Who acts.
- What exactly they do.
- When to stop.

## Stop Conditions

- When work cannot continue without a human.
```
