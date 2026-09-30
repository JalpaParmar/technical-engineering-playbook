# Mobile Observability

Mobile observability should answer: **who is affected, since when, on which version/device/OS, in which flow, and after which change?**

## Signals
- crashes and non-fatal errors;
- app hangs/performance;
- API latency/error categories;
- feature adoption/funnel events;
- release/version distribution;
- key state transitions;
- feature-flag exposure.

## Logging
Use structured, privacy-aware logs. Include correlation/request identifiers when the backend supports them. Never log secrets merely to make debugging easier.

## Release comparison
Compare new vs previous version by crash-free behavior, critical-flow failures, API errors and performance—not only download/install count.

## TPM/Tech Lead dashboard questions
- Is degradation version-specific?
- Is it platform/OS/device specific?
- Did it begin with mobile release, backend release or config change?
- Is a feature flag cohort affected?
- Can we mitigate without a store release?
