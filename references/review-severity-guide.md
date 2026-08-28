# Review Severity Guide

Use severity to communicate impact, not stylistic preference.

- Critical: likely data loss, security compromise, outage, or irreversible production damage.
- High: incorrect core behavior, broken authorization, major compatibility failure, or common-path crash.
- Medium: real defect with limited scope, reachable edge-case failure, stale data, or material maintenance risk.
- Low: minor defect, confusing behavior, or localized robustness issue with limited impact.
- Suggestion: optional improvement with no demonstrated correctness or operational risk.

A useful finding includes a reachable scenario, concrete impact, evidence, and a proportionate remediation. Do not inflate severity because a pattern is unfamiliar.
