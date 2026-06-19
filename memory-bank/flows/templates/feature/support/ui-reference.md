---
title: "FT-XXX: UI Reference Template"
doc_kind: feature-support
doc_function: template
purpose: Governed wrapper template for optional `ui-reference/README.md`. Read when a feature changes interface, navigation, screen states, editor/preview flows, copy/state semantics, or interaction model.
derived_from:
  - ../../../feature-flow.md
  - ../../../../dna/frontmatter.md
status: active
audience: humans_and_agents
template_for: feature-support
template_target_path: ../../../../features/FT-XXX/ui-reference/README.md
canonical_for:
  - feature_support_template_ui_reference
---

# FT-XXX: UI Reference Template

This file describes the wrapper template. The instantiated `ui-reference/README.md` lives below as an embedded contract and is copied without the wrapper frontmatter and history.

## Wrapper Notes

`ui-reference/README.md` does NOT own:

- Product requirements (belongs to `brief.md`)
- Selected architecture (belongs to `design.md`)
- Implementation steps (belongs to `implementation-plan.md`)

Mockups live in `ui-reference/mockups/*.md`. Images, design-tool links, or other versionable/linkable formats are acceptable.

## Instantiated Frontmatter

```yaml
title: "FT-XXX: UI Reference"
doc_kind: feature-support
doc_function: reference
purpose: "Interface reference for FT-XXX: screen map, interaction states, component expectations, and UI traceability."
derived_from:
  - ../brief.md
  # - ../design.md  # add if design.md exists
status: draft
audience: humans_and_agents
```

## Instantiated Body

```markdown
# FT-XXX: UI Reference

## Interface Scope

Which surfaces this reference covers.

| Surface | In scope | Notes |
| --- | --- | --- |
| Public web | yes | |
| Admin panel | no | Out of scope for this feature |

## Screen Map

| Screen ID | Screen name | Entry point | Related requirement |
| --- | --- | --- | --- |
| `UI-01` | Screen name | Route or navigation path | `REQ-01` from `brief.md` |

## Interaction States

| State ID | Screen | State name | Trigger | Visual cue |
| --- | --- | --- | --- | --- |
| `UI-02` | `UI-01` | Loading | API call in flight | Spinner |

## Component Expectations

| Component | Behavior | State dependency |
| --- | --- | --- |
| Submit button | Disabled until form valid | Form validation state |

## Mockups

- [`mockups/main-flow.md`](mockups/main-flow.md) — low-fidelity sketch of the main flow.

## UI Traceability

| UI element | Requirement | Acceptance scenario |
| --- | --- | --- |
| `UI-01` | `REQ-01` | `SC-01` |
```
