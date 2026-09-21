---
tags: [concept]
created: 2026-09-20
---
# Software Architecture

Software architecture is the division of a system into components, their arrangement, and the ways they communicate. Its purpose is to support development, deployment, operation, and maintenance while minimizing lifetime cost and maximizing programmer productivity.

Architecture must support correct behavior, but poorly architected systems can still work correctly. Their difficulties emerge in continued development, deployment, and maintenance.

## Support the Whole Life Cycle

| Concern | Architectural support |
| --- | --- |
| Development | Make development easy for the teams doing it. Different team structures imply different architectural decisions; optimizing only for development can impair deployment, operation, and maintenance. |
| Deployment | Consider deployment early and aim to deploy with a single action. |
| Operation | Make use cases, features, and required behaviors visible as first-class entities so developers can understand the system. |
| Maintenance | Maintenance is the most costly life-cycle activity. Reduce **spelunking** (finding where and how to make a change) and the risk of unintended defects. Components isolated through stable interfaces clarify where future changes belong and reduce breakage. |

**Microservices trade-off:** Firm component boundaries and relatively stable interfaces can ease development, while numerous services complicate connection configuration and startup order. Considering deployment early may favor fewer services, a hybrid of services and in-process components, or more integrated management of interconnections.

## Separate Policy from Details

Structural value is greater than behavioral value because structure preserves the ability to change behavior. Keeping options open preserves this flexibility.

**Policy** embodies business rules and procedures, where the system's true value lives. **Details** enable humans, other systems, and programmers to communicate with policy without determining its behavior. They include IO devices, databases, web systems, servers, frameworks, and communication protocols.

Keep policy independent of details so it can be developed while decisions about those details remain open for as long as possible.

| Decision that can be deferred | Independence required of policy |
| --- | --- |
| Database | Policy does not care whether storage is relational, distributed, hierarchical, or flat files. |
| Web server or web delivery itself | Policy does not know that it is delivered over the web or depend on web technologies. |
| REST, microservices frameworks, or SOA frameworks | Policy is agnostic about its interface to the outside world. |
| Dependency injection framework | Policy does not care how dependencies are resolved. |

Deferring these decisions provides more information before commitment becomes necessary. Working policy independent of details permits experiments with different databases to check applicability and performance, or with different web systems and frameworks.

Even when an organization has already committed to a technology, shape the system so that choice can still be changed for as long as possible.

## Device Independence

Operating systems provide abstract IO services for unit records—records resembling punched cards. Programs call these services instead of controlling devices directly; operators configure the operating system to connect the services to particular devices. The same program can therefore use different unit-record devices without modification, illustrating the [[open-closed principle|Open-Closed Principle]].

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 15: What Is Architecture?
