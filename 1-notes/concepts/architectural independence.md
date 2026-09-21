---
tags: [concept]
created: 2026-09-20
---
# Architectural Independence

Decoupling layers and use cases allows parts of a system to change independently, supporting development, maintenance, deployment, and operation. Use cases, operational constraints, team structures, and deployment needs are incompletely known and change over time; good [[software architecture]] preserves options through well-isolated components.

## Decouple Layers and Use Cases

Supporting use cases is the architect's first priority. Expose them through prominent, clearly named classes, functions, or modules so the system's intent is visible without hunting for behavior.

Apply the [[single responsibility principle|Single Responsibility Principle]] and Common Closure Principle: separate things that change for different reasons and collect things that change for the same reasons.

- **Horizontal layers:** Separate UI, application-specific business rules, application-independent business rules, and database details, including query language and schema. These layers change at different rates and for different reasons, so each should be independently changeable.
- **Vertical use cases:** Keep different use cases separate within each layer. For example, the add-order and delete-order use cases change at different rates and for different reasons; keep their UI portions, business rules, and database functionality separate. Adding new use cases then becomes less likely to disturb existing ones.

## Distinguish True from Accidental Duplication

**True duplication** requires every change in one instance to be repeated in its copies. **Accidental duplication** looks similar but evolves at different rates or for different reasons. Eliminate true duplication; do not unify independent code merely because it resembles other code.

- Similar screens, algorithms, queries, or schemas in different use cases may diverge. Sharing them prematurely couples the use cases and makes later separation difficult.
- A database record and a screen view may have similar structures but change independently. Copy data into a separate view model instead of passing the database record directly to the UI.

## Three Decoupling Modes

Layers and use cases identify what to separate. Decoupling modes describe whether that separation is maintained at the source-code, deployable-unit, or service level.

| Mode | Independence | Execution and communication |
| --- | --- | --- |
| Source level | Control source dependencies so a module's changes do not force changes or recompilation elsewhere. | One executable and address space; components communicate through function calls. This can be a monolith. |
| Deployment level | Partition independently deployable units such as JARs, DLLs, or shared libraries, so one unit's source changes do not force others to be rebuilt and redeployed. | Units may share an address space and use function calls, or occupy separate processes and use interprocess communication, sockets, or shared memory. |
| Service level | Services depend on the data structures they exchange, while their source code and binaries can change independently. | Units communicate solely through network packets. |

## Keep the Decoupling Mode Open

Keep components independent of a particular communication mechanism so they can move between threads, processes, and services as operational needs change.

Defaulting to services encourages coarse-grained boundaries and, where service boundaries are unnecessary, wastes development effort, memory, and processing time.

One strategy is to make components separable into services while retaining them in one address space as long as possible. Source-level decoupling may suffice for the system's entire lifetime. Introduce deployment-level separation or selectively extract services when development, deployment, or operational needs justify it. For example, a system that initially fits on one server may grow to need some components on separate servers.

Declining operational demands may allow services to become deployable units or a monolith again. Architecture should protect most source code from these transitions and allow different deployment sizes to use different modes. Changing modes need not be a trivial configuration switch.

## Support Independent Development, Operation, and Deployment

- **Development:** Conway's law states that a system's design structure mirrors the communication structure of the organization that designs it. Decoupled layers and use cases reduce interference between teams, whether organized around features, components, or layers.
- **Operation:** Architecture must support each use case's required throughput and response time. Separated components with greater throughput or bandwidth needs can be distributed or replicated independently. Separate servers require service-level decoupling; components cannot depend on sharing an address space.
- **Deployment setup:** Aim for immediate deployment after building, without elaborate scripts, manual file setup, or configuration tweaks. Partition and isolate components, with master components responsible for starting, integrating, and supervising the system's components.
- **Independent deployment:** Sufficiently decoupled layers and use cases can be deployed independently and may be hot-swapped—replaced while the system is running.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 16: Independence
