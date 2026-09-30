# System Design Q&A

**Where do you start?** Requirements and nonfunctional constraints, then explicit assumptions. I do not start by naming databases/microservices.

**How do you estimate scale?** Use provided numbers or clearly labeled assumptions to derive rough requests/storage/bandwidth. Precision is less important than identifying likely constraints.

**Cache?** Only after defining source of truth, freshness/invalidation and failure behavior.

**SQL or NoSQL?** Based on data model, access patterns, transaction/consistency needs, scale and operations—not trend.

**Queue?** Useful for asynchronous decoupling/buffering; account for duplicate/order/replay and monitoring.

**How do you finish?** Revisit bottlenecks, failure modes, security, observability, cost/operations and explain trade-offs/evolution.
