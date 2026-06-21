---
id: kotlin.type-inference
type: concept
title: Type Inference
description: Automatic deduction of types from initializing expressions.
tags: [kotlin, fundamentals, types]
prerequisites:
  - kotlin.val-vs-var
related:
  - kotlin.null-safety
  - kotlin.function-types
resource: https://kotlinlang.org/docs/basic-types.html
timestamp: 2026-01-01
---

## Summary

The compiler infers types from context when they are omitted, while keeping Kotlin statically typed.

## Mental model

Type inference is the compiler filling in the type label on your binding. You still have a fixed static type—the compiler just saves you from writing it when the initializer makes it obvious.

## Example

```kotlin
val items = listOf(1, 2, 3)  // List<Int>
val greet: (String) -> Unit = { println(it) }
```

## Common mistakes

- Omitting types in public APIs where explicit types improve readability
- Assuming inferred types are more dynamic than they are
- Letting inference widen numeric types unexpectedly

## Related concepts

- [val vs var](/concepts/val-vs-var.md)
- [Null safety](/concepts/null-safety.md)
