# Android Security & Performance

## Defensive security
Use appropriate platform-backed secure storage/keystore capabilities for cryptographic keys and sensitive credentials. Keep server authorization authoritative, minimize sensitive logs, validate links/intents and review exported components/permissions.

## Performance
Measure:
- startup;
- main-thread blocking/ANRs;
- rendering/jank;
- memory;
- database/query work;
- network;
- background/battery behavior.

## Scenario: slow startup
Inventory synchronous initialization and third-party SDK startup. Move/defer noncritical work only after understanding dependencies and measuring impact.

## Scenario: excessive battery
Investigate polling frequency, wakeups, location, retries, background jobs and network batching. Fix the workload model rather than only micro-optimizing code.

## Checklist
- [ ] exported components intentional
- [ ] permissions minimized
- [ ] sensitive logs removed
- [ ] secure key/credential handling reviewed
- [ ] startup measured
- [ ] ANR traces monitored
- [ ] background work bounded
