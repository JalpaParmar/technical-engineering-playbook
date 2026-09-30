# Mobile-Friendly API Design

Mobile clients live in unreliable networks and remain installed across backend releases.

## Contract principles
- backward compatibility for supported clients;
- stable error model;
- explicit pagination;
- idempotency for retry-sensitive writes;
- sensible payload size;
- server-authoritative authorization;
- correlation identifiers;
- predictable date/time formats;
- version/deprecation policy.

## Error model
Clients need enough structure to distinguish validation, authentication, authorization, conflict, transient server failure and network absence without parsing human text.

## Compatibility
Prefer additive evolution when practical. Backend rollout normally precedes client dependence on new behavior.

## Mobile latency
Avoid excessively chatty workflows where a screen needs many serial round trips. Consider aggregation carefully, while avoiding giant endpoints that couple unrelated features.

## TPM/API readiness questions
- Is the contract frozen/versioned?
- Are mocks/examples available?
- What old clients remain supported?
- Are errors defined?
- Are write retries safe?
- Is auth/token behavior clear?
- How will API and mobile telemetry correlate?
