---
id: kotlin.safe-calls
type: concept
title: Safe Calls
description: The `?.` operator for null-safe member access.
tags: [kotlin, null-safety, operators]
prerequisites:
  - kotlin.nullable-types
related:
  - kotlin.elvis-operator
  - kotlin.smart-casts
resource: https://kotlinlang.org/docs/null-safety.html#safe-calls
timestamp: 2026-01-01
---

## Summary

The safe call operator `?.` invokes a member only when the receiver is non-null; otherwise the whole expression evaluates to null.

## Mental model

Safe call is short-circuiting access: 'if receiver exists, continue; otherwise stop and yield null.' It composes cleanly in chains without nested if-checks.

## Example

```kotlin
val city = user?.address?.city
val upper = name?.uppercase()
```

## Common mistakes

- Chaining so long that null propagation becomes unclear
- Using safe calls where absence should be an error
- Forgetting the result type becomes nullable

## Related concepts

- [Nullable types](/concepts/nullable-types.md)
- [Elvis operator](/concepts/elvis-operator.md)
