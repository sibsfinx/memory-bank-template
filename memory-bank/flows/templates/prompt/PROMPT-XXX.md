---
title: "PROMPT-XXX: Reusable Prompt Name"
doc_kind: prompt
doc_function: template
purpose: Governed wrapper template for a reusable prompt document. Captures the original formulation in frontmatter and the improved prompt in a copyable body block.
derived_from:
  - ../../../dna/governance.md
status: active
audience: humans_and_agents
template_for: prompt
template_target_path: ../../../prompts/PROMPT-XXX-short-name.md
---

# PROMPT-XXX: Reusable Prompt Name

This file describes the wrapper template. The instantiated prompt document lives below as an embedded contract.

## Wrapper Notes

`source_prompt` stores intent and provenance. The body block `prompt` stores the runnable/copyable version. Do not substitute frontmatter for executable prompts or use the body section as a dialogue log.

**Lifecycle:**
1. User formulates a prompt in dialogue.
2. Agent captures the original formulation in `source_prompt`.
3. Agent generates an improved version in the body fenced block.
4. User copies only the body block content for execution.
5. Update the document when substantial changes occur.

**When to create:**
- The prompt will be reused by humans or agents.
- The original formulation needs preservation.
- The prompt becomes part of a workflow.

**When not to create:**
- Single-use prompts for the current dialogue only.
- Content that belongs in engineering/ops/domain directories.

## Instantiated Frontmatter

```yaml
title: "PROMPT-XXX: Prompt Name"
doc_kind: prompt
doc_function: canonical
purpose: "Reusable prompt for [task description]."
derived_from:
  - ../../../dna/governance.md
prompt_kind: task / system / agent / extraction / review / coding
prompt_status: draft / active / archived
source_prompt: |
  Original user formulation goes here, verbatim.
status: draft
audience: humans_and_agents
```

## Instantiated Body

```markdown
# PROMPT-XXX: Prompt Name

## Usage

When to use this prompt and what its boundaries are.

## Prompt

```prompt
<role>
You are a [role description].
</role>

<context>
[Relevant context]
</context>

<task>
[What the model must do]
</task>

<instructions>
1. Step one.
2. Step two.
</instructions>

<constraints>
- Constraint one.
- Constraint two.
</constraints>

<output_format>
[Expected output format]
</output_format>
```

## Variables

| Variable | Required | Description | Example |
| --- | --- | --- | --- |
| `{{variable}}` | yes / no | What it is | Example value |

## Validation Criteria

- [ ] Output satisfies criterion one.
- [ ] Output satisfies criterion two.

## Change History

| Date | Change | Author |
| --- | --- | --- |
| YYYY-MM-DD | Initial draft | |
```
