# Epics, Features, Stories & Acceptance Criteria

## Decomposition
Outcome/problem → epic/capability → feature slices → user stories/tasks. Decompose around independently valuable/testable behavior rather than technical layers alone.

## Story
A story communicates user/business behavior, not every implementation detail.

## Acceptance criteria
Make behavior observable and testable. Include permissions, errors, empty states and important edge cases where relevant.

### Example
**Given** an authenticated user with booking permission  
**When** they submit an available slot  
**Then** the server confirms one booking and the client displays the authoritative result.

Add retry/idempotency behavior separately when required.

## Definition boundaries
Acceptance criteria describe product acceptance. Engineering quality gates, architecture and release readiness belong in their appropriate standards too.
