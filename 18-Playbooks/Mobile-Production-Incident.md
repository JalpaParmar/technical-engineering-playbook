# Mobile Production Incident Playbook

## Trigger
Crash spike, ANR/freeze, broken critical flow, severe API incompatibility, payment/booking failure, bad rollout or other material production degradation.

## Assess
- affected platform/version/OS/device
- user/business impact
- start time and rollout correlation
- backend vs client evidence
- severity and escalation need

## Stabilize
Possible options depend on system design: pause rollout, disable a feature flag, server-side compatibility mitigation, rollback backend, publish hotfix, communicate workaround. Choose based on evidence and risk.

## Investigate
1. crash/ANR traces and logs
2. release diff and configuration
3. API/error-rate telemetry
4. feature-flag exposure
5. affected cohorts
6. reproduction
7. hypotheses ranked by evidence

## Communicate
State known impact, mitigation, evidence and next checkpoint. Do not present a hypothesis as root cause.

## Validate
Confirm recovery in production signals, not only a developer device.

## RCA
Document timeline, root cause, contributing factors, detection gaps, mitigation, permanent fix and preventive actions. Focus on system improvement rather than blame.
