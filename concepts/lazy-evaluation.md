---
id: kotlin.lazy-evaluation
type: concept
title: Lazy Evaluation
description: Deferring computation until a value is actually needed.
tags: [kotlin, lazy, functional]
prerequisites:
  - kotlin.sequences
related:
  - kotlin.sequences
  - kotlin.immutable-collections
resource: https://kotlinlang.org/docs/delegated-properties.html#lazy-properties
timestamp: 2026-01-01
---

## Summary

Lazy evaluation postpones work—sequences compute on demand; `lazy` delegates initialize once on first access.

## Mental model

Lazy means pay-for-what-you-use. Intermediate steps in sequences are not run until a terminal operation forces them—similar in spirit to cold Flows in coroutines.

## Example

```kotlin
val expensive by lazy {
    computeConfig()
}
```

## Common mistakes

- Lazy initialization with thread-safety assumptions without choosing LazyThreadSafetyMode
- Infinite lazy pipelines without limits
- Side effects hidden in lazy chains

## Related concepts

- [Sequences](/concepts/sequences.md)
- [Flows](/concepts/flows.md)
