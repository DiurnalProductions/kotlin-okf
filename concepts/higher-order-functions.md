---
id: kotlin.higher-order-functions
type: concept
title: Higher-Order Functions
description: Functions that take or return other functions.
tags: [kotlin, functional, higher-order]
prerequisites:
  - kotlin.lambdas
related:
  - kotlin.closures
  - kotlin.sequences
resource: https://kotlinlang.org/docs/lambdas.html#higher-order-functions
timestamp: 2026-01-01
---

## Summary

Higher-order functions accept function parameters or return functions, enabling map/filter/reduce style composition.

## Mental model

Instead of looping imperatively everywhere, pass the varying behavior as a function parameter. The collection API is the canonical example of this style in Kotlin.

## Example

```kotlin
fun <T> twice(value: T, transform: (T) -> T): T =
    transform(transform(value))
```

## Common mistakes

- Allocating lambdas in tight loops without considering inline
- Returning functions that capture heavy resources
- Making higher-order APIs without inline for primitive collections

## Related concepts

- [Lambdas](/concepts/lambdas.md)
- [Closures](/concepts/closures.md)
