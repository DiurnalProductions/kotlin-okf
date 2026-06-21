---
id: kotlin.elvis-operator
type: concept
title: Elvis Operator
description: The `?:` operator for providing default values when an expression is null.
tags: [kotlin, null-safety, operators]
prerequisites:
  - kotlin.nullable-types
  - kotlin.safe-calls
related:
  - kotlin.result-type
  - kotlin.smart-casts
resource: https://kotlinlang.org/docs/null-safety.html#elvis-operator
timestamp: 2026-01-01
---

## Summary

The Elvis operator `?:` returns the left operand if it is non-null; otherwise it evaluates and returns the right operand.

## Mental model

Elvis is a concise defaulting mechanism: 'use this value, or if absent, fall back to that.' It keeps null handling expression-oriented rather than imperative.

## Example

```kotlin
val displayName = nickname ?: name
val count = items?.size ?: 0
```

## Common mistakes

- Using Elvis to hide missing data instead of modeling errors
- Placing side effects on the right-hand side unintentionally
- Overusing `?: throw` when `Result` or sealed types fit better

## Related concepts

- [Safe calls](/concepts/safe-calls.md)
- [Result type](/concepts/result-type.md)
