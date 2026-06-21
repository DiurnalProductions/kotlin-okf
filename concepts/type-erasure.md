---
id: kotlin.type-erasure
type: concept
title: Type Erasure
description: Runtime loss of generic type argument information on the JVM.
tags: [kotlin, generics, jvm]
prerequisites:
  - kotlin.generic-classes
  - kotlin.variance
related:
  - kotlin.star-projections
  - kotlin.value-classes
resource: https://kotlinlang.org/docs/generics.html#type-erasure
timestamp: 2026-01-01
---

## Summary

On the JVM, generic type arguments are erased at runtime; `List<String>` and `List<Int>` share the same runtime class.

## Mental model

Compile-time generics, runtime raw types—that is JVM erasure. Use `inline` + `reified` when you need type arguments at runtime in Kotlin.

## Example

```kotlin
inline fun <reified T> isA(value: Any) = value is T
```

## Common mistakes

- Runtime type checks on generic parameters without reified
- Surprising interop with Java generics and arrays
- Expecting distinct runtime classes per type argument

## Related concepts

- [Generic classes](/concepts/generic-classes.md)
- [Star projections](/concepts/star-projections.md)
