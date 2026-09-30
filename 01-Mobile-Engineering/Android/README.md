# Android Engineering — Strong Working / Architecture Track

The objective is strong technical collaboration and architecture knowledge without implying unverified years of hands-on Android delivery.

## Learning map
- [Kotlin, Jetpack & Compose](Kotlin-Jetpack-Compose.md)
- [Coroutines, Flow & Data](Coroutines-Flow-Data.md)
- [Testing, Debugging & Release](Testing-Debugging-Release.md)
- [Interview Q&A](QUESTIONS-ANSWERS.md)
- [Mobile Architecture](../Mobile-Architecture/README.md)

## Architecture mental model
```text
Compose/View UI → ViewModel/State → Use Cases → Repository
                                      ↙       ↘
                                   Remote    Local
```
This is a useful model, not a mandatory layer count.

## Topics to reason about
Lifecycle, configuration/state restoration, coroutine scope, cancellation, unidirectional state, Room migrations, WorkManager, permissions, notifications/deep links, ANRs, memory, network resilience, DI, testing and Play release.
