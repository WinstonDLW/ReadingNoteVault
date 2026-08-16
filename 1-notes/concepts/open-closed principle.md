---
tags: [concept]
created: 2026-08-16
---

# Open-Closed Principle

A software artifact should be open for extension but closed for modification. Extensions should minimize changes to stable code.

At the architectural level, OCP is about dependency direction. Separate functionality by how, why, and when it changes. Make lower-level details depend on the higher-level policies that should be protected.

## Separate What Changes, Then Direct Its Dependencies

A system displays a financial summary on the web. A new requirement adds a print report with different presentation rules.

Report calculation and each presentation have different reasons to change:

- **Separate responsibilities:** The [[single responsibility principle|Single Responsibility Principle]] separates report calculation from web and print presentation.
- **Direct dependencies:** Dependency Inversion arranges source-code dependencies so a new presentation does not force changes to calculation policy.

The detailed design partitions the example into components. It places interfaces (`<I>`) so source-code dependencies cross each component boundary in one direction.

![[3-resource/Clean Architecture/Figure8.2 Partitioning the processes into classes and separating the classes into components.png]]

*Figure 8.2: Interfaces arrange source-code dependencies around the financial-report policy.*

An arrow from A to B denotes a source-code dependency. 

`FinancialDataMapper` implements `FinancialDataGateway`, so the mapper depends on the gateway. The gateway remains independent of the mapper. This keeps the interactor independent of the database implementation.

## Dependencies Create a Protection Hierarchy

If component A should be protected from changes in component B, component B should depend on component A. The arrows therefore point toward the more protected components.

![[3-resource/Clean Architecture/Figure 8.3 The component relationships are unidirectional.png]]

*Figure 8.3: Unidirectional dependencies protect higher-level components from lower-level changes.*

The interactor contains the application's business rules. It therefore receives the greatest protection. Changes to the database, controller, presenters, or views do not propagate into it.

## Interfaces Serve Two Protective Roles

| Role | Mechanism | Effect |
| --- | --- | --- |
| Directional control | A boundary interface reverses a dependency. The lower-level implementation then depends on the protected component. | Keeps policy independent of implementation details. |
| Information hiding | A boundary exposes only what a client directly needs. | Prevents clients from acquiring transitive dependencies on internal entities. |

`FinancialDataGateway`, `FinancialReportPresenter`, and the view interfaces control dependency direction. `FinancialReportRequester` hides the interactor's internal entities from the controller.

Directional control protects policy from lower-level implementations. Information hiding protects clients from internal changes.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 8: OCP: The Open-Closed Principle
