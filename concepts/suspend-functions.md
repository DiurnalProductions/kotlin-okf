---
id: kotlin.suspend-functions
type: concept
title: Suspend Functions
description: Functions that can suspend coroutines without blocking threads.
tags: [kotlin, coroutines, suspend]
prerequisites:
  - kotlin.functions
related:
  - kotlin.coroutine-scope
  - kotlin.dispatchers
resource: https://kotlinlang.org/docs/coroutines-basics.html
timestamp: 2026-01-01
---

## Summary

Suspend functions mark points where coroutines may pause cooperatively, resuming later without holding a thread.

## Mental model

Suspend is not 'async keyword soup'—it is a compiler transform that allows non-blocking waiting. Only suspend functions can call other suspend functions directly.

## Example

```kotlin
suspend fun fetchUser(id: String): User {
    delay(100)  // cooperative suspension
    return repository.load(id)
}
```

## Common mistakes

- Calling suspend functions from blocking code without a coroutine builder
- Using `Thread.sleep` inside coroutines
- Treating suspend as parallelism automatically

## Related concepts

- [Coroutine scope](/concepts/coroutine-scope.md)
- [Structured concurrency](/concepts/structured-concurrency.md)
