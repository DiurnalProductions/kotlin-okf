---
id: kotlin.variance
type: concept
title: Variance
description: How type parameter variance controls subtyping relationships.
tags: [kotlin, generics, variance]
prerequisites:
  - kotlin.generic-classes
related:
  - kotlin.covariance
  - kotlin.contravariance
  - kotlin.star-projections
resource: https://kotlinlang.org/docs/generics.html#variance
timestamp: 2026-01-01
---

## Summary

Variance annotations (`out`, `in`) declare whether a type parameter is producer (`out`), consumer (`in`), or invariant.

## Mental model

Variance answers: if `Cat` is a `Animal`, is `Box<Cat>` a `Box<Animal>`? The answer depends on whether the type parameter appears in output or input positions.

## Example

```kotlin
interface Producer<out T> {
    fun produce(): T
}
```

## Common mistakes

- Declaring `out`/`in` without understanding producer/consumer roles
- Expecting mutable collections to be covariant
- Using variance where simple generics suffice

## Related concepts

- [Covariance](/concepts/covariance.md)
- [Contravariance](/concepts/contravariance.md)
