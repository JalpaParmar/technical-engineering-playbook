# Android Lifecycle & State

## Core idea
Activities/composables are not durable business-state containers. Configuration changes, navigation and process death require explicit state ownership.

## Layers of state
- transient UI state;
- ViewModel/screen state;
- saved/restorable state where appropriate;
- persistent local data;
- authoritative server state.

## ViewModel
Useful for screen state across configuration changes, but process death requires restoration/persistence strategy for state that truly matters.

## Compose
Recomposition is normal. Side effects and expensive work must not be accidentally coupled to arbitrary recomposition.

## Scenario
A booking screen is recreated after rotation. The app must not resubmit the booking merely because UI composition/lifecycle restarts. Submission should be modeled as an explicit operation with stable state/identity.

## Interview answer
**How do you handle lifecycle complexity?**  
I separate UI rendering from operation ownership and durable state. ViewModel/state holders survive normal UI recreation, while critical state is persisted or reconciled with the server. Side effects are lifecycle-aware and idempotent where necessary.
