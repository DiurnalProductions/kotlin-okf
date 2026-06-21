---
id: kotlin.multiplatform-modules
type: concept
title: Multiplatform Modules
description: Gradle modules structuring shared and platform-specific Kotlin code.
tags: [kotlin, multiplatform, modules]
prerequisites:
  - kotlin.packages
related:
  - kotlin.kotlin-multiplatform
  - kotlin.gradle
resource: https://kotlinlang.org/docs/multiplatform-dsl-reference.html
timestamp: 2026-01-01
---

## Summary

KMP modules define source sets like `commonMain`, `jvmMain`, and `iosMain`, compiling shared and platform code into artifacts.

## Mental model

A module is a compilation unit with explicit dependencies and source sets. Common code is the contract; platform source sets fill in platform gaps.

## Example

```kotlin
kotlin {
    jvm()
    iosArm64()
    sourceSets {
        commonMain.dependencies { /* shared deps */ }
    }
}
```

## Common mistakes

- Circular module dependencies
- Leaking platform APIs into commonMain
- One giant module instead of layered modules

## Related concepts

- [Kotlin Multiplatform](/concepts/kotlin-multiplatform.md)
- [Gradle](/concepts/gradle.md)
