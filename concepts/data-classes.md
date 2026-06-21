---
id: kotlin.data-classes
type: concept
title: Data Classes
description: Classes optimized for holding immutable value-oriented data.
tags: [kotlin, types, values]
prerequisites:
  - kotlin.sealed-classes
  - kotlin.classes
related:
  - kotlin.value-classes
  - kotlin.sealed-classes
resource: https://kotlinlang.org/docs/data-classes.html
timestamp: 2026-01-01
---

## Summary

Data classes automatically generate equals, hashCode, toString, copy, and component functions for properties in the primary constructor.

## Mental model

Data classes are transparent carriers of value. They express 'this bundle of fields together means something' and support structural equality—not identity by default.

## Example

```kotlin
data class User(val id: Long, val name: String)

val updated = user.copy(name = "Ada")
```

## Common mistakes

- Marking entities with identity semantics as data classes
- Mutating data class properties declared as `var` casually
- Expecting data classes to enforce deep immutability automatically

## Related concepts

- [Sealed classes](/concepts/sealed-classes.md)
- [Value classes](/concepts/value-classes.md)
