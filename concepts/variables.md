---
id: kotlin.variables
type: concept
title: Variables
description: Named bindings that hold values in Kotlin programs.
tags: [kotlin, fundamentals, variables]
prerequisites:[]
related:
  - kotlin.val-vs-var
  - kotlin.type-inference
resource: https://kotlinlang.org/docs/basic-syntax.html#variables
timestamp: 2026-01-01
---

## Summary

Variables are named references to values. Kotlin distinguishes read-only bindings from mutable ones and encourages declaring bindings close to first use.

## Mental model

Think of a variable as a labeled box holding a value reference, not a memory slot you mutate arbitrarily. Kotlin wants you to name what you mean and prefer stable bindings (`val`) unless mutation is intentional.

## Example

```kotlin
val name = "Ada"
var count = 0
count += 1
```

## Common mistakes

- Using `var` by default instead of `val`
- Reusing one mutable variable for unrelated state
- Assuming variables behave like Java fields without considering scope

## Related concepts

- [val vs var](/concepts/val-vs-var.md)
- [Type inference](/concepts/type-inference.md)
