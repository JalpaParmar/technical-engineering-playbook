# iOS Interview Q&A

## 1. What is ARC and where can it fail?
**Short interview answer:** ARC automates reference-counted lifetime management for class instances, but it cannot break strong reference cycles automatically. I pay particular attention to closure captures, delegates, observers/timers and long-lived async work.

**Deep dive:** ARC inserts ownership operations based on strong/weak/unowned semantics. A leak is often an ownership-design problem, not “ARC failing.”

**Follow-ups:** weak vs unowned? How would you prove a view controller leaks?

## 2. UIKit or SwiftUI?
**Short interview answer:** I don't treat it as a binary choice. For new UI, SwiftUI can simplify state-driven composition, while UIKit remains mature and may be the right fit for existing complex flows. In a legacy app I usually evaluate incremental interoperability rather than a rewrite.

**Follow-ups:** state ownership? navigation? minimum OS? testing?

## 3. Why actors?
**Short interview answer:** Actors isolate mutable state and help prevent unsynchronized data access. They improve data-race safety, but I still need to reason about logical races, reentrancy, cancellation and ordering.

## 4. How would you implement token refresh?
**Short interview answer:** I centralize authentication behavior, allow one coordinated refresh, queue or retry eligible requests after success, and fail cleanly when refresh is invalid. I avoid each request independently launching refresh.

## 5. How do you design offline support?
**Short interview answer:** I first define the source of truth and product expectations for stale data and offline writes. Then I design cache/persistence, synchronization, conflict behavior, retry and UI states. Offline-first is a product/data-consistency decision, not simply “save API data locally.”

## 6. How do you approach a legacy Objective-C modernization?
**Short interview answer:** I avoid a rewrite-first approach. I identify high-change/high-risk boundaries, protect behavior with tests, create interoperability seams, migrate incrementally, and measure whether change becomes safer and faster.

## 7. What belongs on the main actor?
**Short interview answer:** UI-bound mutable state is a common candidate. I explicitly model isolation rather than assuming async work is automatically off the main thread, and I keep expensive CPU/blocking work away from the UI path.

## 8. How do you investigate a memory leak?
**Short interview answer:** I reproduce the flow, verify expected deallocation, inspect ownership paths using memory/debugging tools, then look for cycles from closures, delegates, observers, timers, tasks or caches. I fix the ownership model and add a regression guard where practical.

## 9. What makes an iOS app architecture “good”?
**Short interview answer:** It should make the product safe to change. I look for clear ownership, boundaries, testability, predictable state/data flow, manageable dependencies and appropriate complexity. The pattern name is secondary.

## 10. What would you review before an App Store release?
**Short interview answer:** Build/signing and production config, critical regression and upgrade paths, API/backward compatibility, feature flags, privacy/security-sensitive changes, observability, rollout and a realistic mitigation/hotfix path.
