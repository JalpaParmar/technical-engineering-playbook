# Push Notifications, Deep Links & Background Work

## Push notifications
Treat push as an unreliable delivery signal, not guaranteed message transport. The server remains the source of truth for important business state.

Design for:
- device-token lifecycle and refresh;
- permission state;
- foreground/background presentation;
- notification routing;
- duplicate/stale notifications;
- user/account switching;
- analytics without leaking sensitive data.

## Deep links / universal links
A robust router validates the route, authentication state, required data and whether navigation can be performed from the current UI state.

```text
Incoming URL → Parse/Validate → Auth Gate → Resolve Data → Navigate → Measure
```

Never trust deep-link parameters as authorization.

## Background execution
Mobile OSes control background opportunities. Design work to be resumable, idempotent and tolerant of interruption rather than assuming unlimited execution time.

## Scenario
A push opens an appointment that was cancelled after the push was sent.

Correct behavior: treat the notification payload as navigation context, fetch/resolve current state, and render the current business truth rather than blindly displaying stale payload data.

## Review checklist
- [ ] token lifecycle handled
- [ ] permission-denied UX defined
- [ ] route validation implemented
- [ ] auth/account boundary respected
- [ ] stale/deleted target handled
- [ ] background task resumable
- [ ] duplicate processing safe
