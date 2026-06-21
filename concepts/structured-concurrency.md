---
id: kotlin.structured-concurrency
type: concept
title: Structured Concurrency
description: Parent-child coroutine relationships with explicit lifetimes.
tags: [kotlin, coroutines, structure]
prerequisites:
  - kotlin.coroutine-scope
related:
  - kotlin.cancellation
  - kotlin.dispatchers
resource: https://kotlinlang.org/docs/coroutine-context-and-dispatchers.html
timestamp: 2026-01-01
---

## Summary

Structured concurrency ensures child coroutines complete or cancel before their parent finishes, preventing lost work and leaks.

## Mental model

Coroutines form a tree mirroring your task decomposition. If the parent is cancelled, children are cancelled—no stray background jobs.

## Example

```kotlin
coroutineScope {
    val a = async { loadA() }
    val b = async { loadB() }
    combine(a.await(), b.await())
}
```

## Common mistakes

- Fire-and-forget launches detached from structure
- Using `GlobalScope` or application-wide orphaned jobs
- Swallowing cancellation exceptions in generic catch blocks

## Related concepts

- [Coroutine scope](/concepts/coroutine-scope.md)
- [Cancellation](/concepts/cancellation.md)
