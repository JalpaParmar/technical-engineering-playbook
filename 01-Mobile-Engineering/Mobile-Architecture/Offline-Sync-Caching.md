# Offline, Synchronization & Caching

## Start with product semantics
Before choosing a database, answer:
- can users read stale data?
- can they create/update offline?
- what happens on conflicting edits?
- what must be strongly current?
- what data is sensitive?
- how long can queued operations remain?

## Source of truth
Choose deliberately. A common offline-first design makes local persistence the UI-facing source and synchronizes remote changes into it, but this is not mandatory for every product.

## Sync
Track operation identity, ordering, retryability and server acknowledgement. Idempotency support is especially valuable for retrying writes.

## Conflict strategies
Possible approaches include server-wins, client-wins, field-level merge, version checking or explicit user resolution. The correct choice is a business/data decision.

## Cache invalidation
Define freshness/TTL, event-driven invalidation where available, manual refresh, stale display and storage limits.

## Failure scenario
User submits an appointment change offline, app retries after reconnect, response is lost, then retry occurs again. Without idempotency/operation identity, duplicate server-side actions may occur.

## Checklist
- [ ] source of truth explicit
- [ ] stale-data UX defined
- [ ] offline-write policy defined
- [ ] conflict behavior defined
- [ ] retries idempotent or otherwise safe
- [ ] sync observable
- [ ] storage/security policy defined
