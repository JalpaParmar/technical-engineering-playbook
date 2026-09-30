# Flaky Tests & Testability

Flaky tests destroy trust and slow delivery.

Common causes: uncontrolled time, randomness, async races, shared state, network/environment dependency, order dependence and fragile UI selectors.

## Treatment
Reproduce, classify, fix ownership/synchronization/environment, quarantine only with owner/expiry when necessary, and track recurrence.

## Testability
Explicit dependencies, deterministic clocks/IDs, clear state machines and small boundaries often improve both design and tests.
