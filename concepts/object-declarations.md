---
id: kotlin.object-declarations
type: concept
title: Object Declarations
description: Singleton objects declared with the `object` keyword.
tags: [kotlin, object-model, singleton]
prerequisites:
  - kotlin.classes
related:
  - kotlin.companion-objects
  - kotlin.delegation
resource: https://kotlinlang.org/docs/object-declarations.html
timestamp: 2026-01-01
---

## Summary

`object` declares a singleton instance with lazy initialization, useful for service locators, factories, and named constants groupings.

## Mental model

An object declaration is a class with exactly one instance—created on first access. Use it for true singletons, not as a replacement for dependency injection.

## Example

```kotlin
object Logger {
    fun info(message: String) = println(message)
}
```

## Common mistakes

- Global mutable singletons hiding testability problems
- Using objects where a `val` instance would suffice
- Confusing object expressions with object declarations

## Related concepts

- [Companion objects](/concepts/companion-objects.md)
- [Classes](/concepts/classes.md)
