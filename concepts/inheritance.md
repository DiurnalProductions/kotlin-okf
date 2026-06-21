---
id: kotlin.inheritance
type: concept
title: Inheritance
description: Subclassing classes and implementing interfaces.
tags: [kotlin, object-model, inheritance]
prerequisites:
  - kotlin.interfaces
  - kotlin.classes
related:
  - kotlin.abstract-classes
  - kotlin.delegation
resource: https://kotlinlang.org/docs/inheritance.html
timestamp: 2026-01-01
---

## Summary

Classes inherit from a single superclass; types may implement multiple interfaces. Class inheritance is opt-in via `open`.

## Mental model

Inheritance is an 'is-a' relationship and is intentionally constrained. Kotlin defaults to final classes to push you toward composition unless extension is deliberate.

## Example

```kotlin
open class Base
class Derived : Base(), Repository { /* ... */ }
```

## Common mistakes

- Subclassing for code reuse alone
- Breaking Liskov substitutability with thrown exceptions
- Calling overridable methods from constructors

## Related concepts

- [Abstract classes](/concepts/abstract-classes.md)
- [Delegation](/concepts/delegation.md)
