# Contributing

Help build a copilot that is useful during incidents without taking control away from incident responders.

## Before contributing

1. Read `README.md`, `docs/architecture.md`, and `docs/evaluation.md`.
2. Keep proposals focused on a single, reviewable outcome.
3. Explain how the change preserves evidence, citations, confidence, and human approval.

## Contribution principles

- Treat source material as evidence: preserve provenance and avoid unsupported conclusions.
- Keep production actions human-approved and explicit.
- Use sanitized fixtures; never commit secrets, credentials, customer data, or raw production incident exports.
- Prefer small, reversible changes with focused tests when implementation begins.
- Keep documentation English-first, concise, and aligned with the MVP scope.

## Changes to review

Every implementation change should identify:

- the input evidence and expected citations;
- confidence behavior, including what happens when evidence is insufficient;
- the proposed steps and their safety constraints;
- tests or evaluation cases; and
- the rollback boundary.

## Commit guidance

Use Conventional Commit messages. Keep code, tests, and the documentation that explains one behavior in the same work unit.

Examples:

```text
feat(ingestion): preserve document provenance
fix(retrieval): reject answers without citations
docs(evaluation): define groundedness rubric
```

## Reporting concerns

Do not place sensitive incident details in public issues, commits, or fixtures. If a contribution could weaken the safety boundaries, pause the change and raise the concern with the repository maintainers.
