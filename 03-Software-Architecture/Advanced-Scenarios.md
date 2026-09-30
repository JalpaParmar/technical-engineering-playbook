# Advanced Architecture Scenarios

## Database becomes bottleneck
Measure query/lock/I/O patterns before introducing new stores. Options may include indexing/query changes, caching, replicas, partitioning or workload redesign.

## Service dependency outage
Bound timeouts, stop retry amplification, isolate resources and degrade noncritical features where possible. Validate recovery through user-facing signals.

## Microservice proposal for a small team
Ask which independent scaling/deployment/ownership problem it solves. A modular monolith may preserve boundaries with lower operational cost.

## Event consumer processes duplicate
Treat delivery semantics as design input. Use operation/event identity and idempotent state transition where appropriate.

## Cache returns stale critical data
Classify which data may be stale. Critical write/availability decisions should revalidate against authoritative state.

## Cross-region design
Clarify latency, residency, disaster recovery and consistency requirements before adding active-active complexity.
