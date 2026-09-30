# iOS Persistence — Deep Dive

## Choose by requirement
- **UserDefaults:** small preference-like values, not sensitive structured databases.
- **Keychain:** credentials/secrets appropriate for secure credential storage.
- **Files:** documents/blobs/caches where file semantics fit.
- **Core Data / database layer:** structured persistent models, relationships, queries and migrations.

## Core Data reasoning
Understand managed object contexts, object identity, save boundaries, concurrency rules and migrations. Do not pass managed objects freely across concurrency boundaries without respecting Core Data rules.

## Migration
Production migration planning includes:
1. supported starting versions;
2. model/schema evolution;
3. representative old data;
4. failure/rollback or recovery strategy;
5. storage/time constraints;
6. upgrade-path tests;
7. telemetry.

## Cache vs persistence
A cache may be discardable; durable user-created state may not be. That distinction changes corruption/recovery strategy.

## Scenario
A migration works from version N-1 but users can upgrade from N-4. Test the actual supported upgrade graph rather than only the previous release.
