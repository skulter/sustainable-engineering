---
name: prepare-git-handoff
description: Use when preparing a commit message, pull request body, change summary, or explicitly requested Git handoff. Do not commit, push, rebase, merge, or open a PR without explicit authorization.
---

# Prepare Git Handoff

Create a focused, evidence-backed handoff that matches repository history and conventions.

## Workflow

1. Inspect repository status, the relevant diff, and recent commit or PR style.
2. Separate requested changes from unrelated working-tree changes.
3. Summarize user-visible behavior, implementation boundaries, and validation performed.
4. Draft a commit message in the repository's required language and format.
5. Draft a PR body with summary, key changes, verification, screenshots when relevant, risks, and follow-ups.
6. If a Git mutation is explicitly requested, operate only on confirmed files and verify the resulting state.

## Guardrails

- Never include unrelated files in staging or a commit.
- Do not invent test results, ticket details, or deployment status.
- Do not rewrite history or push unless the user explicitly requests it.
- Keep one commit focused on one coherent change when practical.
