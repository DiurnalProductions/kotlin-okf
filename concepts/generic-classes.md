---
id: kotlin.generic-classes
type: concept
title: Generic Classes
description: Types parameterized by type arguments for reusable abstractions.
tags: [kotlin, generics, types]
prerequisites:
  - kotlin.classes
related:
  - kotlin.variance
  - kotlin.type-erasure
resource: https://kotlinlang.org/docs/generics.html
timestamp: 2026-01-01
---

## Summary

Generic classes and functions declare type parameters in angle brackets, enabling type-safe containers and algorithms.

## Mental model

Generics let you write code once that works for many types while preserving compile-time checks—`List<String>` is not `List<Any>` at compile time.

## Example

```kotlin
class Box<T>(val value: T)

fun <T> singleton(item: T): List<T> = listOf(item)
```

## Common mistakes

- Raw types when migrating from Java habits
- Over-constraining type parameters unnecessarily
- Ignoring reified generics require `inline` functions

## Related concepts

- [Variance](/concepts/variance.md)
- [Type erasure](/concepts/type-erasure.md)
