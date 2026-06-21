---
id: kotlin.nullable-types
type: concept
title: Nullable Types
description: Types that explicitly allow the null value.
tags: [kotlin, null-safety, types]
prerequisites:
  - kotlin.null-safety
  - kotlin.any-unit-nothing
related:
  - kotlin.safe-calls
  - kotlin.elvis-operator
  - kotlin.smart-casts
resource: https://kotlinlang.org/docs/null-safety.html
timestamp: 2026-01-01
---

## Summary

Appending `?` to a type marks it as nullable, separating 'present value' from 'possibly absent' at compile time.

## Mental model

A nullable type is a union of a value and absence, written inline in the type. The compiler treats `String` and `String?` as different types—you cannot pass one where the other is required without conversion.

## Example

```kotlin
fun lengthOrZero(text: String?): Int =
    if (text != null) text.length else 0
```

## Common mistakes

- Nullable everywhere instead of modeling optional data deliberately
- Ignoring smart cast limitations with mutable properties
- Mixing Java nullability annotations inconsistently

## Related concepts

- [Null safety](/concepts/null-safety.md)
- [Safe calls](/concepts/safe-calls.md)
