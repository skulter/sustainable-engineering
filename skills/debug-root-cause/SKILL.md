---
name: debug-root-cause
description: Use when diagnosing runtime errors, broken UI, failed requests, intermittent behavior, stale data, or performance symptoms. Do not implement a fix unless the user asks to fix the diagnosed issue.
---

# Debug Root Cause

Explain why the symptom occurs and identify the narrowest reliable correction.

## Workflow

1. Capture the exact symptom, environment, trigger, and expected behavior.
2. Reproduce when possible and record observable evidence.
3. Trace the failing path across inputs, state, rendering, network, and side effects.
4. Form a small set of falsifiable hypotheses.
5. Test the highest-value hypothesis first and eliminate alternatives.
6. Identify the root cause, contributing conditions, and blast radius.
7. Propose the smallest fix and regression validation; implement only when requested.

## Guardrails

- Do not treat correlation, a rerender, or a timeout as proof of cause.
- Do not add retries, delays, remount keys, or effects until the underlying lifecycle is understood.
- Distinguish frontend, backend, contract, environment, and data causes.
- Keep diagnostics reversible and narrowly scoped.
- State what remains unverified.
