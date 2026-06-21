---
id: kotlin.cancellation
type: concept
title: Cancellation
description: Cooperative cancellation of coroutine work.
tags: [kotlin, coroutines, cancellation]
prerequisites:
  - kotlin.structured-concurrency
  - kotlin.coroutine-scope
related:
  - kotlin.exceptions
  - kotlin.flows
resource: https://kotlinlang.org/docs/cancellation-and-timeouts.html
timestamp: 2026-01-01
---

## Summary

Coroutine cancellation is cooperative—suspend points and `ensureActive()` checks allow cleanup before a coroutine stops.

## Mental model

Cancellation is not Thread.interrupt. A cancelled coroutine throws `CancellationException` at suspension boundaries unless you block without suspending.

## Example

```kotlin
val job = launch {
    try {
        while (isActive) {
            computeChunk()
        }
    } finally {
        cleanup()
    }
}
job.cancel()
```

## Common mistakes

- Catching `Exception` and swallowing cancellation
- Non-suspending blocking loops that ignore cancellation
- Forgetting to close resources in `finally` or `invokeOnCompletion`

## Related concepts

- [Structured concurrency](/concepts/structured-concurrency.md)
- [Flows](/concepts/flows.md)
