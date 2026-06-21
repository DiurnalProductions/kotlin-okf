---
id: kotlin.classes
type: concept
title: Classes
description: User-defined types combining state and behavior.
tags: [kotlin, object-model, classes]
prerequisites:
  - kotlin.variables
  - kotlin.functions
related:
  - kotlin.interfaces
  - kotlin.data-classes
resource: https://kotlinlang.org/docs/classes.html
timestamp: 2026-01-01
---

## Summary

Classes define properties and methods. Kotlin classes are final by default and support primary and secondary constructors.

## Mental model

Classes bundle state with behavior, but Kotlin prefers composition, values, and functions over deep inheritance trees. A class should express a coherent abstraction—not a grab bag.

## Example

```kotlin
class Account private constructor(val id: Long) {
    companion object {
        fun open(id: Long) = Account(id)
    }
}
```

## Common mistakes

- Deep inheritance instead of delegation or composition
- Exposing mutable state without invariants
- Using open classes when sealed or data classes fit

## Related concepts

- [Interfaces](/concepts/interfaces.md)
- [Delegation](/concepts/delegation.md)
