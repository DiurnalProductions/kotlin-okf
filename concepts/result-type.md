---
id: kotlin.result-type
type: concept
title: Result Type
description: Encapsulating success or failure without throwing.
tags: [kotlin, error-handling, result]
prerequisites:
  - kotlin.null-safety
  - kotlin.exceptions
related:
  - kotlin.sealed-state-modeling
  - kotlin.elvis-operator
resource: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/
timestamp: 2026-01-01
---

## Summary

`Result<T>` represents a completed outcome—success value or failure exception—useful for functional error propagation.

## Mental model

Result makes failure explicit in the type for completed computations. Chain with `map`, `recover`, and `getOrElse` instead of try/catch sprawl.

## Example

```kotlin
fun load(): Result<Data> = runCatching {
    repository.fetch()
}
```

## Common mistakes

- Nesting Results without flattening
- Using Result for domain errors better modeled as sealed types
- Ignoring failure exceptions silently with `getOrNull`

## Related concepts

- [Exceptions](/concepts/exceptions.md)
- [Sealed state modeling](/concepts/sealed-state-modeling.md)
