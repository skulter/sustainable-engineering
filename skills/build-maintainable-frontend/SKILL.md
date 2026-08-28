---
name: build-maintainable-frontend
description: Use for React, Next.js, and TypeScript UI work involving components, hooks, server state, forms, or effects. Do not use for backend-only or infrastructure-only changes.
---

# Build Maintainable Frontend

Implement frontend behavior with clear ownership, predictable data flow, and readable components.

## Workflow

1. Identify the source of truth for server data, form data, URL state, and local interaction state.
2. Reuse the repository's component library, design tokens, DTOs, service layer, and query patterns.
3. Keep data fetching in services and query hooks; keep rendering and user interaction in components.
4. Derive values during render when possible. Use effects only to synchronize with external systems.
5. Extract a component or hook when it creates a meaningful responsibility boundary, not merely because code is long.
6. Cover reachable loading, error, empty, disabled, and optimistic or pending states.
7. Validate behavior and inspect rerender-sensitive code when relevant.

## Guardrails

- Do not mirror query data into local state without a concrete editing or lifecycle need.
- Do not use remount keys to repair synchronization unless remounting is the intended product behavior.
- Prefer named handlers when they clarify intent or are reused.
- Keep types close to ownership and reuse existing contract types.
- Keep user-facing text in the established localization mechanism.

Read [frontend state and effects](../../references/frontend-state-and-effects.md).
