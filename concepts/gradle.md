---
id: kotlin.gradle
type: concept
title: Gradle
description: Primary build system for Kotlin projects.
tags: [kotlin, ecosystem, gradle]
prerequisites:
  - kotlin.multiplatform-modules
related:
  - kotlin.dependencies
  - kotlin.maven-ecosystem
resource: https://kotlinlang.org/docs/gradle.html
timestamp: 2026-01-01
---

## Summary

Gradle builds Kotlin projects using the Kotlin Gradle plugin, managing compilation, testing, and packaging.

## Mental model

Gradle is the orchestration layer: source sets, tasks, plugins, and dependencies become buildable artifacts. Kotlin DSL (`build.gradle.kts`) is idiomatic for new projects.

## Example

```kotlin
plugins {
    kotlin("jvm") version "2.0.0"
}
```

## Common mistakes

- Applying plugins without compatible versions
- Putting logic in build scripts that belongs in convention plugins
- Ignoring configuration cache compatibility

## Related concepts

- [Dependencies](/concepts/dependencies.md)
- [Multiplatform modules](/concepts/multiplatform-modules.md)
