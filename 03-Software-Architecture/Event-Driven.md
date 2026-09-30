# Event-Driven Architecture

Producers publish facts/events; consumers react asynchronously.

Benefits: time decoupling, fan-out, buffering and independent consumers. Costs: eventual consistency, duplicates/order, schema evolution, debugging and operations.

An **event** says something happened; a **command** requests an action.

Do not assume exactly-once end-to-end. Design consumers for actual delivery semantics.

An outbox-style approach can reduce DB/event dual-write inconsistency by persisting publish intent with the business transaction.
