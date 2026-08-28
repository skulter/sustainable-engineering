---
name: implement-scoped-change
description: Use when the user asks to implement, fix, or refactor code within an established repository. Do not use for analysis-only, review-only, or broad architecture planning requests.
---

# Implement Scoped Change

Deliver the smallest complete change that satisfies the confirmed requirement and fits the repository.

## Workflow

1. Read repository instructions and inspect the referenced implementation.
2. Confirm current behavior, expected behavior, and explicit non-goals.
3. Reuse existing DTOs, services, hooks, components, utilities, tokens, and conventions.
4. Modify the narrowest responsible layer; preserve unrelated user changes.
5. Cover reachable loading, error, empty, disabled, and pending states when relevant.
6. Run the narrowest useful validation and review the final diff.

## Implementation Rules

- Keep service, server-state, UI-state, and rendering responsibilities separated.
- Avoid speculative abstractions, one-use utilities, unrelated renames, and opportunistic cleanup.
- Match local naming and file organization before introducing a new pattern.
- Do not invent business logic or silently choose among behavior-changing interpretations.
- Do not commit, push, rebase, open a PR, or deploy unless explicitly requested.

Read [maintainability criteria](../../references/maintainability-criteria.md) when the change introduces a new component, hook, service, or shared boundary.
