# Mobile Release & Mitigation Scenarios

## Reality
A native binary cannot usually be instantly rolled back for every installed user. Mobile “rollback” often means a combination of staged rollout controls, feature flags, backend compatibility, server-side mitigation and hotfix.

## Scenario 1 — Crash in new optional feature
If safely designed, disable via feature flag, halt rollout, investigate, fix/test and resume with monitoring.

## Scenario 2 — New client incompatible with backend
Restore backward-compatible backend behavior where safe or mitigate the client feature. This is why compatibility is a release architecture concern.

## Scenario 3 — Bad local migration
Feature flags may not undo already-migrated local data. Data migration needs its own recovery design and upgrade testing.

## Scenario 4 — Store review delays hotfix
Use operational mitigations if available and safe; communicate that store approval timing is an external dependency.

## Pre-release questions
- What can we disable remotely?
- What cannot be reversed after execution?
- Which backend versions support this client?
- How do we detect impact?
- Who owns the incident decision?
