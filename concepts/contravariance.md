---
id: kotlin.contravariance
type: concept
title: Contravariance
description: Consumer variance using the `in` modifier.
tags: [kotlin, generics, contravariance]
prerequisites:
  - kotlin.variance
related:
  - kotlin.covariance
  - kotlin.function-types
resource: https://kotlinlang.org/docs/generics.html#contravariance
timestamp: 2026-01-01
---

## Summary

`in T` marks contravariant type parameters—subtyping reverses for consumers that accept `T`.

## Mental model

If you only consume values, a handler of `Animal` can handle `Dog`. Contravariance flips the subtyping arrow for input-only positions.

## Example

```kotlin
interface Sink<in T> {
    fun accept(value: T)
}
```

## Common mistakes

- Applying `in` to producer APIs
- Forgetting function parameter types are contravariant in classical terms
- Mixing invariant and contravariant uses of the same parameter

## Related concepts

- [Variance](/concepts/variance.md)
- [Function types](/concepts/function-types.md)
