---
name: document-decisions-and-flows
description: Use when turning verified code, routes, APIs, or decisions into concise technical documentation, IA, runbooks, or diagrams. Do not document guessed behavior as fact.
---

# Document Decisions And Flows

Create a compact document that helps developers and stakeholders navigate the real system.

## Workflow

1. Define the audience, question, scope, and source date.
2. Collect facts from routes, navigation, handlers, contracts, configuration, and decisions.
3. Separate menu access, in-page actions, deep links, redirects, external transitions, and unreachable routes.
4. Organize information around user or data flow rather than repository file order.
5. Use a table for exact mappings and one focused diagram only when relationships are materially clearer visually.
6. Mark inferred, conditional, deprecated, and physically unreachable paths.
7. End with decisions, gaps, and next actions.

## Guardrails

- Keep every material claim traceable to inspected evidence.
- Avoid duplicate diagrams and decorative detail.
- Use stable labels and include exact route or contract names.
- Keep the main document concise; move exhaustive evidence to an appendix only when needed.
