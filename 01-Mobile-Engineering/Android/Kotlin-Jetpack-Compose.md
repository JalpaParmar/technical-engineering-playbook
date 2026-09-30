# Kotlin, Jetpack & Compose

## Kotlin
Know null safety, data/sealed classes, extension functions, higher-order functions, generics and coroutines. Kotlin reduces some classes of nullability error but does not make application logic automatically safe.

## Compose mental model
Compose is declarative: state drives UI. Keep business rules outside composables and make state ownership/lifetime deliberate.

Questions:
- where is the source of truth?
- which state survives recreation/process death?
- are side effects tied to the correct lifecycle?
- is recomposition doing unnecessary work?

## ViewModel
A ViewModel is useful for screen-level state and logic that should survive configuration changes. It is not a general dumping ground for repositories, UI widgets and unrelated global state.

## Dependency injection
Hilt/Dagger are common DI approaches; Koin is another ecosystem option. DI helps explicit dependencies/testability, but excessive abstraction can increase cognitive cost.

## Scenario: screen reloads repeatedly
Inspect state ownership, effect keys, lifecycle collection and whether network calls are initiated directly by recomposition rather than a stable state/event boundary.

## Compose review checklist
- [ ] state ownership clear
- [ ] immutable UI state preferred where practical
- [ ] side effects deliberate
- [ ] lifecycle-aware collection
- [ ] expensive work not performed during composition
- [ ] accessibility semantics considered
- [ ] navigation/events do not replay unexpectedly
