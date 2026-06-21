---
id: kotlin.covariance
type: concept
title: Covariance
description: Producer variance using the `out` modifier.
tags: [kotlin, generics, covariance]
prerequisites:
  - kotlin.variance
related:
  - kotlin.contravariance
  - kotlin.lists
resource: https://kotlinlang.org/docs/generics.html#covariance
timestamp: 2026-01-01
---

## Summary

`out T` marks `T` as covariant—subtyping follows the type argument direction for read-only producers.

## Mental model

Covariance preserves the direction of subtyping: if you only produce `T`, a `List<Dog>` can be treated as `List<Animal>` when read-only at the type level.

## Example

```kotlin
interface Source<out T> {
    fun next(): T
}
```

## Common mistakes

- Using `out` on types that also consume T
- Assuming all read-only interfaces are safely covariant in practice
- Confusing covariance with immutability guarantees

## Related concepts

- [Variance](/concepts/variance.md)
- [Immutable collections](/concepts/immutable-collections.md)
