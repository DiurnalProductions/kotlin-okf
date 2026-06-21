---
id: kotlin.flows
type: concept
title: Flows
description: Cold asynchronous streams built with coroutines.
tags: [kotlin, coroutines, flow]
prerequisites:
  - kotlin.suspend-functions
  - kotlin.coroutine-scope
related:
  - kotlin.sequences
  - kotlin.cancellation
resource: https://kotlinlang.org/docs/flow.html
timestamp: 2026-01-01
---

## Summary

Flow emits multiple values over time asynchronously, supporting operators similar to collections with coroutine-aware execution.

## Mental model

Flow is to async streams what Sequence is to lazy lists—cold by default, collected in a coroutine, respecting structured concurrency and cancellation.

## Example

```kotlin
fun ticks(): Flow<Int> = flow {
    var i = 0
    while (true) {
        emit(i++)
        delay(1_000)
    }
}
```

## Common mistakes

- Treating Flow like a hot Rx stream without SharedFlow/StateFlow
- Running blocking code inside `flow { }` builder
- Collecting flows without lifecycle-aware scope

## Related concepts

- [Sequences](/concepts/sequences.md)
- [Cancellation](/concepts/cancellation.md)
