# Concurrency Fundamentals

Concurrency introduces data races, logical races, deadlocks, starvation, ordering bugs and cancellation/lifetime complexity.

Concepts: mutual exclusion, immutability, message passing, isolation/actors, atomic operations, structured concurrency, backpressure, cancellation and idempotency.

A **data race** is conflicting unsynchronized memory access. A **logical race** can exist even with memory safety—for example an old network response replacing a newer result.

Review: What state is shared? Who mutates it? What ordering is assumed? What if work completes twice/out of order? How is cancellation propagated?
