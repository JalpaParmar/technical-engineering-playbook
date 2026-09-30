# iOS Mobile Security — Defensive Deep Dive

## Threat-model questions
What data is valuable? Who can access the device? What can a malicious client manipulate? Which decisions must the server enforce?

## Principles
- minimize sensitive data on device;
- use platform secure credential storage appropriately;
- keep authorization on trusted server boundaries;
- do not embed long-lived secrets in the app binary;
- redact sensitive logs/analytics;
- validate untrusted deep-link/input data;
- review third-party SDK data collection;
- protect release/signing credentials.

## Certificate pinning
Pinning can reduce certain trust risks but creates operational complexity and outage risk during certificate/key changes. Do not add it automatically; evaluate threat model, rotation and recovery.

## Compromised client assumption
A determined attacker can inspect/modify a client. Therefore client-side flags, hidden screens and local checks cannot protect server-owned authorization.

## Review checklist
- [ ] sensitive data inventory
- [ ] auth/token lifecycle reviewed
- [ ] server authorization verified
- [ ] logs/analytics redacted
- [ ] deep links/input treated untrusted
- [ ] third-party SDK/privacy reviewed
- [ ] signing/secrets protected
