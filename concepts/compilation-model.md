---
id: kotlin.compilation-model
type: concept
title: Compilation Model
description: How Kotlin source is compiled to platform-specific output.
tags: [kotlin, execution, compiler]
prerequisites:[]
related:
  - kotlin.jvm-relationship
  - kotlin.kotlin-multiplatform
resource: https://kotlinlang.org/docs/compiler-reference.html
timestamp: 2026-01-01
---

## Summary

Kotlin compiles `.kt` sources through the Kotlin compiler frontend and backend into platform artifacts such as JVM bytecode, JS, or native binaries.

## Mental model

Kotlin is not interpreted. Source becomes an intermediate representation tailored to each target. One language front-end, multiple back-ends—that is the multiplatform story.

## Example

```text
hello.kt  -->  Kotlin compiler  -->  JVM .class / JS / native klib
```

## Common mistakes

- Assuming Kotlin runs like a scripting interpreter on the JVM
- Ignoring compiler plugins and their effect on output
- Confusing compile-time inlining with runtime behavior

## Related concepts

- [JVM relationship](/concepts/jvm-relationship.md)
- [Kotlin Multiplatform](/concepts/kotlin-multiplatform.md)
