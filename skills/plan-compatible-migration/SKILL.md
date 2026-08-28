---
name: plan-compatible-migration
description: Use when renaming routes, packages, modules, APIs, configuration keys, or persisted contracts while existing consumers may remain. Do not use for an isolated internal rename with no compatibility surface.
---

# Plan Compatible Migration

Change an externally visible name or contract without stranding existing consumers.

## Workflow

1. Inventory the old identifier across runtime routes, links, imports, packages, scripts, lockfiles, CI, deployment, monitoring, documentation, and external integrations.
2. Classify each occurrence as public contract, internal implementation, generated artifact, or historical text.
3. Define the new canonical contract and a compatibility mechanism such as redirect, rewrite, alias, adapter, or dual read.
4. Sequence changes so producers and consumers remain compatible.
5. Define telemetry, deprecation criteria, rollback, and removal timing.
6. Validate old and new paths plus representative deep links and deployment artifacts.

## Guardrails

- Do not perform a global text replacement without classifying occurrences.
- Preserve stable identifiers that do not need to match product branding.
- Coordinate backend, infrastructure, and external consumers when their contract changes.
- Make irreversible cleanup a later step after compatibility is proven.

Read [enterprise boundary guide](../../references/enterprise-boundary-guide.md).
