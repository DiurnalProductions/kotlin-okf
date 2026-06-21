---
id: kotlin.collections
type: concept
title: Collections Overview
description: Kotlin's standard library collection hierarchy and idioms.
tags: [kotlin, collections, stdlib]
prerequisites:
  - kotlin.generic-classes
related:
  - kotlin.lists
  - kotlin.sets
  - kotlin.maps
  - kotlin.immutable-collections
resource: https://kotlinlang.org/docs/collections-overview.html
timestamp: 2026-01-01
---

## Summary

The Kotlin standard library provides read-only and mutable collection interfaces with rich extension functions for transformation and aggregation.

## Mental model

Collections are functional pipelines over data—map, filter, groupBy—not manual index loops. Choose read-only interfaces at API boundaries unless mutation is required.

## Example

```kotlin
val names = users.map { it.name }.filter { it.isNotBlank() }
```

## Common mistakes

- Exposing mutable collections from public APIs
- Assuming Java collections are automatically read-only
- Using collections where sequences would avoid materialization

## Related concepts

- [Lists](/concepts/lists.md)
- [Immutable collections](/concepts/immutable-collections.md)
