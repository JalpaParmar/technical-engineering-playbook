# Advanced iOS Scenarios

## 1. Stale search results
**Symptom:** fast typing shows results for an older query.  
**Investigate:** task cancellation, response ordering, state ownership.  
**Design:** cancel superseded work and ensure only current request identity publishes state.

## 2. View controller never deallocates
Inspect closure captures, delegates, timers/observers, Combine subscriptions, tasks and coordinator ownership. Prove the ownership path with tooling rather than adding `weak` randomly.

## 3. API succeeds but UI freezes
Measure decoding/mapping/image/database work and main-actor usage. “API issue” may actually be client CPU/blocking.

## 4. Token expires during 20 concurrent requests
Coordinate a single refresh and replay only eligible requests. Avoid a refresh storm.

## 5. Migration crash after upgrade
Identify old schema/version paths, reproduce upgrade rather than clean install, protect user data, and define mitigation. Add upgrade-path testing to release gates.

## 6. App killed during write
Design important writes/operations so recovery state is known. For server operations, stable operation IDs and reconciliation can prevent accidental duplicates.

## 7. Feature flag disabled after incident
Ensure disabled behavior is safe even if app has cached state or is mid-flow. Feature flags need tested fallback semantics, not only a remote boolean.
