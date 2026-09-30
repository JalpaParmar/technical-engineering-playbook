# Mobile Payment Engineering

Payment flows are high-risk distributed workflows. The client should not be the authority for final payment status.

## Core concerns
- payment intent/order identity;
- idempotency;
- authentication/authorization;
- sensitive-data minimization;
- timeout and ambiguous-result handling;
- retries;
- app termination/backgrounding;
- webhook/server reconciliation;
- duplicate taps/requests;
- receipt/status recovery.

## Ambiguous result
A network timeout after “Pay” does **not** prove failure. The server/payment provider may have processed the charge. Query/reconcile using stable transaction identity before allowing an unsafe retry.

```text
Create intent → Present/collect authorized payment data → Confirm
      ↓                                            ↓
 Stable ID                                  timeout/interrupt
      └──────────────→ Server reconciliation ←────┘
```

## Checklist
- [ ] duplicate submission protected
- [ ] retry semantics defined
- [ ] final status verified server-side
- [ ] sensitive data minimized
- [ ] interrupted-flow recovery defined
- [ ] logs avoid payment secrets
- [ ] observability/reconciliation available

> Actual payment SDK/compliance requirements are provider- and region-specific and must be verified against current official guidance.
