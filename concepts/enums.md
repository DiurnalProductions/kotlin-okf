---
id: kotlin.enums
type: concept
title: Enums
description: Type-safe enumerations of named constants.
tags: [kotlin, types, enums]
prerequisites:
  - kotlin.sealed-classes
related:
  - kotlin.sealed-classes
  - kotlin.data-classes
resource: https://kotlinlang.org/docs/enum-classes.html
timestamp: 2026-01-01
---

## Summary

Enum classes represent fixed sets of named values, optionally with properties and behavior.

## Mental model

Enums are finite nominal constants. Use them when variants are singletons without distinct per-case data; use sealed classes when each case carries different structure.

## Example

```kotlin
enum class Direction { NORTH, SOUTH, EAST, WEST }

enum class Color(val rgb: Int) {
    RED(0xFF0000),
    GREEN(0x00FF00)
}
```

## Common mistakes

- Using enums when sealed classes would model structured variants better
- Adding behavior that belongs in domain services
- Serializing enums without stable naming strategy

## Related concepts

- [Sealed classes](/concepts/sealed-classes.md)
- [Data classes](/concepts/data-classes.md)
