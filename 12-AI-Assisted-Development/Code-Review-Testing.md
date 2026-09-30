# AI Code Review & Testing

## AI review can inspect
Potential logic errors, missing edge cases, concurrency, security smells, test gaps, duplicated logic and documentation.

## Limits
It may invent APIs, misunderstand domain invariants, miss repository context or produce noisy style comments.

## Workflow
Human states review goal/risk → AI reviews diff with context → findings include evidence/path → engineer validates → automated tests/static/security checks → human approval.

Generated tests must assert meaningful behavior, not merely mirror implementation.
