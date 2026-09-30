# iOS Hands-On Exercises

Do these without copying the solution first.

## Exercise 1 — Search race
Build a Swift search ViewModel/service where each keystroke can start async work. Prevent stale responses and support cancellation.

**Validate:** deliberately delay older requests longer than newer ones.

## Exercise 2 — Retain cycle
Create a view-controller/service callback cycle, prove deallocation fails, then fix ownership. Explain why the chosen weak/unowned relationship is correct.

## Exercise 3 — Token refresh coordinator
Model multiple concurrent requests receiving unauthorized responses. Ensure only one refresh runs and eligible requests resume.

## Exercise 4 — Offline repository
Implement repository behavior using remote + in-memory/local fake sources. Define stale/read/write semantics explicitly.

## Exercise 5 — UIKit/SwiftUI boundary
Host one SwiftUI feature inside a UIKit navigation flow (or model the boundary if no Xcode environment). Document state/navigation ownership.

## Exercise 6 — Migration reasoning
Design a schema change with N-3 → current upgrade tests and a failure strategy.

## Exercise 7 — Incident drill
Given a crash spike after rollout, write: impact statement, hypotheses, evidence requests, mitigation options, validation and RCA outline.
