# Sustainable Engineering

An evidence-first Codex plugin for building software that remains understandable, maintainable, and safe to change.

It packages focused workflows for analysis, implementation, review, debugging, validation, architecture, localization, performance, security, migration, release preparation, and technical documentation.

## Principles

- Start from the closest source of truth.
- Keep changes scoped to the confirmed requirement.
- Prefer existing contracts and conventions over speculative abstractions.
- Review code for human readability as well as correctness.
- Validate in proportion to risk.
- Keep external mutations, Git operations, and deployments explicitly authorized.

## Included skills

### Core workflows

| Skill | Use it when | What it produces |
| --- | --- | --- |
| `analyze-from-source` | A codebase, ticket, design, API, or failure is unfamiliar and the implementation scope is not yet proven. | An evidence map of current behavior, relevant sources, affected scope, risks, and the smallest credible next step. |
| `implement-scoped-change` | The expected behavior is confirmed and code must be implemented, fixed, or refactored. | The smallest complete change that follows repository conventions and preserves unrelated work. |
| `review-for-humans` | A diff, pull request, or implementation needs correctness and maintainability review. | Findings ordered by severity, with impact, evidence, location, and proportionate remediation. |
| `rethink-better-approach` | A working or proposed solution may contain unnecessary state, effects, coupling, or abstraction. | A tradeoff-based comparison that recommends a simpler alternative—or keeps the current design when it is already better. |
| `debug-root-cause` | Runtime errors, broken UI, failed requests, stale data, or intermittent behavior must be diagnosed. | A reproducible explanation of the root cause, contributing conditions, blast radius, and regression strategy. |
| `validate-proportionally` | A change is ready for verification or handoff. | A risk-mapped validation record containing checks run, outcomes, skipped checks, and residual risk. |
| `build-maintainable-frontend` | React, Next.js, or TypeScript UI work involves components, hooks, server state, forms, or effects. | A frontend implementation with explicit state ownership, predictable data flow, and complete reachable UI states. |
| `trace-api-flow` | An endpoint must be located, proven active, or traced to every runtime consumer. | A contract-to-UI map covering method, endpoint, DTO, service, query hook, cache behavior, trigger, and consumer. |
| `prepare-git-handoff` | A commit message, PR body, change summary, or explicitly authorized Git handoff is needed. | A focused handoff based on the actual diff, repository history, and validation evidence. |

### Specialized workflows

| Skill | Use it when | What it produces |
| --- | --- | --- |
| `design-sustainable-architecture` | A change crosses modules, introduces shared ownership, or requires new system boundaries. | An incremental architecture with clear data ownership, dependency direction, compatibility, observability, and rollback. |
| `verify-ui-against-design` | UI must be implemented or reviewed against Figma, screenshots, tokens, or a component system. | A state-aware visual comparison and scoped implementation that preserves design-system reuse and accessibility. |
| `audit-localization` | User-facing text, translation keys, locale dictionaries, status labels, or formatting may be incomplete. | A locale-consistent mapping of visible strings, keys, interpolation, pluralization, and formatting behavior. |
| `assess-security-risk` | Code crosses authentication, authorization, secrets, untrusted input, uploads, redirects, or sensitive-data boundaries. | Scoped security findings ranked by exploitability and impact, with authoritative-boundary mitigations. |
| `assess-performance` | Rendering, requests, bundles, computation, or data volume creates measurable latency or scalability concerns. | A measured bottleneck analysis and the smallest optimization that improves the same baseline without hiding behavior. |
| `plan-compatible-migration` | Routes, packages, modules, APIs, configuration keys, or persisted contracts must be renamed or replaced. | A staged migration covering consumers, compatibility aliases, telemetry, rollback, and eventual cleanup. |
| `prepare-release-safely` | A deployment, rollout, or production verification plan is required. | A release checklist with prerequisites, smoke tests, observation signals, success thresholds, and recovery triggers. |
| `document-decisions-and-flows` | Verified routes, APIs, decisions, IA, or operational flows must be documented. | A concise, traceable document using tables and focused diagrams only where they materially improve understanding. |

### Shared decision references

The plugin also includes compact reference guides that relevant skills load only when needed:

- **Maintainability criteria** — intent, ownership, coupling, contracts, testability, operations, and deletion.
- **Enterprise boundary guide** — dependency direction and responsibility across routes, services, hooks, UI, domain, and shared layers.
- **Frontend state and effects** — ownership rules for server, URL, form, local, derived, and externally synchronized state.
- **Risk-based validation** — the narrowest useful checks for each change category.
- **Review severity guide** — impact-based definitions for critical, high, medium, low, and optional findings.

### Typical combinations

- New feature: `analyze-from-source` → `implement-scoped-change` → `validate-proportionally` → `prepare-git-handoff`
- Production bug: `debug-root-cause` → `implement-scoped-change` → `validate-proportionally`
- Existing solution cleanup: `review-for-humans` → `rethink-better-approach` → `implement-scoped-change`
- API investigation: `trace-api-flow` → `document-decisions-and-flows`
- Cross-cutting rename: `design-sustainable-architecture` → `plan-compatible-migration` → `prepare-release-safely`

## Install

Add this repository as a Codex marketplace:

```bash
codex plugin marketplace add skulter/sustainable-engineering
```

Install and enable the plugin:

```bash
codex plugin add sustainable-engineering@sustainable-engineering
```

Start a new Codex thread after installation so the new skills are available.

## Use

Codex can select a skill automatically when the task matches its description. You can also invoke one explicitly:

```text
$review-for-humans Review this diff for correctness and maintainability.
$trace-api-flow Trace this endpoint to every runtime consumer.
$rethink-better-approach Reconsider this implementation and recommend a simpler approach.
```

Repository-specific instructions and the closest implementation source remain authoritative over this plugin's general guidance.

## 한국어 요약

코드 분석부터 구현, 검수, 디버깅, 검증, 배포 준비까지 근거와 범위를 우선하며 사람이 지속적으로 관리할 수 있는 코드 구조를 지향하는 개인용 Codex 플러그인입니다.
