---
id: kotlin.extension-functions
type: concept
title: Extension Functions
description: Adding functions to existing types without inheritance or modification.
tags: [kotlin, functions, extensions]
prerequisites:
  - kotlin.functions
  - kotlin.classes
related:
  - kotlin.functions
  - kotlin.classes
resource: https://kotlinlang.org/docs/extensions.html
timestamp: 2026-01-01
---

## Summary

Extension functions appear as members on a receiver type but are resolved statically as top-level functions.

## Mental model

Extensions are syntactic sugar for `Receiver.(args) -> Result` functions—they improve readability and API ergonomics without subclassing.

## Example

```kotlin
fun String.lastChar(): Char = this[length - 1]

"Kotlin".lastChar()
```

## Common mistakes

- Treating extensions as runtime polymorphism
- Defining extensions that should be members for cohesion
- Import abuse leading to ambiguous extensions

## Related concepts

- [Functions](/concepts/functions.md)
- [Classes](/concepts/classes.md)
