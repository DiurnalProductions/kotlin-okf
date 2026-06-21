---
id: kotlin.smart-casts
type: concept
title: Smart Casts
description: Compiler-driven type narrowing after checks and control flow.
tags: [kotlin, null-safety, types]
prerequisites:
  - kotlin.null-safety
  - kotlin.nullable-types
related:
  - kotlin.sealed-classes
  - kotlin.classes
resource: https://kotlinlang.org/docs/typecasts.html#smart-casts
timestamp: 2026-01-01
---

## Summary

After null checks, type checks, or exhaustive `when` branches, the Kotlin compiler automatically narrows types in safe regions.

## Mental model

Smart casts are the compiler remembering facts you proved. If you checked `x != null` in an immutable context, Kotlin trusts that fact in the same block without redundant casts.

## Example

```kotlin
fun greet(name: String?) {
    if (name != null) {
        println(name.length)  // name is String here
    }
}
```

## Common mistakes

- Expecting smart casts on mutable `var` properties accessed multiple times
- Smart casting open properties from other modules
- Relying on casts across concurrent mutation

## Related concepts

- [Null safety](/concepts/null-safety.md)
- [Sealed classes](/concepts/sealed-classes.md)
