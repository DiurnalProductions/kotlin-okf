---
id: kotlin.coroutine-scope
type: concept
title: Coroutine Scope
description: Structured boundary for launching and managing coroutines.
tags: [kotlin, coroutines, scope]
prerequisites:
  - kotlin.suspend-functions
related:
  - kotlin.structured-concurrency
  - kotlin.cancellation
resource: https://kotlinlang.org/docs/coroutine-context-and-dispatchers.html
timestamp: 2026-01-01
---

## Summary

A coroutine scope provides a `CoroutineContext` and lifecycle boundary—coroutines launched in a scope belong to that scope.

## Mental model

Scope is ownership: every coroutine has a parent scope that defines context and cancellation hierarchy. Never use GlobalScope in application code.

## Example

```kotlin
class Loader(private val scope: CoroutineScope) {
    fun start() = scope.launch {
        loadData()
    }
}
```

## Common mistakes

- Launching coroutines without a scope tied to lifecycle
- Leaking scope across components
- Ignoring scope context when testing

## Related concepts

- [Suspend functions](/concepts/suspend-functions.md)
- [Structured concurrency](/concepts/structured-concurrency.md)
