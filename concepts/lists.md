---
id: kotlin.lists
type: concept
title: Lists
description: Ordered collections with indexed access.
tags: [kotlin, collections, lists]
prerequisites:
  - kotlin.collections
related:
  - kotlin.immutable-collections
  - kotlin.sequences
resource: https://kotlinlang.org/docs/list-operations.html
timestamp: 2026-01-01
---

## Summary

`List` and `MutableList` represent ordered sequences with positional access and predictable iteration order.

## Mental model

Lists are ordered sequences—use them when order matters or index access is required. Prefer `List` return types to signal callers should not mutate.

## Example

```kotlin
val readOnly: List<Int> = listOf(1, 2, 3)
val mutable = mutableListOf(1, 2, 3)
```

## Common mistakes

- Using lists where sets would enforce uniqueness
- Mutating a list while iterating it
- Confusing `Array` and `List` interop semantics

## Related concepts

- [Collections overview](/concepts/collections.md)
- [Immutable collections](/concepts/immutable-collections.md)
