---
tags: [concept]
created: 2026-09-27
---
# Clean Architecture

Clean Architecture separates higher-level policies from lower-level mechanisms. Its **Dependency Rule** requires source code dependencies to point inward, toward the policies.

Inner code must not name functions, classes, variables, or other software elements declared outside its layer. It must not use outer-layer data formats, especially framework-generated formats.

This separation keeps business rules independent of frameworks, UI, databases, and other external systems. The rules can be tested without external infrastructure, and obsolete external components can be replaced without disturbing them.

## Responsibilities of the Layers

| Layer, from inner to outer | Responsibility | Scope and change expectations |
| --- | --- | --- |
| **Entities** | Encapsulate enterprise-wide Critical Business Rules reusable across applications. | For a single application, these are its most general business rules. Application-operation changes, such as navigation or security changes, should not affect this layer. |
| **Use Cases** | Implement application-specific rules. Orchestrate data flowing to and from Entities and direct their rules toward use-case goals. | Changes to application behavior affect this layer, but should not affect Entities. Database, UI, and framework changes should not affect use cases. |
| **Interface Adapters** | Translate between formats convenient for Entities and use cases and formats needed by external systems. | Contains GUI MVC components and adapters for persistence or external services. Inner layers remain unaware of external formats. |
| **Frameworks and Drivers** | Supply external tools such as databases and web frameworks. | Contains low-level details, generally with only glue code connecting them to the next layer inward. |

Entities can be objects with methods or data structures with functions. Their business role and reuse matter, not an object-oriented representation. See [[business rules|Business Rules]] for the Entity/use-case distinction.

Four circles are schematic. A system may need more layers; the Dependency Rule still applies at every boundary.

### Adapter Responsibilities

- **GUI:** Presenters, views, and controllers belong in the interface-adapter layer. MVC models are likely data structures passed from controllers to use cases and back toward presenters and views.
- **Persistence and services:** Adapters convert internal data to persistence formats and external-service data to internal forms. Keep all SQL in the database-related adapters. Code farther inward must know nothing of the database.

## Cross Boundaries Without Reversing Dependencies

Control flows from Controller through Use Case Interactor to Presenter. The use case cannot directly depend on the outer Presenter. It calls an output-port interface owned by the inner use-case layer, and Presenter implements that interface.

This applies the [[dependency inversion principle|Dependency Inversion Principle]]. Dynamic polymorphism lets control cross outward while source dependencies across the boundary still point inward.

![[3-resource/clean-architecture-figure-22-1-clean-architecture.jpg]]

*Figure 22.1: Policies sit inside mechanisms; the inset distinguishes control flow from source dependencies.*

## Pass Data Convenient for the Inner Layer

Use isolated, simple structures across boundaries: structs, DTOs, function arguments, HashMap, or simple objects. Do not pass Entity objects or database rows through those boundaries. The structures must preserve the Dependency Rule.

A framework-generated database row would force inner code to know an outer format. Convert it into data convenient for the inner layer before crossing the boundary.

## Web-Based Java Scenario

Controller packages input gathered by the web server into plain Java `InputData`. `UseCaseInteractor` uses it to coordinate Entities and retrieves their data through `DataAccessInterface`. It gathers the results into plain Java `OutputData`.

`InputBoundary` and `OutputBoundary` keep these exchanges independent of the concrete Controller and Presenter. The diagram shows source dependencies, all of which cross boundaries inward.

![[3-resource/clean-architecture-figure-22-2-web-java-scenario.jpg]]

*Figure 22.2: Input, output, and data-access interfaces separate the interactor from web and database adapters.*

Presenter converts `OutputData` into a plain Java `ViewModel`. It formats dates and currency as strings and supplies button/menu labels and flags indicating whether they should be disabled. View then has little to do beyond placing that prepared data into HTML.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 22: The Clean Architecture
