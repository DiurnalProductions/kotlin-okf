---
id: kotlin.lambdas
type: concept
title: Lambdas
description: Anonymous function literals and concise functional syntax.
tags: [kotlin, functional, lambdas]
prerequisites:
  - kotlin.functions
  - kotlin.function-types
related:
  - kotlin.higher-order-functions
  - kotlin.closures
resource: https://kotlinlang.org/docs/lambdas.html
timestamp: 2026-01-01
---

## Summary

Lambdas are function literals written with `{ args -> body }`, often passed as the last argument outside parentheses.

## Mental model

Lambdas are unnamed functions you hand to APIs expecting behavior. Trailing lambda syntax makes DSL-shaped APIs read naturally.

## Example

```kotlin
list.filter { it > 0 }
list.map { value -> value * 2 }
```

## Common mistakes

- Shadowing outer names carelessly in nested lambdas
- Using `it` when multiple parameters make names unclear
- Capturing mutable state unintentionally

## Related concepts

- [Function types](/concepts/function-types.md)
- [Higher-order functions](/concepts/higher-order-functions.md)
