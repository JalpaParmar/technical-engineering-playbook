# Backend/API Q&A

**401 vs 403?** Commonly 401 means missing/invalid authentication; 403 means authenticated but not permitted. Document semantics consistently.

**Why idempotency key?** To recognize retried intent where duplicate effects are dangerous.

**SQL vs NoSQL?** Decide from model/access patterns, transactions/consistency, scale and operations.

**Why queue?** Async decoupling/buffering, with duplicate/order/replay costs.

**Mobile API evolution?** Favor additive compatible changes, know supported clients, stage backend first and define deprecation.
