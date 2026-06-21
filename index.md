# Kotlin Knowledge Pack

Kotlin is a statically typed language emphasizing safety, expressiveness, immutability, and structured concurrency. This OKF knowledge pack models the Kotlin language itself—fundamentals, type system, object model, functional features, collections, coroutines, and build ecosystem—not application frameworks.

Framework-specific topics (Jetpack Compose, Ktor, Spring Boot, Android SDK) belong in separate knowledge packs.

## Start Here

New to Kotlin? Begin with immutability and explicit types, then null safety, then functions and classes. Add coroutines once synchronous Kotlin feels natural.

**Recommended first path:**

1. [Variables](/concepts/variables.md) → [val vs var](/concepts/val-vs-var.md) → [Type inference](/concepts/type-inference.md)
2. [Null safety](/concepts/null-safety.md) → [Nullable types](/concepts/nullable-types.md) → [Smart casts](/concepts/smart-casts.md)
3. [Functions](/concepts/functions.md) → [Lambdas](/concepts/lambdas.md) → [Classes](/concepts/classes.md)
4. [Collections overview](/concepts/collections.md) → [Immutable collections](/concepts/immutable-collections.md)
5. [Suspend functions](/concepts/suspend-functions.md) → [Structured concurrency](/concepts/structured-concurrency.md) → [Flows](/concepts/flows.md)

---

## Language fundamentals

* [Variables](/concepts/variables.md) - Named bindings that hold values
* [val vs var](/concepts/val-vs-var.md) - Read-only versus mutable declarations
* [Type inference](/concepts/type-inference.md) - Static types inferred from context
* [Any, Unit, and Nothing](/concepts/any-unit-nothing.md) - Root, unit, and bottom types
* [Null safety](/concepts/null-safety.md) - Compile-time null reference prevention
* [Smart casts](/concepts/smart-casts.md) - Compiler type narrowing after checks

## Type system

* [Nullable types](/concepts/nullable-types.md) - Explicit optional values with `?`
* [Safe calls](/concepts/safe-calls.md) - Null-safe member access with `?.`
* [Elvis operator](/concepts/elvis-operator.md) - Default values with `?:`
* [Sealed classes](/concepts/sealed-classes.md) - Finite closed type hierarchies
* [Enums](/concepts/enums.md) - Named constant enumerations
* [Data classes](/concepts/data-classes.md) - Value-oriented structured data
* [Inline value classes](/concepts/value-classes.md) - Lightweight domain wrappers

## Execution model

* [Compilation model](/concepts/compilation-model.md) - Source to platform artifacts
* [JVM relationship](/concepts/jvm-relationship.md) - Kotlin on the Java Virtual Machine
* [Bytecode](/concepts/bytecode.md) - JVM bytecode output
* [Kotlin Multiplatform overview](/concepts/kotlin-multiplatform.md) - Shared code across targets
* [Memory management](/concepts/memory-management.md) - High-level JVM allocation and GC

## Functional programming

* [Functions](/concepts/functions.md) - Named callable units
* [Function types](/concepts/function-types.md) - Types describing function signatures
* [Lambdas](/concepts/lambdas.md) - Anonymous function literals
* [Higher-order functions](/concepts/higher-order-functions.md) - Functions as parameters and results
* [Closures](/concepts/closures.md) - Capturing outer scope in lambdas
* [Extension functions](/concepts/extension-functions.md) - API extensions without subclassing

## Object model

* [Classes](/concepts/classes.md) - User-defined types with state and behavior
* [Interfaces](/concepts/interfaces.md) - Capability contracts
* [Inheritance](/concepts/inheritance.md) - Subclassing and implementation
* [Abstract classes](/concepts/abstract-classes.md) - Partial implementations
* [Delegation](/concepts/delegation.md) - Composition via `by`
* [Object declarations](/concepts/object-declarations.md) - Singleton objects
* [Companion objects](/concepts/companion-objects.md) - Class-scoped singletons

## Generics

* [Generic classes](/concepts/generic-classes.md) - Parameterized types
* [Variance](/concepts/variance.md) - Producer and consumer variance
* [Covariance](/concepts/covariance.md) - `out` producer variance
* [Contravariance](/concepts/contravariance.md) - `in` consumer variance
* [Star projections](/concepts/star-projections.md) - Unknown type arguments with `*`
* [Type erasure](/concepts/type-erasure.md) - JVM runtime generic limitations

## Collections

* [Collections overview](/concepts/collections.md) - Standard library collection hierarchy
* [Lists](/concepts/lists.md) - Ordered indexed collections
* [Sets](/concepts/sets.md) - Unique element collections
* [Maps](/concepts/maps.md) - Key-value associations
* [Immutable vs mutable collections](/concepts/immutable-collections.md) - Read-only interfaces versus mutation
* [Sequences](/concepts/sequences.md) - Lazy collection pipelines
* [Lazy evaluation](/concepts/lazy-evaluation.md) - Deferred computation

## Coroutines

* [Suspend functions](/concepts/suspend-functions.md) - Cooperative suspension points
* [Coroutine scope](/concepts/coroutine-scope.md) - Lifecycle boundaries for coroutines
* [Structured concurrency](/concepts/structured-concurrency.md) - Parent-child coroutine trees
* [Dispatchers](/concepts/dispatchers.md) - Thread pool routing
* [Cancellation](/concepts/cancellation.md) - Cooperative job cancellation
* [Flows](/concepts/flows.md) - Cold asynchronous streams

## Error handling

* [Exceptions](/concepts/exceptions.md) - Throwable-based exceptional control flow
* [Result type](/concepts/result-type.md) - Success/failure without throwing
* [Sealed state modeling](/concepts/sealed-state-modeling.md) - Exhaustive UI and domain states

## Ecosystem and modules

* [Packages](/concepts/packages.md) - Namespace organization
* [Multiplatform modules](/concepts/multiplatform-modules.md) - KMP source sets and modules
* [Gradle](/concepts/gradle.md) - Kotlin build orchestration
* [Dependencies](/concepts/dependencies.md) - Library coordinates and scopes
* [Maven ecosystem](/concepts/maven-ecosystem.md) - Repositories and artifact publishing

---

## Recommended learning progression

### Phase 1 — Language core

Variables and immutability → type inference → null safety chain (nullable types, safe calls, Elvis, smart casts) → Any/Unit/Nothing.

### Phase 2 — Types and data modeling

Sealed classes → enums → data classes → value classes.

### Phase 3 — Functions and objects

Functions → function types → lambdas → higher-order functions → closures → extension functions. In parallel: classes → interfaces → prefer delegation over inheritance.

### Phase 4 — Generics and collections

Generic classes → variance (covariance, contravariance) → star projections → type erasure. Collections → lists/sets/maps → immutable APIs → sequences → lazy evaluation.

### Phase 5 — Concurrency and errors

Suspend functions → coroutine scope → structured concurrency → dispatchers → cancellation → flows. Exceptions → Result → sealed state modeling.

### Phase 6 — Build and platform

Compilation model → JVM relationship → bytecode → memory management. Packages → multiplatform modules → Gradle → dependencies → Maven ecosystem. Kotlin Multiplatform when sharing code across targets.
