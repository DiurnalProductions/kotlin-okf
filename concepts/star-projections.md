---
id: kotlin.star-projections
type: concept
title: Star Projections
description: Using `*` when type arguments are unknown or irrelevant.
tags: [kotlin, generics, projections]
prerequisites:
  - kotlin.variance
related:
  - kotlin.type-erasure
  - kotlin.generic-classes
resource: https://kotlinlang.org/docs/generics.html#star-projections
timestamp: 2026-01-01
---

## Summary

Star projections (`Foo<*>`) represent unknown type arguments while respecting declared variance bounds.

## Mental model

A star projection says 'some specific type argument exists, but I do not know or care which.' It is safer than raw types and aligns with variance limits.

## Example

```kotlin
fun printSize(list: List<*>) {
    println(list.size)
}
```

## Common mistakes

- Using star projections where a specific type parameter is needed
- Expecting to write into covariant star-projected collections
- Confusing `List<*>` with `List<Any?>`

## Related concepts

- [Variance](/concepts/variance.md)
- [Type erasure](/concepts/type-erasure.md)
