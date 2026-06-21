---
id: kotlin.value-classes
type: concept
title: Inline Value Classes
description: Zero-overhead wrapper types for domain-specific primitives.
tags: [kotlin, types, inline]
prerequisites:
  - kotlin.data-classes
related:
  - kotlin.type-erasure
  - kotlin.jvm-relationship
resource: https://kotlinlang.org/docs/inline-classes.html
timestamp: 2026-01-01
---

## Summary

Value classes (`@JvmInline value class`) wrap a single underlying value to create distinct types without runtime boxing on the JVM when used as concrete types.

## Mental model

Value classes add meaning to raw primitives at compile time—UserId is not just Long—while staying lightweight at runtime when inlined.

## Example

```kotlin
@JvmInline
value class UserId(val value: Long)

fun findUser(id: UserId) { /* ... */ }
```

## Common mistakes

- Using value classes with nullable or generic erasure in ways that force boxing
- Expecting referential identity
- Wrapping many fields instead of using a data class

## Related concepts

- [Data classes](/concepts/data-classes.md)
- [Type erasure](/concepts/type-erasure.md)
