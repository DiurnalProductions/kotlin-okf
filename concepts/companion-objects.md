---
id: kotlin.companion-objects
type: concept
title: Companion Objects
description: Named or anonymous singletons associated with a class.
tags: [kotlin, object-model, companion]
prerequisites:
  - kotlin.classes
  - kotlin.object-declarations
related:
  - kotlin.object-declarations
  - kotlin.classes
resource: https://kotlinlang.org/docs/object-declarations.html#companion-objects
timestamp: 2026-01-01
---

## Summary

Companion objects provide class-scoped factory methods and constants, accessed via the class name in Kotlin.

## Mental model

Companion objects are the class's single associated object—like static members in Java but as a real object implementing interfaces if needed.

## Example

```kotlin
class User private constructor(val name: String) {
    companion object {
        fun guest() = User("guest")
    }
}
```

## Common mistakes

- Overusing companion objects as service registries
- Forgetting Java interop uses `@JvmStatic` for true static methods
- Putting heavy initialization in companion object blocks

## Related concepts

- [Object declarations](/concepts/object-declarations.md)
- [Classes](/concepts/classes.md)
