---
id: kotlin.jvm-relationship
type: concept
title: JVM Relationship
description: How Kotlin interoperates with the Java Virtual Machine.
tags: [kotlin, jvm, execution]
prerequisites:
  - kotlin.compilation-model
related:
  - kotlin.bytecode
  - kotlin.memory-management
resource: https://kotlinlang.org/docs/jvm-get-started.html
timestamp: 2026-01-01
---

## Summary

On the JVM, Kotlin compiles to bytecode, runs on the same runtime as Java, and interoperates bidirectionally with Java libraries and types.

## Mental model

Kotlin on JVM is a JVM language first-class citizen: same runtime, garbage collector, and classloading—plus Kotlin-specific stdlib and coroutine machinery layered on top.

## Example

```kotlin
// Kotlin calling Java
val list = java.util.ArrayList<String>()

// Java sees Kotlin via generated class files and @Jvm* annotations
```

## Common mistakes

- Ignoring platform types from Java APIs
- Expecting Kotlin null safety to apply inside Java code automatically
- Forgetting `@JvmStatic`, `@JvmOverloads`, and visibility differences

## Related concepts

- [Bytecode](/concepts/bytecode.md)
- [Memory management](/concepts/memory-management.md)
