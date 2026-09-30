# Mobile Performance Engineering

## Rule: measure first
Performance work starts with a user-visible metric and representative measurement.

## Areas
- cold/warm launch;
- time to interactive/useful content;
- frame/render performance;
- main-thread responsiveness;
- memory;
- network latency/payload;
- decoding;
- database;
- images;
- battery/energy.

## Budget thinking
Teams can define performance budgets for critical journeys and detect regression in CI/telemetry where practical.

## Investigation
```text
Symptom → Metric → Reproduce → Profile → Bottleneck → Change
→ Re-measure → Representative devices → Production validation
```

## Trade-off
Preloading can improve perceived latency but increase launch time, memory/network use and stale data. Optimize the user journey, not one isolated metric.
