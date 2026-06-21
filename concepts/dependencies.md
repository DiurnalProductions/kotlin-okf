---
id: kotlin.dependencies
type: concept
title: Dependencies
description: Declaring external libraries and modules in builds.
tags: [kotlin, ecosystem, dependencies]
prerequisites:
  - kotlin.gradle
related:
  - kotlin.maven-ecosystem
  - kotlin.packages
resource: https://kotlinlang.org/docs/gradle-configure-project.html
timestamp: 2026-01-01
---

## Summary

Dependencies are declared in Gradle with coordinates (`group:artifact:version`) and scoped to configurations like `implementation` and `api`.

## Mental model

Dependencies are directed edges in your build graph. Choose scopes deliberately—`api` exposes transitively, `implementation` hides internals.

## Example

```kotlin
dependencies {
    implementation("org.jetbrains.kotlinx:kotlinx-coroutines-core:1.9.0")
    testImplementation(kotlin("test"))
}
```

## Common mistakes

- Leaking implementation dependencies via `api`
- Version catalog neglect leading to drift
- Depending on heavy libraries for tiny utilities

## Related concepts

- [Gradle](/concepts/gradle.md)
- [Maven ecosystem](/concepts/maven-ecosystem.md)
