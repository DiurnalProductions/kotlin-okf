---
id: kotlin.null-safety
type: concept
title: Null Safety
description: Kotlin's compile-time approach to eliminating null reference errors.
tags: [kotlin, null-safety, types]
prerequisites:
  - kotlin.type-inference
  - kotlin.any-unit-nothing
related:
  - kotlin.nullable-types
  - kotlin.safe-calls
  - kotlin.smart-casts
resource: https://kotlinlang.org/docs/null-safety.html
timestamp: 2026-01-01
---

## Summary

Nullability is part of the type system. Non-null types cannot hold null unless you explicitly opt into nullable types.

## Mental model

Null is not a universal default—it is an explicit possibility you must declare with `?`. The compiler tracks whether a reference might be absent and forces you to handle that possibility before use.

## Example

```kotlin
var name: String = "Kotlin"
// name = null  // compile error

var nickname: String? = null  // explicitly nullable
```

## Common mistakes

- Using platform types from Java without narrowing
- Forcing non-null with `!!` instead of modeling absence
- Treating null checks as runtime-only concerns

## Related concepts

- [Nullable types](/concepts/nullable-types.md)
- [Smart casts](/concepts/smart-casts.md)
