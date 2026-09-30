# Kotlin Example — Explicit UI State

**Type:** Illustrative learning example.

```kotlin
data class ProfileUiState(
    val loading: Boolean = false,
    val name: String? = null,
    val error: String? = null
)
```

A ViewModel can expose a state stream and update it as repository work progresses.

## Why this matters
Explicit state prevents the UI from inferring business state from scattered booleans/widgets.

## Trade-off
Do not create enormous state objects containing unrelated screen concerns. Split boundaries when ownership/lifecycle differs.
