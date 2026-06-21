---
id: kotlin.interfaces
type: concept
title: Interfaces
description: Abstract contracts with method and property declarations.
tags: [kotlin, object-model, interfaces]
prerequisites:
  - kotlin.classes
related:
  - kotlin.delegation
  - kotlin.inheritance
resource: https://kotlinlang.org/docs/interfaces.html
timestamp: 2026-01-01
---

## Summary

Interfaces define capabilities classes may implement, supporting default and property implementations.

## Mental model

Interfaces describe what something can do. Prefer small, focused interfaces and combine them rather than building monolithic supertypes.

## Example

```kotlin
interface Repository {
    suspend fun load(id: String): String
}
```

## Common mistakes

- Using interfaces purely for namespace grouping
- Fat interfaces violating interface segregation
- Forgetting interface methods are public by default

## Related concepts

- [Classes](/concepts/classes.md)
- [Delegation](/concepts/delegation.md)
