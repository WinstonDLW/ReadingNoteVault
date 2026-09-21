---
tags: [source]
created: 2026-08-11
---
# Clean Architecture

Source: *Clean Architecture: A Craftsman's Guide to Software Structure and Design* by Robert C. Martin.

Original: [[0-inbox/Clean Architecture A Craftsman Guide to Software Structure and Design.pdf|Book PDF]]

## Processed Scope

### Chapter 7: SRP: The Single Responsibility Principle

Introduces [[single responsibility principle|Single Responsibility Principle]] as a module responsibility principle based on actor-owned change pressure rather than "one thing per module."

### Chapter 8: OCP: The Open-Closed Principle

The [[open-closed principle|Open-Closed Principle]] protects higher-level policy from changes in lower-level details by separating functionality according to reasons for change and directing dependencies toward the policy.

### Chapter 9: LSP: The Liskov Substitution Principle

Extends the [[liskov substitution principle|Liskov Substitution Principle]] from inheritance to architectural interfaces: implementations are interchangeable only when they preserve the behavior expected by their users without implementation-specific exceptions.

### Chapter 10: ISP: The Interface Segregation Principle

The [[interface segregation principle|Interface Segregation Principle]] separates interfaces according to client needs. Depending on unused capabilities allows unrelated changes and failures to propagate through a system.

### Chapter 11: DIP: The Dependency Inversion Principle

The [[dependency inversion principle|Dependency Inversion Principle]] directs source dependencies toward stable business-rule abstractions, allowing them to oppose the flow of control. Unavoidable concrete dependencies are isolated from those rules.

### Chapter 15: What Is Architecture?

Defines [[software architecture|Software Architecture]] by its support for the system's life cycle, with the goal of minimizing lifetime cost and maximizing programmer productivity. Separating policy from details keeps technical decisions open while policy development proceeds.

### Chapter 16: Independence

[[architectural independence|Architectural Independence]] separates layers and use cases to support independent development, deployment, and operation. Distinguishing true from accidental duplication preserves that separation, while the choice of source-level, deployment-level, or service-level decoupling remains open to change.

### Chapter 17: Boundaries: Drawing Lines

[[architectural boundaries|Architectural Boundaries]] separate components that change for different reasons and direct source dependencies from replaceable details toward core business rules. This plugin structure defers technical decisions and protects business rules from changes in those details.
