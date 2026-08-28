---
name: review-for-humans
description: Use when reviewing a diff, pull request, or implementation for correctness, maintainability, and human readability. Do not modify code unless the user separately asks for fixes.
---

# Review For Humans

Review code as production software that another developer must safely understand and maintain.

## Workflow

1. Read repository rules, the diff, and enough surrounding code to understand intent.
2. Verify behavior against the closest requirement, contract, or existing convention.
3. Check correctness, state transitions, error handling, compatibility, and test coverage.
4. Check responsibility boundaries, naming, control flow, duplication, and cognitive load.
5. Distinguish defects from optional improvements.

## Finding Format

Lead with findings ordered by severity. For each finding include:

- severity and concrete impact
- exact file and line
- evidence or failure scenario
- smallest credible remediation

If no material issue exists, say so and identify remaining validation or uncertainty.

## Rules

- Do not report formatter-only preferences as defects.
- Do not call code “best practice” or “bad” without explaining the operational cost.
- Do not recommend abstraction solely to reduce line count.
- Preserve repository conventions unless they create a demonstrated risk.
- Keep review read-only.

Use [review severity guide](../../references/review-severity-guide.md) and [maintainability criteria](../../references/maintainability-criteria.md).
