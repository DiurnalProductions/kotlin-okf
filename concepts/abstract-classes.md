---
id: kotlin.abstract-classes
type: concept
title: Abstract Classes
description: Partially implemented classes that cannot be instantiated directly.
tags: [kotlin, object-model, abstract]
prerequisites:
  - kotlin.inheritance
related:
  - kotlin.interfaces
  - kotlin.sealed-classes
resource: https://kotlinlang.org/docs/classes.html#abstract-classes
timestamp: 2026-01-01
---

## Summary

Abstract classes may declare abstract members and share implemented behavior among related subclasses.

## Mental model

Use abstract classes when subclasses share concrete state or helper implementations. Prefer interfaces when you only need a contract.

## Example

```kotlin
abstract class Shape {
    abstract fun area(): Double
}
```

## Common mistakes

- Choosing abstract classes over sealed hierarchies for finite variants
- Mixing unrelated subclasses under one abstract base
- Using abstract classes where interface + composition suffices

## Related concepts

- [Inheritance](/concepts/inheritance.md)
- [Sealed classes](/concepts/sealed-classes.md)
