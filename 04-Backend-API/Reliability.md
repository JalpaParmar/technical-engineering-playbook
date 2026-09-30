# API Reliability & Idempotency

Bound remote calls with timeouts. Retry only transient and safe operations, with bounded backoff/jitter where appropriate.

For retry-sensitive writes such as booking/payment, stable idempotency/operation keys can let the server recognize repeated intent.

A client timeout after submit means unknown—not necessarily failed. Reconcile status before issuing a dangerous duplicate operation.
