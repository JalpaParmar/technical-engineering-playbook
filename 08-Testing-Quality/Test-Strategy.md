# Test Strategy

Start from risk: critical journeys, money/data integrity, complex logic, integration boundaries and historically fragile areas.

Use the cheapest reliable level. Unit tests give fast logic feedback; integration/contract tests validate boundaries; UI/E2E tests protect selected journeys but cost more to run/maintain.

## Risk matrix
High impact + high change/complexity deserves stronger coverage and observability.

## Shift left/right
Prevent/detect early with design review/static/unit/integration checks, and validate production behavior with safe rollout/telemetry. Neither replaces the other.

## TPM questions
What could fail? Which layer catches it? What is not automated? What blocks release? How do we know production is healthy?
