---
title: Frontend Engineering
doc_kind: engineering
doc_function: canonical
purpose: UI surfaces, frontend stack, component boundaries, design system integration, and i18n layer.
derived_from:
  - ../dna/governance.md
  - ../product/context.md
status: active
audience: humans_and_agents
---

# Frontend Engineering

This document captures the actual UI surfaces of the project and establishes an engineering contract. It does not repeat product-level principles (in `product/vision.md`) or domain language rules (in `domain/`).

## UI Surfaces

| Surface | Code location | Stack | Backend integration | Design ownership |
| --- | --- | --- | --- | --- |
| Public web | `apps/web/` | React / Next.js | REST API | Design system |
| Internal backoffice | `apps/admin/` | React | GraphQL | Ad-hoc |
| Mobile app | — | — | — | — |

## Component And Styling Rules

- Where the shared component library lives.
- When to create a new ad-hoc UI element vs. using the design system.
- Theme token ownership.
- New UI elements should first look for a place in the shared component library.

## Interaction Patterns

Document the canonical approach for interactivity (server-rendered, SPA, islands, or other paradigm). Do not mix patterns without explicit justification.

## Localization

- Where translations are sourced and stored.
- How they are integrated (i18n library, server-side, etc.).
- Caching strategy.
- How new translation keys are added.
- Fallback behavior ownership.
- If multiple translation sources exist, establish priority and merge order.
