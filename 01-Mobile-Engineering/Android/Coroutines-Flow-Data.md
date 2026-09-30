# Coroutines, Flow & Data

## Coroutines
Structured concurrency ties child work to a lifecycle/scope. Understand dispatchers, cancellation, exception propagation and scope ownership.

Avoid `GlobalScope`-style unbounded lifetime for ordinary feature work.

## Flow
Flow models asynchronous streams. For UI, distinguish cold streams from state/event representations and collect with lifecycle awareness.

## Networking
Retrofit commonly describes HTTP APIs while OkHttp provides transport/interceptors. Keep authentication, retries and error mapping intentional.

## Persistence
Room provides an abstraction over SQLite with compile-time query validation and migration support. Migration strategy is a release concern, not only a database concern.

## Background work
Use lifecycle-appropriate mechanisms. WorkManager is intended for deferrable, guaranteed background work under its constraints; it is not a replacement for every coroutine/task.

## Scenario: duplicate API requests
Check:
- multiple collectors;
- repeated UI effects;
- retry interceptors;
- repository sharing/caching;
- lifecycle restart behavior;
- pagination state.

## Data checklist
- [ ] source of truth defined
- [ ] offline/stale behavior defined
- [ ] auth refresh coordinated
- [ ] retries bounded and safe
- [ ] DB migrations tested
- [ ] duplicate writes/requests considered
- [ ] cancellation respected
