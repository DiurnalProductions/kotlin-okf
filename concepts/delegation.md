---
id: kotlin.delegation
type: concept
title: Delegation
description: Composing behavior by forwarding to another object.
tags: [kotlin, object-model, delegation]
prerequisites:
  - kotlin.inheritance
  - kotlin.interfaces
related:
  - kotlin.object-declarations
  - kotlin.classes
resource: https://kotlinlang.org/docs/delegated-properties.html
timestamp: 2026-01-01
---

## Summary

Kotlin supports class delegation with `by` to implement interfaces by forwarding calls to a delegate instance.

## Mental model

Delegation is composition with compiler assistance: 'implement this interface by reusing that object.' It is often preferable to inheritance for reuse.

## Example

```kotlin
class CachedRepo(private val inner: Repository) : Repository by inner
```

## Common mistakes

- Delegating without understanding which methods are forwarded
- Hiding mutable delegate state unexpectedly
- Using inheritance when delegation would avoid fragile base classes

## Related concepts

- [Interfaces](/concepts/interfaces.md)
- [Object declarations](/concepts/object-declarations.md)
