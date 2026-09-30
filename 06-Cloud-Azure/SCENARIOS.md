# Azure Architecture Scenarios

**Function floods downstream:** control concurrency/rate, buffer if appropriate, prevent retry amplification.

**Secret expires:** prefer managed identity where possible; otherwise monitor/test rotation.

**DB CPU spike:** correlate query/load/release; scaling may mitigate while query/index/contention investigation continues.

**Region outage requirement:** clarify RTO/RPO before multi-region complexity; test failover, routing, data consistency and ownership.
