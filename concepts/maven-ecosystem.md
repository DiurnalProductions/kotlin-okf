---
id: kotlin.maven-ecosystem
type: concept
title: Maven Ecosystem
description: Artifact coordinates, repositories, and publishing conventions.
tags: [kotlin, ecosystem, maven]
prerequisites:
  - kotlin.dependencies
  - kotlin.gradle
related:
  - kotlin.packages
  - kotlin.multiplatform-modules
resource: https://kotlinlang.org/docs/maven.html
timestamp: 2026-01-01
---

## Summary

Kotlin libraries publish JVM artifacts to Maven-compatible repositories using standard coordinates and POM metadata.

## Mental model

Maven Central is the package registry of the JVM world. Coordinates identify artifacts; repositories host them; Gradle resolves the graph.

## Example

```text
org.jetbrains.kotlin:kotlin-stdlib:2.0.0
```

## Common mistakes

- Snapshot dependencies in production builds
- Repository ordering causing dependency substitution surprises
- Publishing without reproducible versions

## Related concepts

- [Dependencies](/concepts/dependencies.md)
- [Gradle](/concepts/gradle.md)
