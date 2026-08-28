---
name: trace-api-flow
description: Use when locating an API, proving whether it is used, or mapping an endpoint through DTOs, services, query hooks, and UI consumers. Do not change API behavior unless explicitly requested.
---

# Trace API Flow

Produce a reliable map from contract to runtime consumer.

## Workflow

1. Locate the endpoint definition, HTTP method, path parameters, query parameters, body, and response DTO.
2. Find the service method and any request or response transformation.
3. Find query or mutation hooks, query keys, enablement conditions, invalidation, and caching options.
4. Find every direct and indirect component consumer.
5. Distinguish active runtime calls from exports, dead code, mocks, tests, and generated definitions.
6. Identify pagination, authorization, status filtering, and error behavior that affect completeness.
7. Summarize gaps or the cleanest existing API composition.

## Output

Prefer a compact table with: method and endpoint, service, hook, consumer, trigger, parameters, and confidence.

## Rules

- Do not infer runtime use from a service declaration alone.
- Do not assume one page represents a complete paginated collection.
- Treat API documentation as a contract candidate and verify local integration.
- Keep the task read-only unless implementation is requested.
