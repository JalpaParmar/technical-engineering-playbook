# Feature Flags & API Compatibility

## Why this matters on mobile
Installed clients cannot all be upgraded immediately. Backend changes must coexist with older app versions.

## API evolution
Prefer additive compatible changes where practical. Define deprecation windows and understand minimum supported client versions before removing behavior.

## Feature flags
Useful for staged exposure and mitigation, but they add state combinations.

For every flag define:
- default value;
- target cohort;
- dependencies;
- safe disabled behavior;
- expiry/removal plan;
- telemetry;
- test combinations.

## Scenario
New app sends a new optional field while old app does not. Backend should handle both during the compatibility window. If the field becomes mandatory, rollout sequencing must account for old installed clients.

## Checklist
- [ ] old supported clients tested
- [ ] server tolerates expected request versions
- [ ] flag fallback safe
- [ ] flag dependency/order documented
- [ ] stale cached configuration considered
- [ ] removal date/owner defined
