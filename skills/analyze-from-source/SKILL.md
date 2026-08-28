---
name: analyze-from-source
description: Use when an unfamiliar codebase, ticket, specification, design, API, or error must be investigated before deciding implementation scope. Do not use when the exact edit and source file are already unambiguous.
---

# Analyze From Source

Establish an evidence-backed understanding before proposing or changing code.

## Workflow

1. Read the applicable repository instructions and the closest source of truth.
2. Inspect direct evidence first: referenced files, diffs, logs, contracts, DTOs, designs, and existing implementations.
3. Trace only the dependencies and consumers needed to explain the requested behavior.
4. Separate confirmed facts, reasonable inferences, and unresolved questions.
5. State the affected scope, likely risks, and the smallest viable next action.

## Rules

- Keep the investigation read-only unless the user also requests implementation.
- Prefer repository search and direct references over assumptions or generic advice.
- Treat existing business rules and API contracts as authoritative until contradictory evidence appears.
- Ask before editing when ambiguity can materially change behavior.
- Do not broaden the task into unrelated cleanup.

## Output

Return a concise evidence map: current behavior, relevant files or contracts, root constraint, affected scope, and recommended next step.
