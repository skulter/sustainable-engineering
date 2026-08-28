---
name: audit-localization
description: Use when checking or changing user-facing translations, locale dictionaries, status labels, dates, numbers, or language-specific UI. Do not rename code symbols unless the request includes refactoring.
---

# Audit Localization

Ensure every user-visible string is sourced, translated, formatted, and scoped consistently.

## Workflow

1. Identify the application's translation mechanism and the correct domain dictionary.
2. Find all user-facing strings in the requested screen, including modals, tooltips, empty states, validation, buttons, statuses, and accessibility labels.
3. Reuse semantically correct keys; create a new key when existing wording or context differs.
4. Verify every supported locale has the same key shape and appropriate wording.
5. Check interpolation, pluralization, date and number formatting, fallbacks, and server-provided status mapping.
6. Validate the touched dictionaries and render states.

## Guardrails

- Change localization only when that is the requested scope; keep component names and internal keys stable unless necessary.
- Do not hardcode a language-specific fallback.
- Do not coerce translation results solely to silence types.
- Do not reuse a key whose visible meaning differs by screen.
- Preserve product terminology and approved abbreviations.
