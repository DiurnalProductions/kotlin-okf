---
id: kotlin.val-vs-var
type: concept
title: val vs var
description: Read-only versus mutable variable declarations in Kotlin.
tags: [kotlin, fundamentals, immutability]
prerequisites:
  - kotlin.variables
related:
  - kotlin.type-inference
  - kotlin.immutable-collections
resource: https://kotlinlang.org/docs/properties.html
timestamp: 2026-01-01
---

## Summary

`val` declares a read-only binding; `var` declares a mutable binding. Prefer `val` unless the value must change.

## Mental model

`val` means the reference cannot be reassigned after initialization—like a named constant for the lifetime of that binding. `var` allows reassignment. Immutability is a default mindset in Kotlin, not an afterthought.

## Example

```kotlin
val pi = 3.14
// pi = 3.14159  // compile error

var temperature = 20
temperature = 22  // OK
```

## Common mistakes

- Declaring everything as `var` out of habit
- Confusing `val` with deep immutability (a `val` list can still be mutated if mutable)
- Using `lateinit var` when a nullable type is clearer

## Related concepts

- [Variables](/concepts/variables.md)
- [Immutable collections](/concepts/immutable-collections.md)
