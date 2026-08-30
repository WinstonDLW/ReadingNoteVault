---
tags: [concept]
created: 2026-08-17
---
# Liskov Substitution Principle

Code written against a type should behave the same when an object of that type is replaced by an object of a subtype. A replacement that changes the program's behavior violates the Liskov Substitution Principle, regardless of the declared subtype relationship.

## Behavior Defines the Subtype

`Billing` calls `calcFee()` through `License`. `PersonalLicense` and `BusinessLicense` use different fee algorithms, yet `Billing` behaves the same with either subtype.

![[3-resource/Clean Architecture/Figure 9.1 License, and its derivatives, conform to LSP.png]]

## A Declared Subtype Can Change Program Behavior

`Rectangle` allows width and height to change independently. `Square` must keep them equal. Figure 9.2 declares a subtype relationship that conflicts with these operations.

![[3-resource/Clean Architecture/Figure 9.2 The infamous square rectangle problem.png]]

A program defined in terms of `Rectangle` may rely on this sequence:

```text
r.setW(5)
r.setH(2)
assert r.area() == 10
```

If `r` is a `Square`, changing the height also affects the width, so the assertion fails. Detecting `Square` with a special case makes the program's behavior depend on the concrete type. `Square` is therefore not substitutable for `Rectangle`.

## LSP Scales to Architecture

LSP applies wherever code depends on an abstraction implemented in multiple ways. The abstraction may be a class, interface, method convention, or service protocol.

When an implementation violates the behavior promised by the abstraction, dependent code must recognize and handle it separately. Each exception adds conditionals, configuration, or other compensating mechanisms. As exceptions accumulate, implementation-specific complexity spreads into the architecture.

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 9: LSP: The Liskov Substitution Principle
