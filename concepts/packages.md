---
id: kotlin.packages
type: concept
title: Packages
description: Namespace organization for Kotlin declarations.
tags: [kotlin, modules, packages]
prerequisites:
  - kotlin.classes
related:
  - kotlin.multiplatform-modules
  - kotlin.gradle
resource: https://kotlinlang.org/docs/packages.html
timestamp: 2026-01-01
---

## Summary

Packages group related declarations and map to directory structure. Imports bring declarations into scope.

## Mental model

Packages are namespaces—not class loaders by themselves. They define visibility boundaries at the source level and organize APIs.

## Example

```kotlin
package com.example.app.model

import com.example.app.util.formatName
```

## Common mistakes

- Package names not matching directory paths
- Wildcard imports reducing clarity
- Confusing package visibilities with module boundaries

## Related concepts

- [Multiplatform modules](/concepts/multiplatform-modules.md)
- [Gradle](/concepts/gradle.md)
