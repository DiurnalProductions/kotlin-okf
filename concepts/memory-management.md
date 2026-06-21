---
id: kotlin.memory-management
type: concept
title: Memory Management
description: High-level memory and allocation behavior on Kotlin/JVM.
tags: [kotlin, jvm, memory]
prerequisites:
  - kotlin.jvm-relationship
related:
  - kotlin.immutable-collections
  - kotlin.sequences
resource: https://kotlinlang.org/docs/jvm-get-started.html
timestamp: 2026-01-01
---

## Summary

On the JVM, Kotlin objects are garbage-collected heap allocations. Value semantics and immutability reduce shared mutable state bugs but do not eliminate GC.

## Mental model

Kotlin references point to heap objects collected by the JVM GC. Prefer immutable values and avoid unnecessary allocation hot paths—especially in collection pipelines.

## Example

```kotlin
val snapshot = users.toList()  // new list, old list unchanged if immutable source
```

## Common mistakes

- Assuming `val` prevents mutation of referenced objects
- Creating huge intermediate lists where sequences would stream
- Retaining references in long-lived coroutine scopes unintentionally

## Related concepts

- [JVM relationship](/concepts/jvm-relationship.md)
- [Sequences](/concepts/sequences.md)
