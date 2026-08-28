---
name: assess-security-risk
description: Use when code handles authentication, authorization, secrets, untrusted input, uploads, redirects, external requests, or sensitive data. Do not present a full security audit when only a narrow review was performed.
---

# Assess Security Risk

Review the changed trust boundaries and provide actionable, evidence-backed findings.

## Workflow

1. Identify assets, actors, entry points, trust boundaries, and privilege transitions.
2. Trace untrusted data through validation, storage, rendering, logging, and outbound requests.
3. Check authentication, authorization, tenant isolation, secret handling, injection, unsafe redirects, file handling, and sensitive data exposure as relevant.
4. Verify controls at the authoritative server boundary; treat client checks as user experience, not enforcement.
5. Rank findings by exploitability and impact.
6. Recommend the smallest effective mitigation and validation.

## Guardrails

- Keep analysis scoped to inspected code and state coverage limits.
- Do not label theoretical concerns as vulnerabilities without a feasible path.
- Do not expose secrets or sensitive data in diagnostics.
- Do not weaken security controls for convenience.
- Keep review read-only unless fixes are explicitly requested.
