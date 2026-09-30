# Android Interview Q&A

## 1. Why Kotlin coroutines?
**Short interview answer:** Coroutines let asynchronous work be expressed sequentially while supporting structured concurrency, cancellation and lifecycle-aware scope design. The key is not just using `suspend`; it is owning scopes and cancellation correctly.

## 2. Flow vs a one-shot suspend function?
**Short interview answer:** I use a suspend function for a single asynchronous result and Flow when values evolve over time. For UI I also think about state/event semantics and lifecycle-aware collection.

## 3. What causes ANRs?
**Short interview answer:** A common cause is the app failing to keep the main thread responsive, for example blocking I/O or expensive work. I use traces/telemetry to establish the actual blocked path rather than assuming.

## 4. Why Room?
**Short interview answer:** Room gives a structured SQLite persistence layer with typed entities/DAOs and migration support. The important architecture questions remain source-of-truth, transaction boundaries, migrations and offline synchronization.

## 5. Compose vs traditional Views?
**Short interview answer:** Compose is declarative and state-driven, which can simplify UI composition. Existing View-based apps can adopt it incrementally. I would decide based on product lifecycle, team capability, platform support and migration cost rather than rewriting by default.

## 6. What does Hilt solve?
**Short interview answer:** Hilt standardizes dependency provisioning/scopes on top of Dagger, helping make dependencies explicit and testable. DI still needs sensible boundaries; adding interfaces/providers everywhere can become unnecessary complexity.

## 7. How would you debug duplicate network calls?
**Short interview answer:** I trace where the request originates and check lifecycle restarts, multiple Flow collectors, recomposition/effects, retry interceptors and repository sharing. I fix the ownership/event problem rather than simply adding a boolean guard.
