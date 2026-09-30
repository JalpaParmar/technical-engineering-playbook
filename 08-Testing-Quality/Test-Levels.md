# Unit, Integration, Contract & UI Testing

**Unit:** isolated behavior/state/rules. **Integration:** real collaboration between selected components. **Contract:** verifies producer/consumer interface assumptions. **UI/E2E:** user journey through broad stack.

Do not force every test into a textbook pyramid. Choose a portfolio that gives fast, trustworthy feedback for the architecture.

## Mobile/API contract
Contract tests can detect schema/behavior drift before mobile clients encounter it, but cannot replace real integration testing.

## Test doubles
Mocks verify interactions; stubs return controlled values; fakes provide lightweight working behavior. Use the simplest double that supports the test intent.
