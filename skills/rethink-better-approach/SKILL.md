---
name: rethink-better-approach
description: Use when a working or proposed solution should be reconsidered for simplicity, clarity, or long-term maintainability. Do not trigger for routine implementation without a meaningful design choice.
---

# Rethink Better Approach

Challenge a candidate solution once, using evidence and explicit tradeoffs rather than fashion.

## Workflow

1. Describe the current approach and the problem it solves.
2. Identify concrete costs: hidden coupling, duplicate state, effect-driven synchronization, unclear ownership, compatibility risk, or excessive indirection.
3. Generate alternatives only when they materially improve those costs.
4. Compare options by correctness, readability, change size, migration cost, testability, and reversibility.
5. Recommend the smallest superior option, or explicitly keep the current approach if alternatives are not better.
6. If implementation is requested, change only the selected scope and validate it.

## Guardrails

- Prefer deletion and simplification over new abstraction.
- Do not replace familiar repository conventions merely for theoretical purity.
- Do not optimize for fewer lines at the expense of intent.
- Avoid premature generic APIs and flexibility without a current consumer.
- Separate “must fix now” from “consider later.”

Use [maintainability criteria](../../references/maintainability-criteria.md) for the comparison.
