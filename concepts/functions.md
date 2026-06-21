---
id: kotlin.functions
type: concept
title: Functions
description: Named callable units with parameters, return types, and expression bodies.
tags: [kotlin, functions, fundamentals]
prerequisites:
  - kotlin.variables
  - kotlin.type-inference
related:
  - kotlin.lambdas
  - kotlin.extension-functions
resource: https://kotlinlang.org/docs/functions.html
timestamp: 2026-01-01
---

## Summary

Functions are first-class building blocks declared with `fun`, supporting default arguments, named arguments, and single-expression bodies.

## Mental model

Functions are values you can pass around—not merely methods bolted onto classes. Kotlin favors concise expression-bodied functions when logic is pure and obvious.

## Example

```kotlin
fun greet(name: String, excited: Boolean = false): String =
    if (excited) "Hi, $name!" else "Hello, $name"
```

## Common mistakes

- Using side effects in expression-bodied functions unintentionally
- Overloading when default or extension functions are clearer
- Ignoring `tailrec` for recursive algorithms that qualify

## Related concepts

- [Lambdas](/concepts/lambdas.md)
- [Extension functions](/concepts/extension-functions.md)
