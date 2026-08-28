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

- `analyze-from-source`
- `implement-scoped-change`
- `review-for-humans`
- `rethink-better-approach`
- `debug-root-cause`
- `validate-proportionally`
- `build-maintainable-frontend`
- `trace-api-flow`
- `prepare-git-handoff`

### Specialized workflows

- `design-sustainable-architecture`
- `verify-ui-against-design`
- `audit-localization`
- `assess-security-risk`
- `assess-performance`
- `plan-compatible-migration`
- `prepare-release-safely`
- `document-decisions-and-flows`

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
