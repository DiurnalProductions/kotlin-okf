---
id: kotlin.sequences
type: concept
title: Sequences
description: Lazy collection pipelines that compute elements on demand.
tags: [kotlin, collections, lazy]
prerequisites:
  - kotlin.immutable-collections
  - kotlin.lambdas
related:
  - kotlin.lazy-evaluation
  - kotlin.flows
resource: https://kotlinlang.org/docs/sequences.html
timestamp: 2026-01-01
---

## Summary

Sequences defer computation until terminal operations, chaining intermediate transformations without eager intermediate lists.

## Mental model

A sequence is a lazy iterator pipeline—elements are produced one step at a time. Use sequences for large or infinite data and multi-step transforms.

## Example

```kotlin
val result = (1..1_000_000).asSequence()
    .filter { it % 2 == 0 }
    .map { it * it }
    .take(3)
    .toList()
```

## Common mistakes

- Using sequences for tiny collections where eager lists are faster
- Forgetting terminal operation is required
- Mixing sequence and collection operations accidentally

## Related concepts

- [Lazy evaluation](/concepts/lazy-evaluation.md)
- [Flows](/concepts/flows.md)
