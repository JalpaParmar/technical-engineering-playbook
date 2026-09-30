# iOS Security & Release

## Defensive security
- use Keychain for appropriate secrets;
- avoid logging tokens/PII;
- validate server trust using platform defaults unless a justified design requires more;
- treat local data as potentially accessible on a compromised device;
- enforce authorization server-side;
- minimize permissions;
- keep dependencies current and reviewed.

Client-side checks are not a substitute for backend authorization.

## Release readiness
### Build
- [ ] version/build number correct
- [ ] production configuration verified
- [ ] signing/provisioning valid
- [ ] debug/test endpoints disabled
- [ ] feature flags reviewed

### Quality
- [ ] critical flows regression-tested
- [ ] upgrade path tested
- [ ] supported OS/device matrix considered
- [ ] accessibility/localization risks reviewed

### Backend/dependencies
- [ ] required APIs deployed and compatible
- [ ] migrations complete/compatible
- [ ] backward compatibility understood
- [ ] third-party dependencies healthy

### Operations
- [ ] crash/analytics monitoring ready
- [ ] rollout strategy defined
- [ ] kill switch/feature flag available where appropriate
- [ ] hotfix/mitigation path understood
- [ ] support/stakeholders know meaningful risks

## Store release
Treat TestFlight/App Store submission, review, phased release and production monitoring as part of delivery—not an afterthought. Store behavior/policies are version-sensitive and should be verified against current Apple guidance.
