---
name: verify-ui-against-design
description: Use when implementing or reviewing UI against Figma, screenshots, design tokens, or an existing component system. Do not use when no visual or interaction source of truth is available.
---

# Verify UI Against Design

Match the design while preserving reusable UI patterns and accessible behavior.

## Workflow

1. Inspect the exact design node, screenshot, state, viewport, and interaction notes.
2. Inspect existing components, tokens, typography, icons, and nearby screens before creating UI.
3. Compare structure, alignment, sizing, spacing, typography, colors, borders, elevation, overflow, and responsive behavior.
4. Verify interactive, loading, empty, error, disabled, hover, focus, and expanded states.
5. Reuse the design system when it can reproduce the design; add scoped styling only for genuine gaps.
6. Validate in the target runtime and compare again at the intended viewport.

## Guardrails

- Do not infer dimensions from a partial screenshot when inspectable design data exists.
- Do not revive removed UI or functionality merely because a neighboring design contains it.
- Avoid arbitrary values when an existing token or component variant matches.
- Preserve keyboard access, focus visibility, labels, contrast, and reduced-motion expectations.
- Report any deliberate deviation and its reason.
