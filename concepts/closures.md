---
id: kotlin.closures
type: concept
title: Closures
description: Lambdas that capture variables from enclosing scopes.
tags: [kotlin, functional, closures]
prerequisites:
  - kotlin.higher-order-functions
  - kotlin.lambdas
related:
  - kotlin.sequences
  - kotlin.coroutine-scope
resource: https://kotlinlang.org/docs/lambdas.html#closures
timestamp: 2026-01-01
---

## Summary

Closures capture references from outer scopes, allowing lambdas to carry contextual state.

## Mental model

A closure is a function plus its captured environment. Captured `val` bindings are safe; captured mutable state requires discipline—especially across async boundaries.

## Example

```kotlin
fun counter(): () -> Int {
    var n = 0
    return { ++n }
}
```

## Common mistakes

- Capturing mutable vars shared across concurrent coroutines
- Accidental memory leaks via long-lived closures
- Assuming captured variables are copied by value

## Related concepts

- [Higher-order functions](/concepts/higher-order-functions.md)
- [Coroutine scope](/concepts/coroutine-scope.md)
