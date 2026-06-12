---
doc_kind: governance
doc_function: canonical
purpose: Foundational principles of project documentation. Read first.
status: active
---

# Principles

1. **Single Source of Truth (SSoT).** Every fact has exactly one canonical owner. Duplicates are a defect.

2. **Atomicity.** One file — one topic. As content grows, split into sub-files.

3. **Compactness.** Documents must remain readable. When a document expands, split it into separate files.

4. **Progressive Disclosure.** Information flows from high-level overview to deeper details, with links guiding readers downward through the hierarchy.

5. **WHY / WHAT / HOW.** Product requirements and use cases explain *what*; ADRs explain *why* choices were made; implementation plans and code demonstrate *how* execution occurs.

6. **Code vs Documentation Division.** Code manages implementation details; documentation owns intent, rationale, and contracts.

7. **Index-First.** Every document must appear in an index. Orphaned files are defects.

8. **Annotated Links.** Links should clarify what content they point to and justify why readers should follow them.

9. **ADR Separation.** Each architectural decision requires its own dedicated ADR document in a designated section.
