---
id: kotlin.any-unit-nothing
type: concept
title: Any, Unit, and Nothing
description: Kotlin's top, unit, and bottom types in the type hierarchy.
tags: [kotlin, types, fundamentals]
prerequisites:
  - kotlin.type-inference
related:
  - kotlin.nullable-types
  - kotlin.functions
resource: https://kotlinlang.org/docs/basic-types.html
timestamp: 2026-01-01
---

## Summary

`Any` is the supertype of all non-null types, `Unit` is the type of useful absence of value, and `Nothing` is the type of expressions that never complete normally.

## Mental model

`Any` is the root of the non-null world—everything meaningful is an `Any`. `Unit` is not void-as-nothing; it is a real singleton type signaling 'done, no meaningful result.' `Nothing` sits at the bottom: if the compiler knows an expression never returns, it can prove unreachable code and refine types.

## Example

```kotlin
fun log(message: String): Unit {
    println(message)
}

fun fail(msg: String): Nothing {
    throw IllegalStateException(msg)
}
```

## Common mistakes

- Treating `Unit` like Java `void` in all contexts
- Forgetting `Any?` includes null while `Any` does not
- Not using `Nothing` to model exhaustive control flow

## Related concepts

- [Nullable types](/concepts/nullable-types.md)
- [Functions](/concepts/functions.md)
