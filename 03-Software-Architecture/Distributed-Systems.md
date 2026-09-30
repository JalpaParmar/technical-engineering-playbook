# Distributed Systems Fundamentals

Networks fail, latency varies, messages duplicate, clocks differ and partial failure exists.

Understand timeout, retry/backoff/jitter, idempotency, consistency, availability, replication, queues, eventual consistency and correlation IDs.

Retries can amplify outages. Bound attempts, back off/jitter and respect end-to-end latency budgets.

For payments/bookings, stable operation identity helps the server recognize retried intent.

Do not use “eventual consistency” vaguely: define what users may observe and which invariants must remain strong.
