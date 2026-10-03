---
tags: [concept]
created: 2026-10-03
---
# Humble Object

The Humble Object pattern divides behavior between two modules or classes:

- **Humble module:** Keeps the hard-to-test behavior stripped down to its bare essentials.
- **Other module:** Contains the testable logic removed from the humble module.

This separation often defines an [[architectural boundaries|architectural boundary]]. Communication across it usually uses simple data structures. Keeping testable logic outside the humble module improves the testability of the system.

## Presenter and View

GUIs are hard to unit-test because checking the rendered screen is difficult. Most presentation behavior can be tested without rendering the GUI.

- **Presenter:** Accepts application data and prepares it for display in a simple **View Model**. It contains the testable presentation logic.
- **View:** Is the humble object. It moves prepared data from the View Model into the GUI without processing that data.

| Display concern | What Presenter puts in the View Model |
| --- | --- |
| Date | A string formatted for display. |
| Currency | A string with appropriate decimal places and currency markers; a boolean flag when negative values should appear red. |
| Buttons and menus | Name strings and boolean flags indicating whether controls should be disabled. |
| Radio buttons, checkboxes, and text fields | Appropriate name strings and boolean values. |
| Tables of numbers | Tables of properly formatted strings. |

Every application-controlled aspect of the screen is represented in the View Model as strings, booleans, or enums. The Presenter/View split supplies the presentation boundary in [[clean architecture|Clean Architecture]].

## Database Gateways

Database gateways are polymorphic interfaces between use-case interactors and the database. Their methods expose the create, read, update, and delete operations required by the application.

For example, `UserGateway.getLastNamesOfUsersWhoLoggedInAfter(Date)` accepts a date and returns a list of last names.

Gateway implementations in the database layer are humble objects. They perform the SQL or other database access needed by each method. SQL stays out of the use-case layer.

Interactors retain application-specific business rules and are not humble objects. They can be tested with stubs or test doubles that implement the gateway interfaces in place of real database access.

## Data Mappers

From their users' perspective, objects expose public operations and hide private data. Data structures expose public variables without implied behavior.

Tools called ORMs, such as Hibernate, load relational-table data into data structures. **Data mapper** therefore describes their role more precisely.

Data mappers belong in the database layer. They form another Humble Object boundary between gateway interfaces and the database.

## Service Boundaries

- **Outbound:** The application fills simple data structures. Boundary modules format that data and send it to external services.
- **Inbound:** Service listeners receive external data and convert it into simple structures. They pass those structures across the boundary to the application.

The communication machinery stays at the boundary, separate from the application's testable behavior.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 23: Presenters and Humble Objects
