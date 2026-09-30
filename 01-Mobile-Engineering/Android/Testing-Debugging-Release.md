# Android Testing, Debugging & Release

## Testing
Prioritize deterministic domain/ViewModel tests, repository integration tests where valuable, and UI tests for critical journeys.

## ANR reasoning
An Application Not Responding condition often points to excessive blocking of the main thread or responsiveness problems. Investigate traces and measured behavior rather than guessing.

## Debugging flow
Impact → device/OS/app version → logs/crash/ANR traces → recent changes → reproduce → isolate → mitigate → fix → regression test → monitor.

## Release checklist
- [ ] version/build configuration correct
- [ ] signing and production endpoints verified
- [ ] min/target SDK implications reviewed
- [ ] critical flows and upgrades tested
- [ ] Room/data migrations tested
- [ ] backend compatibility confirmed
- [ ] feature flags reviewed
- [ ] crash/ANR monitoring ready
- [ ] staged rollout/mitigation approach defined
- [ ] current Play policies verified before release

Platform/store policies and SDK requirements are version-sensitive.
