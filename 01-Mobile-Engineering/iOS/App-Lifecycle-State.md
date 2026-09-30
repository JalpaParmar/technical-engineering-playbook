# iOS App Lifecycle & State

## Why it matters
Mobile apps are interrupted, backgrounded, terminated and relaunched. Correctness cannot depend on a screen staying alive.

## State categories
- **ephemeral UI state:** selection, animation, temporary input;
- **screen/domain state:** data required to render a feature;
- **durable local state:** data intentionally persisted;
- **server state:** authoritative business state for server-owned workflows.

Choose persistence/lifetime deliberately.

## Scene/app transitions
Understand active/inactive/background transitions and scene-based lifecycle. Avoid assuming background time is unlimited. Save only state that must survive and can be restored safely.

## Restoration questions
- What if the OS kills the app after backgrounding?
- What if the account changes before restoration?
- Is cached navigation still valid?
- Does the server object still exist?
- Could restoring a pending action duplicate it?

## Scenario: checkout interrupted
Do not treat a locally remembered “submitted” flag as proof of server completion. Restore the stable transaction/order identity and reconcile authoritative status.

## Interview answer
**How do you design for app termination?**  
I separate ephemeral UI state from durable business state. Critical server operations get stable identity and reconciliation. On relaunch I reconstruct from persisted/server truth instead of assuming the previous screen lifecycle completed.
