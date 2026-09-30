# Mobile Architecture Interview Q&A

## 1. MVVM vs Clean Architecture?
**Short interview answer:** They solve different levels of the problem. MVVM primarily structures presentation/state, while Clean Architecture is about dependency direction and protecting domain policy. They can be used together, but I add layers only when complexity justifies them.

## 2. How do you design an offline-first app?
**Short interview answer:** I begin with product semantics—what can be stale, what can be edited offline and how conflicts should behave. Then I define the source of truth, persistence, synchronization, operation identity/idempotency, retries and user-visible sync state.

## 3. When should a mobile app be modularized?
**Short interview answer:** When meaningful ownership, coupling, testing or build boundaries justify it. I prefer feature/domain boundaries with small public APIs and avoid splitting simply to increase module count.

## 4. Repository pattern—why?
**Short interview answer:** A repository can give the domain/presentation layer a stable data contract while coordinating remote/local sources. It becomes harmful if it is only a pass-through layer with no meaningful boundary.

## 5. How do you choose an architecture?
**Short interview answer:** I start from product complexity, state/data consistency, team size, expected lifetime, testability and change patterns. I prefer the simplest architecture that makes likely changes safe. Pattern names come after constraints.
