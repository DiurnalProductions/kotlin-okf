---
id: kotlin.sealed-state-modeling
type: concept
title: Sealed State Modeling
description: Modeling UI and domain state with sealed classes.
tags: [kotlin, error-handling, state]
prerequisites:
  - kotlin.sealed-classes
  - kotlin.result-type
related:
  - kotlin.data-classes
  - kotlin.flows
resource: https://kotlinlang.org/docs/sealed-classes.html
timestamp: 2026-01-01
---

## Summary

Sealed hierarchies express loading, success, error, and empty states as exhaustive alternatives consumed with `when`.

## Mental model

Replace boolean flags and nullable triples with one sealed state type. The compiler forces you to handle every state in UI and domain logic.

## Example

```kotlin
sealed interface UiState<out T> {
    data object Loading : UiState<Nothing>
    data class Ready<T>(val data: T) : UiState<T>
    data class Error(val cause: Throwable) : UiState<Nothing>
}
```

## Common mistakes

- Adding unrelated states to one hierarchy
- Using sealed classes without exhaustive `when`
- Mixing ephemeral and persistent state in the same type

## Related concepts

- [Sealed classes](/concepts/sealed-classes.md)
- [Result type](/concepts/result-type.md)
