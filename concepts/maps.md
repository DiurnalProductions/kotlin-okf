---
id: kotlin.maps
type: concept
title: Maps
description: Key-value associations with unique keys.
tags: [kotlin, collections, maps]
prerequisites:
  - kotlin.collections
related:
  - kotlin.immutable-collections
  - kotlin.sets
resource: https://kotlinlang.org/docs/map-operations.html
timestamp: 2026-01-01
---

## Summary

`Map` and `MutableMap` associate keys to values, supporting efficient lookup by key.

## Mental model

Maps are functions from keys to optional values—think dictionary, index, or cache. Prefer immutable maps for shared configuration.

## Example

```kotlin
val scores: Map<String, Int> = mapOf("Ada" to 99, "Lin" to 97)
```

## Common mistakes

- Using mutable maps as global state
- Null values confusion with `Map.get` vs `getValue`
- Keys with unstable `hashCode` implementations

## Related concepts

- [Collections overview](/concepts/collections.md)
- [Immutable collections](/concepts/immutable-collections.md)
