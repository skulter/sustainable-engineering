# Enterprise Boundary Guide

Use boundaries to express ownership, not ceremony.

## Typical Application Flow

- Route or controller: transport, authentication context, input boundary
- Service: request execution, external contract, transformation
- Query or mutation hook: cache key, lifecycle, invalidation
- Component: rendering and user interaction
- Domain module: business rules independent from transport and UI
- Shared module: feature-agnostic primitives with stable consumers

## Dependency Rules

- Depend inward on stable contracts.
- Keep shared layers independent from feature layers.
- Keep authorization at authoritative server boundaries.
- Avoid duplicating DTO or domain shapes in consumers.
- Expose the smallest public surface required by current consumers.
- Add compatibility at the boundary when contracts migrate.

Introduce a new boundary only when it clarifies ownership, isolates change, or protects a contract.
