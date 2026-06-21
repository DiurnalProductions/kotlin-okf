---
id: kotlin.function-types
type: concept
title: Function Types
description: Types describing function signatures as values.
tags: [kotlin, functions, types]
prerequisites:
  - kotlin.functions
related:
  - kotlin.lambdas
  - kotlin.higher-order-functions
resource: https://kotlinlang.org/docs/lambdas.html#function-types
timestamp: 2026-01-01
---

## Summary

Function types like `(Int, Int) -> Int` describe parameter lists and return types, enabling functions to be stored and passed like other values.

## Mental model

A function type is a contract: these inputs, that output, possibly nullable or suspend-modified. It is how Kotlin makes higher-order programming type-safe.

## Example

```kotlin
val sum: (Int, Int) -> Int = { a, b -> a + b }
val action: () -> Unit = { println("done") }
```

## Common mistakes

- Confusing function type syntax with function invocation
- Omitting parentheses when nesting function types
- Forgetting suspend function types use `suspend` modifier in the type

## Related concepts

- [Functions](/concepts/functions.md)
- [Higher-order functions](/concepts/higher-order-functions.md)
