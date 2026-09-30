# Senior Mobile Engineering Q&A

## How do you prevent duplicate distributed operations?
Use stable operation identity/idempotency where supported, explicit client state, bounded retries and server reconciliation. A disabled button alone is not sufficient.

## What is the biggest risk in offline-first?
Usually not storage—it is defining truth, conflict semantics and synchronization under partial failure.

## How do you review a mobile API?
I review compatibility, auth, errors, retry/idempotency, pagination, payload/latency, time semantics and observability, plus how old installed clients behave.

## What makes a good feature flag?
Safe defaults, explicit cohort, observability, tested on/off behavior, dependency awareness and an expiry/removal owner.

## How do you decide whether to cache?
Start with product freshness/offline/latency needs. Define invalidation and source of truth before choosing technology.

## What is a mobile rollback?
Often mitigation rather than literal binary rollback: stop staged rollout, disable features, restore backend compatibility, use server-side mitigation and ship a hotfix.

## How do you manage cross-platform technical consistency?
Standardize behavior/contracts/quality/security/telemetry. Do not force identical framework patterns when platform-native choices differ.

## How do you balance architecture and delivery speed?
Architecture should reduce expected cost/risk of change. I add structure where likely complexity justifies it and avoid speculative layers.

## How do you communicate a technical risk as TPM?
State trigger, probability/uncertainty, impact, evidence, owner, mitigation, decision deadline and effect on scope/timeline—without presenting hypotheses as facts.

## How do AI coding tools change mobile engineering?
They can accelerate code understanding, test generation, migration planning and review, but generated platform APIs/version assumptions must be verified and security/architecture decisions remain human-owned.
