# Queues, Webhooks & Async Integration

Queues provide buffering and temporal decoupling but introduce duplicate/order/retry/poison-message concerns.

Treat webhooks as untrusted, retryable input. Verify authenticity using provider guidance, deduplicate when needed, respond promptly and process asynchronously where appropriate.

Define schema ownership, retry/dead-letter policy, replay behavior and operator tooling.
