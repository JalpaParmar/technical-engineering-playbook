# Android Hands-On Exercises

## Exercise 1 — Compose duplicate request
Create a deliberately incorrect composable that triggers work during recomposition, then move operation ownership to an appropriate state/effect boundary.

## Exercise 2 — Flow lifecycle
Expose repository state through Flow and collect it lifecycle-aware. Explain cold vs state-like stream behavior.

## Exercise 3 — Coroutine cancellation
Start a long-running request from a ViewModel, cancel/replace it, and verify stale state is not published.

## Exercise 4 — Room migration
Create a schema evolution and test migration from an older database version rather than only clean install.

## Exercise 5 — WorkManager/idempotency
Model a retryable background sync and ensure repeating the operation does not duplicate server-side intent.

## Exercise 6 — ANR drill
Given a trace showing main-thread disk/SDK initialization, propose mitigation, measurement and regression monitoring.
