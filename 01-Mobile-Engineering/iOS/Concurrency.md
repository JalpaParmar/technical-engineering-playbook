# iOS Concurrency

## Core model
Concurrency improves responsiveness and throughput but introduces ordering, cancellation, isolation and shared-state risks.

### async/await
Use structured async code to express asynchronous operations without deeply nested callbacks.

```swift
struct UserService {
    let session: URLSession

    func user(id: String) async throws -> User {
        let url = URL(string: "https://example.invalid/users/\(id)")!
        let (data, response) = try await session.data(from: url)
        guard let http = response as? HTTPURLResponse,
              (200..<300).contains(http.statusCode) else {
            throw ServiceError.invalidResponse
        }
        return try JSONDecoder().decode(User.self, from: data)
    }
}
```

The URL is illustrative only.

### Main actor
UI-related mutable state commonly belongs on the main actor. Do not assume every async function automatically runs away from the main thread.

### Actors
Actors help isolate mutable state. They reduce data-race risk but do not eliminate logical races or bad ordering assumptions.

### Cancellation
Cancellation is cooperative. Long operations should notice cancellation and avoid publishing stale results.

## Scenario: search-as-you-type
Risk: response for “sw” arrives after response for “swift” and overwrites newer results.

Approaches:
- cancel prior task;
- track request identity;
- isolate state;
- ensure only latest result can update UI.

## Legacy bridge
When moving callbacks to async/await:
1. preserve error semantics;
2. preserve cancellation where possible;
3. avoid double-resume when using continuations;
4. define actor isolation explicitly;
5. test ordering and failure paths.

## Troubleshooting checklist
- [ ] UI state mutation isolation understood
- [ ] shared mutable state identified
- [ ] cancellation handled
- [ ] stale responses prevented
- [ ] blocking work kept off UI path
- [ ] task lifetime/ownership understood
- [ ] error propagation tested
