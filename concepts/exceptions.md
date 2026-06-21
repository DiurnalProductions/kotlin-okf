---
id: kotlin.exceptions
type: concept
title: Exceptions
description: Throwable-based error signaling in Kotlin.
tags: [kotlin, error-handling, exceptions]
prerequisites:
  - kotlin.functions
related:
  - kotlin.result-type
  - kotlin.cancellation
resource: https://kotlinlang.org/docs/exceptions.html
timestamp: 2026-01-01
---

## Summary

Kotlin uses Java-compatible exceptions for exceptional conditions. Unchecked exceptions are the default style on JVM.

## Mental model

Exceptions are for exceptional control flow—not expected business outcomes. For expected failures, prefer typed results or sealed models.

## Example

```kotlin
fun parsePort(raw: String): Int =
    raw.toIntOrNull() ?: throw IllegalArgumentException("Invalid port: $raw")
```

## Common mistakes

- Using exceptions for routine validation paths
- Catching broad `Exception` in coroutines (breaks cancellation)
- Empty catch blocks hiding failures

## Related concepts

- [Result type](/concepts/result-type.md)
- [Cancellation](/concepts/cancellation.md)
