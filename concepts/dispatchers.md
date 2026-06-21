---
id: kotlin.dispatchers
type: concept
title: Dispatchers
description: Coroutine dispatchers that map work onto thread pools.
tags: [kotlin, coroutines, dispatchers]
prerequisites:
  - kotlin.coroutine-scope
  - kotlin.structured-concurrency
related:
  - kotlin.suspend-functions
  - kotlin.flows
resource: https://kotlinlang.org/docs/dispatchers.html
timestamp: 2026-01-01
---

## Summary

Dispatchers (`Main`, `IO`, `Default`, `Unconfined`) route coroutine execution to appropriate threads for CPU, I/O, or UI work.

## Mental model

Dispatchers answer 'where does this coroutine run?' Suspend frees threads; dispatchers assign resumed work. Use `withContext` to switch safely.

## Example

```kotlin
withContext(Dispatchers.IO) {
    readFile()
}
```

## Common mistakes

- Blocking IO on `Dispatchers.Default`
- Excessive dispatcher switching
- Assuming `Main` exists on all platforms

## Related concepts

- [Structured concurrency](/concepts/structured-concurrency.md)
- [Suspend functions](/concepts/suspend-functions.md)
