---
tags: [concept]
created: 2026-09-13
---
# Dependency Inversion Principle

Source code dependencies should favor stable abstract interfaces and avoid volatile concrete implementations.

## Stable Abstractions

Interface changes require changes to implementations, while implementation changes often leave interfaces unchanged. Stable interfaces therefore protect dependent code from implementation changes.

Dependencies on stable operating-system and platform facilities are tolerated. The concern is concrete modules under active development and frequent change.

- Add functionality to implementations without changing their interfaces where possible.
- Refer to abstract interfaces instead of volatile concrete classes. Avoid naming anything both concrete and volatile; this also constrains how objects are created.
- Do not derive from volatile concrete classes. In statically typed languages, inheritance is the strongest and most rigid source code relationship. It is less problematic in dynamically typed languages, but remains a dependency.
- Do not override concrete functions. Overriding inherits their dependencies; make the function abstract and provide multiple implementations instead.

## Abstract Factory

Creating an object requires a dependency on its concrete definition. An Abstract Factory confines that dependency to a concrete factory, allowing the application to create and use objects through interfaces.

**Example:** `Application` calls `ServiceFactory.makeSvc()`. Its implementation in `ServiceFactoryImpl` creates `ConcreteImpl` and returns it as a `Service`.

![[3-resource/clean-architecture-figure-11-1-abstract-factory.png]]

*Figure 11.1: The curved line marks the boundary between abstract and concrete components.*

The **abstract component** groups `Application`, which contains the business rules, with the `Service` and `ServiceFactory` interfaces. The **concrete component** contains `ConcreteImpl` and `ServiceFactoryImpl`.

- **Control flow:** `Application` calls the factory and service through their interfaces; the concrete implementations execute those calls.
- **Source dependencies:** `ServiceFactoryImpl` depends on `ServiceFactory`, and `ConcreteImpl` depends on `Service`.

The calls cross the boundary toward the implementations, while source dependencies point back toward the interfaces. This reversal is **Dependency Inversion**.

## Concrete Components

The dependency from `ServiceFactoryImpl` to `ConcreteImpl` still violates DIP. Such violations cannot be eliminated entirely; gather them into a small number of concrete components, separate from the rest of the system.

One such component is commonly `main`. In this example, `main` creates `ServiceFactoryImpl` and places it in a global variable typed as `ServiceFactory`, through which `Application` accesses the factory.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 11: DIP: The Dependency Inversion Principle
