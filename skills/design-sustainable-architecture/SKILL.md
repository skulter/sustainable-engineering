---
name: design-sustainable-architecture
description: Use when planning module boundaries, shared ownership, a cross-cutting refactor, or a system change with multiple consumers. Do not use for a localized fix with an established implementation pattern.
---

# Design Sustainable Architecture

Design an incremental structure that a team can operate and change over time.

## Workflow

1. Identify business capabilities, current boundaries, consumers, and sources of truth.
2. State quality attributes that matter now: reliability, security, performance, operability, compatibility, and developer experience.
3. Map dependency direction, data ownership, public contracts, and failure boundaries.
4. Compare a small number of viable options with migration and operational costs.
5. Prefer the least complex option that preserves clear ownership and future change paths.
6. Define incremental adoption, compatibility, validation, observability, and rollback.
7. Record decisions and rejected alternatives briefly.

## Guardrails

- Do not introduce a service, package, shared layer, event bus, or generic framework without a concrete boundary problem.
- Keep feature-specific code out of shared layers.
- Preserve stable contracts during migration whenever practical.
- Distinguish architecture required now from optional evolution.

Read [enterprise boundary guide](../../references/enterprise-boundary-guide.md) and [maintainability criteria](../../references/maintainability-criteria.md).
