---
id: kotlin.immutable-collections
type: concept
title: Immutable vs Mutable Collections
description: Read-only interfaces versus mutable collection implementations.
tags: [kotlin, collections, immutability]
prerequisites:
  - kotlin.collections
  - kotlin.lists
  - kotlin.sets
  - kotlin.maps
related:
  - kotlin.val-vs-var
  - kotlin.sequences
resource: https://kotlinlang.org/docs/collections-overview.html#collection-mutability
timestamp: 2026-01-01
---

## Summary

Kotlin distinguishes read-only collection interfaces from mutable ones. Read-only views may still be backed by mutable implementations.

## Mental model

Read-only means 'this API will not mutate'—not necessarily 'this data can never change elsewhere.' For true stability, copy defensively or use persistent structures.

## Example

```kotlin
fun process(items: List<String>) { /* caller cannot mutate via this API */ }
```

## Common mistakes

- Assuming `List` guarantees deep immutability
- Casting read-only lists to mutable implementations
- Returning internal mutable collections from getters

## Related concepts

- [Collections overview](/concepts/collections.md)
- [val vs var](/concepts/val-vs-var.md)
