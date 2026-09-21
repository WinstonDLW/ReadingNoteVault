---
tags: [concept]
created: 2026-09-21
---
# Architectural Boundaries

Architectural boundaries separate software elements and restrict their source dependencies. Dependencies point from replaceable details toward core business rules. This protects the rules from changes in those details.

Coupling to premature technical decisions increases development and maintenance effort. Drawing boundaries before coding can keep those decisions out of business logic. Frameworks, databases, and other details can then be chosen later.

## Draw Boundaries at Axes of Change

Draw a boundary at an **axis of change**: the components on either side change at different rates and for different reasons. The [[single responsibility principle|Single Responsibility Principle]] identifies these boundaries.

GUI and dependency injection frameworks change for different reasons than business rules. Separate them from the rules. Also separate the database from both the business rules and the GUI.

## Put the Database Behind an Interface

Business rules need functions to fetch and save data. They do not need database schemas or query languages.

The business-rules component owns `DatabaseInterface`, which `BusinessRules` uses. `DatabaseAccess` implements that interface and translates its calls into database operations. The access code therefore depends on the business-rules component.

The rules can be written and tested before storage is chosen. These class names represent roles; a real application may have many classes and interfaces in each role.

![[3-resource/clean-architecture-figure-17-1-database-interface.jpg]]

*Figure 17.1: `DatabaseAccess` implements the interface and controls the database. None of the other depicted classes depends on `DatabaseAccess`.*

Draw the boundary across the inheritance relationship, below `DatabaseInterface`:

- **Business-rules side:** `BusinessRules` and `DatabaseInterface`.
- **Database side:** `DatabaseAccess` and the actual database.

![[3-resource/clean-architecture-figure-17-2-database-boundary.jpg]]

*Figure 17.2: The interface dependency crosses the boundary. The dependency on the actual database stays on the database side.*

In Figure 17.3, `Database` names the component containing both the database engine and its access classes.

![[3-resource/clean-architecture-figure-17-3-database-component.jpg]]

*Figure 17.3: The component's access code depends on `BusinessRules`. The database engine itself does not.*

This dependency direction applies the [[dependency inversion principle|Dependency Inversion Principle]] and the Stable Abstractions Principle: lower-level details depend on higher-level abstractions.

## Treat GUI and Database as Plugins

IO is irrelevant to the business-rule model. The model can do its work without its presentation interface.

![[3-resource/clean-architecture-figure-17-4-gui-boundary.jpg]]

*Figure 17.4: The GUI depends on business rules. Business rules remain independent of the presentation technology.*

These boundaries form a **plugin architecture**. GUI, database, and other optional or replaceable components plug into independent core business rules.

![[3-resource/clean-architecture-figure-17-5-plugin-architecture.jpg]]

*Figure 17.5: Both GUI and database dependencies point toward the core business-rules component.*

Protection is **asymmetric**:

- Plugin implementation changes should not force business-rule changes.
- Business-rule interface changes may require updates to dependent plugins.

Replacing a plugin can require substantial work and revised communication with business rules. Boundaries make replacement practical. They do not guarantee unchanged interfaces.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 17: Boundaries: Drawing Lines
