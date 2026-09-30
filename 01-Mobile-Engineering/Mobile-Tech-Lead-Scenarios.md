# Mobile Tech Lead Scenarios

Use these to practice decisions, not memorized definitions.

## Scenario 1 — iOS and Android disagree on API behavior
1. Establish product/API contract and examples.
2. Determine whether the difference is platform convention or contract ambiguity.
3. Align backend semantics first.
4. Allow platform-native implementation where behavior remains equivalent.
5. Add contract/acceptance tests for the disputed cases.

**Interview signal:** cross-team technical leadership without forcing identical implementation.

## Scenario 2 — Backend API will miss sprint commitment
Assess affected stories and critical path. Agree API contract early, use mocks/stubs where safe, parallelize client work, track integration risk, and avoid calling the feature “done” until real integration is validated.

## Scenario 3 — Crash spike after phased rollout
Pause/limit rollout if impact warrants it, segment crash data by version/device/flow, correlate changes and flags, choose mitigation, validate recovery, then complete RCA.

## Scenario 4 — Team proposes full legacy rewrite
Ask for measurable problems, business horizon, migration risk, test coverage, parallel-development cost and incremental alternatives. A rewrite must earn its risk.

## Scenario 5 — Platform teams use different architecture patterns
Do not standardize pattern names merely for governance. Standardize contracts, quality gates, observability, security and product behavior; let platform architecture reflect ecosystem/team constraints when justified.

## Scenario 6 — Senior engineer and product disagree on technical debt
Translate debt into delivery/quality risk: defect probability, change lead time, unsupported dependency, incident exposure or blocked roadmap. Prioritize debt based on business impact rather than “clean code” alone.

## Scenario 7 — Store review blocks urgent release
Separate what can be mitigated server-side/feature-flagged from what requires a client release. Communicate store-review uncertainty explicitly and maintain a tested operational mitigation path for critical features.
