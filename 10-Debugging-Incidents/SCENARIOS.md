# Incident Scenarios

## DB CPU 100%
Protect service, identify expensive workload/query/release correlation, inspect locks/index/query plans as appropriate, scale only as mitigation if needed, validate recovery.

## Login outage
Check auth provider, API, DB/cache, certificates/secrets/config and recent deployments. Establish whether failure is universal or cohort/region-specific.

## Retry loop overload
Stop amplification first via config/flag/rate control where safe, then fix retry classification/backoff/idempotency.

## Mobile crash spike
Segment by version/OS/device/feature cohort, pause rollout if warranted, inspect symbolicated traces and recent changes, mitigate and monitor.

## Queue backlog
Measure producer/consumer rates, poison messages, downstream latency and capacity. Scaling consumers may worsen a slow downstream dependency.
