---
name: validate-proportionally
description: Use after code changes or before handoff to choose and run validation proportional to risk. Do not run repository-wide checks or deployment workflows unless they are necessary and authorized.
---

# Validate Proportionally

Build confidence with the smallest set of checks that can detect likely regressions.

## Workflow

1. Classify change risk by affected behavior, shared surface, data mutation, and deployment impact.
2. Map each material risk to a check.
3. Start with touched-file formatting or static analysis, then focused tests, type checks, builds, or manual verification as justified.
4. Inspect failures before broadening the validation scope.
5. Review the final diff for accidental changes and unresolved markers.
6. Report commands run, outcomes, skipped checks, and residual risk.

## Rules

- Never claim a check passed when it was not run.
- Do not hide pre-existing failures; separate them from regressions introduced by the change.
- Avoid repository-wide validation when a package, file, or test target is sufficient.
- Do not mutate external systems as part of validation without authorization.

Use [risk-based validation](../../references/risk-based-validation.md).
