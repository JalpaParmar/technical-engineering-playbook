# Software Architecture Q&A

**Monolith or microservices?** Choose from domain/team boundaries, scaling/deployment needs, consistency and operational maturity. A modular monolith is often preferable until distribution gives concrete value.

**Eventual consistency?** Different components may temporarily expose different state while converging; define what inconsistency business rules tolerate.

**Why a queue?** Decouple timing, buffer bursts or process asynchronously; account for duplicate/order/replay complexity.

**Prevent cascading failure?** Bound calls, control retries, isolate resources, shed load/degrade gracefully and monitor dependencies.

**ADR?** Context, constraints, alternatives, decision, consequences and revisit triggers for consequential choices.
