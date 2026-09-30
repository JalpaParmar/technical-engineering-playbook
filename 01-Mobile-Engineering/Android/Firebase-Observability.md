# Firebase & Android Observability

Firebase is an ecosystem, not a single architecture decision. Possible capabilities include crash reporting, analytics, messaging, remote configuration and other services.

## Architecture questions
- Which capability is actually needed?
- What data leaves the app?
- What privacy/consent rules apply?
- Is vendor coupling acceptable?
- What is the fallback if the service is unavailable?
- Are environments separated correctly?

## Crash/ANR monitoring
Segment by app version, Android version, device family, rollout cohort and feature exposure. A stack trace without release/context data is often insufficient.

## Remote configuration / feature flags
Use typed/default local values, define safe failure behavior and avoid putting authorization/security policy solely in remote client configuration.

## Messaging
Treat notification delivery as best-effort. Resolve current server state for important workflows.

> Product capabilities, SDK APIs and platform requirements are version-sensitive; verify current official Firebase/Android documentation before implementation.
