---
tags: [concept]
created: 2026-09-27
---
# Screaming Architecture

An application's top-level directories and highest-level source files should reveal its purpose and use cases, rather than its frameworks. The architecture should provide the structures those use cases need.

The repository should suggest a health care, accounting, or inventory management system, rather than merely Rails, Spring/Hibernate, or ASP.

New developers should be able to learn the system's use cases before knowing how it is delivered. Views and controllers can remain details to decide later.

## Keep Technology and Delivery Decisions Open

Decouple use cases from frameworks, databases, web servers, and other peripheral concerns. This allows those choices to be deferred and makes them easier to change later.

The web is a delivery mechanism, an IO device. It should not dominate the system's structure. Defer even the choice to deliver over the web where possible.

Keep the architecture as independent of delivery as possible. Console, web, thick-client, and web-service delivery should be possible without undue complication or changes to the fundamental architecture.

## Use Frameworks as Tools

Frameworks can be powerful and useful, but they should not supply the architecture. Their examples often assume pervasive adoption, allowing the framework to do everything.

Evaluate each framework's benefits and costs skeptically. Decide how to use it and protect the system from it. Develop a strategy that preserves the use-case emphasis and prevents the framework from taking over the architecture.

## Test Business Behavior Without Infrastructure

Unit-testing use cases should not require frameworks, a running web server, or a connected database.

Keep [[business rules|Entities]] as plain objects without framework or database dependencies. Use-case objects coordinate those Entities. Their behavior should also be testable together without framework complications.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 21: Screaming Architecture
- Referenced in that chapter: Ivar Jacobson, *Object Oriented Software Engineering: A Use Case Driven Approach*, for architecture as structures that support use cases.
