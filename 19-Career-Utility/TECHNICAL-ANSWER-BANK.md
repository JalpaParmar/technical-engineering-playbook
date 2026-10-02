# Technical Interview Answer Bank

## SOLID?
Design heuristics for coupling/changeability, not rigid rules. Apply where real variation/ownership benefits.

## Composition vs inheritance?
Prefer composition for flexible behavior/lower coupling; inheritance for genuine stable substitutable relationships.

## Monolith vs microservices?
Choose from domain/team boundaries, independent scaling/deployment, consistency and operational maturity. Distribution must earn its complexity.

## Idempotency?
Stable operation identity lets retries avoid duplicate business effects—critical for payments/bookings.

## Eventual consistency?
Components may temporarily expose different state while converging; define which user/business invariants can tolerate it.

## Queue?
Temporal decoupling/buffering/async processing, with duplicate/order/replay/operational costs.

## SQL vs NoSQL?
Data model, access patterns, transactions/consistency, scale and operations—not fashion.

## Cache?
Define source of truth, freshness/invalidation and failure behavior first.

## Authentication vs authorization?
Who are you versus may you perform this action on this resource; authorization belongs on trusted server boundaries.

## API compatibility for mobile?
Favor additive evolution, know supported clients, stage backend before client dependency, test old/new versions and define deprecation.

## MVVM?
Separates view rendering from presentation/state logic; useful when it improves testability/changeability, not because every screen needs layers.

## ARC retain cycle?
Strong references can keep objects alive cyclically; reason about ownership and use weak/unowned only when lifetime semantics justify it.

## async/await / actors?
Structured concurrency improves lifecycle/cancellation; actors isolate mutable state, but logical races such as stale results still require design.

## Offline-first?
Define source of truth, freshness, write/conflict semantics, synchronization and user-visible states before choosing storage.

## Mobile rollback?
Often mitigation: stop staged rollout, flag off, restore backend compatibility and hotfix; installed binaries cannot simply be recalled.

## Functions vs App Service?
Event-driven/serverless versus continuously hosted web/API workloads; choose from workload, scaling and operations.

## Blue/green vs canary?
Environment switch versus gradual traffic exposure; both require data/schema/state planning.

## Threat modeling?
Map assets, trust boundaries, realistic threats and controls before incidents expose gaps.

## Logs vs metrics vs traces?
Discrete context, aggregate behavior and request path/timing; combine based on diagnostic question.

## RAG?
Retrieve relevant external knowledge into model context; evaluate retrieval separately from generation and enforce authorization before retrieval.

## RAG vs fine-tuning?
RAG supplies runtime knowledge; fine-tuning changes model behavior/weights for suitable tasks. Different problems.

## Agent vs workflow?
Use agents when dynamic iterative planning/tool selection adds value; deterministic workflows for known predictable steps.

## AI evaluation?
Representative task set + deterministic checks/human rubric/calibrated graders where appropriate + production feedback.

## Safe AI coding?
Bound scope, require diffs/evidence, run deterministic tests/static/security checks and keep humans accountable for architecture/release.
