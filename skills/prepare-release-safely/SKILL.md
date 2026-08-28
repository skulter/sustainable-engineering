---
name: prepare-release-safely
description: Use when preparing a deployment or release checklist, rollout plan, or production verification. Do not deploy, publish, or mutate production without explicit authorization.
---

# Prepare Release Safely

Make release readiness, observation, and recovery explicit.

## Workflow

1. Confirm the intended artifact, version, environment, owner, and release scope.
2. Verify required tests, builds, configuration, secrets, migrations, feature flags, and dependency compatibility.
3. Define pre-release checks, deployment order, smoke tests, and user-critical journeys.
4. Define observability: dashboards, logs, alerts, success thresholds, and observation window.
5. Define rollback or roll-forward triggers and exact recovery actions.
6. Record approval dependencies, known risks, and post-release follow-ups.

## Guardrails

- Do not equate a successful build with production readiness.
- Do not claim deployment or smoke-test success without direct evidence.
- Avoid irreversible migrations before compatible application versions are live.
- Keep release actions read-only until the user explicitly authorizes mutation.
- Stop when credentials, approvals, or external coordination are required.
