---
tags: [concept]
created: 2026-09-27
---
# Business Rules

Entities contain application-independent business rules. Use cases contain application-specific rules that control how and when Entities are used.

Business rules make or save money for the business. They should be the system's most independent and reusable code. User interfaces, databases, and other technical concerns plug into them.

## Entities Bind Critical Rules and Data

- **Critical Business Rules** would exist and make or save money even without an automated system.
- **Critical Business Data** is the data those rules require. It would also exist without automation.

An **Entity** binds a small set of critical rules to critical data. It contains or readily accesses that data and exposes functions implementing the rules. It remains independent of databases, user interfaces, and third-party frameworks.

An Entity need not be an object-oriented class. A separate software module can bind the rules and data together.

**Loan example:** Charging interest is a critical rule whether software or a clerk calculates it. The loan balance, interest rate, and payment schedule are critical data.

![[3-resource/clean-architecture-figure-20-1-loan-entity.jpg]]

*Figure 20.1: Loan exposes payment, interest, and late-fee operations over its critical data.*

## Use Cases Control How Entities Are Used

A **use case** specifies an application's input, output, and processing steps. These rules apply to the automated application rather than a manual environment.

It describes the interaction between users and Entities. It does not prescribe the presentation technology or how data reaches the system.

A use-case object contains:

- Functions implementing the application-specific rules.
- Input and output data.
- References to the Entities it uses.

**Loan application example:** The use case controls when payment estimation may begin. The Customer Entity holds the critical rules governing the bank's relationship with its customers.

![[3-resource/clean-architecture-figure-20-2-loan-use-case.jpg]]

*Figure 20.2: The application workflow specifies data and processing without prescribing a UI.*

## Dependencies Point from Use Cases to Entities

Entities are higher level because they generalize across applications and sit farther from inputs and outputs. Use cases are lower level because they belong to a particular application and sit closer to its inputs and outputs.

Use cases depend on Entities. Entities know nothing of the use cases controlling them. This direction follows the [[dependency inversion principle|Dependency Inversion Principle]].

## Keep Request and Response Models Independent

A use case accepts a simple request data structure and returns a simple response data structure.

### No Technical Dependencies

These models have no web, UI, or framework dependencies. They do not inherit from interfaces such as `HttpRequest` or `HttpResponse`.

Dependencies in the models would indirectly bind the use case to those technologies. Use-case code should know nothing of HTML or SQL.

### No Entity References in the Models

Request and response models must not contain Entity references. These exchanged data structures are separate from the use-case object's own references to Entities.

Models and Entities serve different purposes and change for different reasons, even when their data looks similar. Coupling them violates the [[single responsibility principle|Single Responsibility Principle]] and Common Closure Principle. It leads to unnecessary data and conditionals.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 20: Business Rules
