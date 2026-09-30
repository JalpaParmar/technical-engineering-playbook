# Advanced Android Scenarios

## 1. Duplicate API requests after rotation/navigation
Inspect ViewModel ownership, Flow collectors, lifecycle restart behavior, Compose effects and repository sharing.

## 2. ANR during startup
Use traces/profiling to find main-thread blocking: disk, initialization, database, SDK startup or synchronous network-related work.

## 3. Work executes twice
Check unique-work policy, operation idempotency and server-side operation identity. “Exactly once” should not be assumed from mobile scheduling.

## 4. Room migration works on clean install but crashes upgrades
Test actual old-version databases through supported migration paths. Clean install is not a migration test.

## 5. Compose event repeats
Separate durable UI state from one-time event semantics and inspect collection/effect lifecycle.

## 6. Push opens wrong account data
Treat account identity as part of route validation. Never assume notification payload remains valid after logout/account switch.
