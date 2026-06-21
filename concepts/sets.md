---
id: kotlin.sets
type: concept
title: Sets
description: Collections of unique elements without guaranteed order.
tags: [kotlin, collections, sets]
prerequisites:
  - kotlin.collections
related:
  - kotlin.immutable-collections
  - kotlin.maps
resource: https://kotlinlang.org/docs/set-operations.html
timestamp: 2026-01-01
---

## Summary

`Set` and `MutableSet` hold unique elements, with `LinkedHashSet` and `HashSet` providing common implementations.

## Mental model

Sets answer membership questions: 'is this element present?' Order is implementation-dependent unless you choose a linked variant.

## Example

```kotlin
val tags: Set<String> = setOf("kotlin", "okf", "kotlin")
println(tags.size)  // 2
```

## Common mistakes

- Using sets with mutable elements that break uniqueness
- Expecting sorted iteration from plain `setOf`
- O(n) lookups by converting lists to sets repeatedly

## Related concepts

- [Collections overview](/concepts/collections.md)
- [Maps](/concepts/maps.md)
