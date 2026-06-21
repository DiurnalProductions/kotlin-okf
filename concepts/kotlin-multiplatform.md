---
id: kotlin.kotlin-multiplatform
type: concept
title: Kotlin Multiplatform Overview
description: Sharing Kotlin code across JVM, native, JS, and WASM targets.
tags: [kotlin, multiplatform, execution]
prerequisites:
  - kotlin.compilation-model
related:
  - kotlin.multiplatform-modules
  - kotlin.jvm-relationship
resource: https://kotlinlang.org/docs/multiplatform.html
timestamp: 2026-01-01
---

## Summary

Kotlin Multiplatform (KMP) shares common Kotlin code across platforms while allowing expect/actual declarations for platform-specific implementations.

## Mental model

KMP is selective sharing: write business logic once in common code, isolate platform differences behind expect/actual or interfaces, compile each target separately.

## Example

```kotlin
// commonMain
expect fun platformName(): String

// jvmMain
actual fun platformName(): String = "JVM"
```

## Common mistakes

- Putting UI or platform APIs in common code
- Underestimating expect/actual maintenance cost
- Treating KMP as 'write once run everywhere' without platform seams

## Related concepts

- [Multiplatform modules](/concepts/multiplatform-modules.md)
- [Compilation model](/concepts/compilation-model.md)
