# Cross-Platform Mobile Concepts

This section compares engineering concerns shared across iOS and Android without pretending the platforms are identical.

## Common concerns
- UI state and lifecycle
- concurrency/cancellation
- networking/auth/retry
- persistence/migrations
- offline sync
- push/deep links
- permissions
- accessibility/localization
- analytics/crash reporting
- feature flags
- testing
- store release and staged rollout

## Translation map
| Concern | iOS examples | Android examples |
|---|---|---|
| declarative UI | SwiftUI | Jetpack Compose |
| async work | Swift concurrency | Kotlin coroutines |
| stream/state tools | Combine/AsyncSequence concepts | Flow |
| local relational persistence | Core Data/SQLite ecosystem | Room/SQLite |
| background work | platform background APIs | WorkManager/platform APIs |

These are conceptual parallels, **not one-to-one API equivalents**.

## TPM/Tech Lead lens
When coordinating both platforms, align on product behavior and API contracts while allowing platform-native implementation choices. “Pixel/code symmetry” should not override platform conventions, accessibility or lifecycle correctness.
