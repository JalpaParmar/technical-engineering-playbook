# Automation & Quality Gates

Automate repeatable high-signal checks: compile/build, lint/static analysis, unit/integration tests, security/dependency checks and selected performance/contract checks.

A gate should have a clear risk rationale. Too many slow/flaky gates train teams to bypass CI.

## Release gate examples
- critical tests green;
- no unresolved release-blocking defects;
- migration/upgrade tested;
- security findings dispositioned;
- observability ready;
- rollback/mitigation defined.

Never treat coverage percentage alone as quality.
