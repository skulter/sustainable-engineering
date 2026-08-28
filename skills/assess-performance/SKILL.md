---
name: assess-performance
description: Use when investigating slow rendering, excessive requests, large bundles, expensive computation, or scalability concerns. Do not optimize based only on intuition when measurement is possible.
---

# Assess Performance

Find the dominant cost, verify its cause, and optimize without obscuring the code.

## Workflow

1. Define the user-visible metric or capacity limit and establish a baseline.
2. Measure the relevant path: network waterfall, API latency, query count, render count, CPU, memory, bundle size, or long tasks.
3. Trace the dominant cost to data volume, scheduling, serialization, rendering, caching, or algorithmic work.
4. Evaluate the smallest interventions and their correctness tradeoffs.
5. Implement only when requested, then compare against the same baseline.
6. Record gains, regressions, and remaining limits.

## Guardrails

- Do not add memoization, virtualization, concurrency, caching, or pagination without a demonstrated need.
- Include cache invalidation and stale-data behavior in performance decisions.
- Preserve deterministic behavior and readability.
- Distinguish development-mode artifacts from production behavior.
