---
id: kotlin.sealed-classes
type: concept
title: Sealed Classes
description: Restricted class hierarchies for modeling finite sets of alternatives.
tags: [kotlin, types, algebraic-data-types]
prerequisites:
  - kotlin.nullable-types
  - kotlin.classes
related:
  - kotlin.data-classes
  - kotlin.enums
  - kotlin.sealed-state-modeling
resource: https://kotlinlang.org/docs/sealed-classes.html
timestamp: 2026-01-01
---

## Summary

Sealed classes define a closed set of subclasses known at compile time, enabling exhaustive `when` expressions.

## Mental model

A sealed class is a typed sum: the value is exactly one of a known set of variants. The compiler can verify you handled every case—ideal for state machines and domain events.

## Example

```kotlin
sealed class Outcome {
    data class Success(val value: String) : Outcome()
    data class Failure(val error: Throwable) : Outcome()
}
```

## Common mistakes

- Using sealed classes for open-ended plugin systems
- Forgetting subclasses must live in the same module
- Mixing too many unrelated variants in one hierarchy

## Related concepts

- [Data classes](/concepts/data-classes.md)
- [Sealed state modeling](/concepts/sealed-state-modeling.md)
