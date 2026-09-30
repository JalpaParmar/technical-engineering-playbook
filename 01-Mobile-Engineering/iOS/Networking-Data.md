# Networking & Data

## Network layer responsibilities
A robust client separates request construction, transport, authentication, decoding, error mapping, retry policy and observability.

```text
Feature → Repository → API Client → URLSession
                    ↘ Auth / Retry / Metrics
Feature ← Domain Model ← Decoder / Mapper
```

## Authentication/token refresh
Avoid allowing many failed requests to trigger simultaneous refresh operations. Coordinate refresh, replay only appropriate requests, and define what happens when refresh fails.

## Retry
Retry only when the failure and operation are safe to retry. Consider:
- idempotency;
- network/transient status;
- backoff and jitter;
- maximum attempts;
- user experience;
- cancellation.

Never blindly retry every 4xx/5xx.

## Caching
Define:
- source of truth;
- freshness;
- invalidation;
- stale-while-refresh behavior;
- offline behavior;
- storage limits;
- sensitive-data rules.

## Pagination
Track stable page/cursor state, loading state, end-of-data, duplicates and refresh interactions. Cursor-based pagination can be safer than offset pagination for frequently changing datasets, depending on backend support.

## Persistence
Use the least complex persistence mechanism that satisfies consistency, query, migration and security requirements. Keychain is appropriate for certain secrets/credentials; it is not a general database.

## Data migration checklist
- [ ] upgrade from supported old versions tested
- [ ] migration is deterministic
- [ ] failure strategy defined
- [ ] destructive migration explicitly approved if applicable
- [ ] storage/backup implications considered
- [ ] telemetry can identify migration failures
