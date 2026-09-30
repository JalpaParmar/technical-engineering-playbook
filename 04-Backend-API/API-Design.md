# API Design & Compatibility

Define schema, structured errors, pagination, dates/times, nullability, limits and compatibility policy.

Offset pagination is simple but can shift as data changes; cursor pagination can be more stable for suitable ordered datasets.

Favor compatible additive evolution where practical. Define deprecation/support windows. API readiness includes contract/examples, auth, errors, mocks, compatibility, test data and observability.
