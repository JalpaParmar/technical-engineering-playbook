# Mobile Architecture Review Checklist

## Product & constraints
- [ ] primary user journeys identified
- [ ] offline/stale-data expectations explicit
- [ ] supported OS/device constraints known
- [ ] security/privacy requirements identified

## State & UI
- [ ] state ownership clear
- [ ] navigation ownership clear
- [ ] one source of truth where appropriate
- [ ] loading/empty/error/offline states modeled

## Data/API
- [ ] repository/data boundaries intentional
- [ ] authentication/token refresh coordinated
- [ ] retry/idempotency considered
- [ ] cache freshness/invalidation defined
- [ ] migrations/version compatibility considered

## Concurrency
- [ ] shared mutable state identified
- [ ] UI isolation respected
- [ ] cancellation/lifecycle handled
- [ ] stale-response/order races considered

## Modularity/testability
- [ ] module responsibilities clear
- [ ] dependency direction intentional
- [ ] critical business logic independently testable
- [ ] abstractions earn their complexity

## Operations
- [ ] analytics/logging/crash signals defined
- [ ] feature flags/kill switches considered
- [ ] release/rollback or mitigation path defined
- [ ] architecture risks documented
