# Data Stores: SQL, NoSQL & Caching

SQL is strong for relational models, transactions and constraints. NoSQL is a family of document/key-value/wide-column/graph models; choose from access patterns and consistency needs.

Use transactions to protect real invariants. Distributed workflows may require compensation/saga-style reasoning.

For caches define source of truth, invalidation, TTL/freshness, eviction and failure behavior. Redis is useful for several patterns but is not generic performance magic.
