---
title: "ADR-XXX: Short Decision Name"
doc_kind: adr
doc_function: template
purpose: Governed wrapper template for an ADR. Read to instantiate a decision record without mixing the wrapper document metadata with the future ADR frontmatter.
derived_from:
  - ../../../dna/governance.md
  - ../../../dna/frontmatter.md
status: active
audience: humans_and_agents
template_for: adr
template_target_path: ../../../adr/ADR-XXX.md
---

# ADR-XXX: Short Decision Name

This file describes the wrapper template. The instantiated ADR lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

`decision_status: proposed` in the embedded contract below means the ADR text is a proposal and is not considered an accepted decision until the instantiated ADR is moved to `accepted` status.

## Instantiated Frontmatter

```yaml
title: "ADR-XXX: Short Decision Name"
doc_kind: adr
doc_function: canonical
purpose: "Records an architectural or engineering decision, its current `decision_status`, and consequences."
derived_from:
  - ../features/FT-XXX/brief.md
status: draft
decision_status: proposed
date: YYYY-MM-DD
audience: humans_and_agents
must_not_define:
  - current_system_state
  - implementation_plan
```

## Instantiated Body

```markdown
# ADR-XXX: Short Decision Name

## Context

What problem, constraint, trade-off, or architectural tension needs to be resolved.

## Decision Drivers

- What requirements or constraints influence the choice.
- What KPIs, operational, or product factors matter.
- What dependencies and already-accepted decisions must be considered.

## Considered Options

| Option | Pros | Cons | Why it is / is not the leading candidate |
| --- | --- | --- | --- |
| `Option A` | What it provides | What constraints it creates | Reason for the decision |

## Decision

For `decision_status: proposed`, describe the proposed solution here and avoid the language of final choice (`selected`, `definitively rejected`, `accepted`) until the ADR is moved to `accepted`. After the ADR is moved to `accepted`, update the wording so that this section records the accepted decision, its scope of applicability, and the affected components.

## Consequences

### Positive

What is simplified, improved, or made possible.

### Negative

What constraints, debts, or additional costs appear.

### Neutral / Organizational

What documents, processes, or areas of responsibility need to be updated after acceptance.

## Risks And Mitigation

What risks remain after the choice and how we reduce them.

## Follow-up

What downstream documents, tasks, benchmarks, or migrations must follow this decision.

## Related Links

- Feature `brief.md` / `design.md` / analysis documents that provide context.
- Related ADRs, if this decision depends on them or refines them.
```
