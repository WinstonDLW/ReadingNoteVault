---
tags: [concept]
created: 2026-08-16
---

# Open-Closed Principle

The Open-Closed Principle says software should be easy to extend by adding behavior without forcing changes to existing code.

At the architectural level, this is not just a rule about classes. It is a rule about protecting higher-level policy from lower-level detail. Separate the parts that change for different reasons, then make source-code dependencies point toward the parts that should be harder to disturb.

## Financial Report Example

A system displays a financial summary on a web page. The page can scroll, and negative numbers appear in red.

Later, stakeholders ask for the same information as a printed report. The printed report needs pagination, headers, footers, column labels, and negative numbers in parentheses.

Some new code must exist for the printed report. OCP asks a sharper question: how much existing code must change?

The design response is to separate two responsibilities:

| Responsibility | Example behavior | Why it changes |
| --- | --- | --- |
| Calculate reportable data | inspect financial data and produce report data | business and reporting policy |
| Present reportable data | format for web, screen, PDF, or print | delivery medium and presentation rules |

If calculation and presentation are tangled together, adding the printed report forces edits through existing web-report code. If they are separated, the printed report can be added as another presentation path.

## Dependency Direction

The separation is not enough by itself. The dependencies must point toward the code that should be protected.

Figure 8.3 The component relationships are unidirectional

![[3-resource/Clean Architecture/Figure 8.3 The component relationships are unidirectional.png]]

In this dependency hierarchy, lower-level details depend on higher-level policy:

| Protected component | Protected from changes in |
| --- | --- |
| Financial Report Interactor | database, controller, presenters, views |
| Financial Report Controller | presenters and views |
| Screen Presenter / Print Presenter | web view and PDF view |

The interactor deserves the most protection because it contains the application business rules. Views and databases are lower-level details because they are more likely to change for peripheral reasons.

The rule is:

```text
If component A should be protected from changes in component B,
then component B should depend on component A.
```

## Directional Control

Making dependencies point the right way often adds interfaces. The extra interfaces are not ceremony; they prevent higher-level code from naming lower-level implementations.

Figure 8.2 Partitioning the processes into classes and separating the classes into components

![[3-resource/Clean Architecture/Figure8.2 Partitioning the processes into classes and separating the classes into components.png]]

For example, an interactor should not depend directly on the database mapper. A gateway interface lets the database side depend inward instead. Presenter and view interfaces serve the same purpose for output paths.

This is dependency inversion in service of OCP: invert a dependency when the natural source-code direction would make stable policy depend on volatile detail.

## Information Hiding

Some interfaces protect against a different problem: knowing too much.

A controller may need to request a report without depending on the internal entities used by the interactor. A narrow request interface hides those internals. This prevents transitive dependencies, where a component becomes indirectly coupled to things it does not directly use.

Information hiding supports OCP because code is easier to extend when each component knows only the part of another component that it actually needs.

## Use It When

- adding a new output format requires editing existing output code
- business rules depend on UI, database, framework, or delivery details
- lower-level implementation changes ripple into higher-level policy
- a component mentions classes it does not directly need
- extension repeatedly means modification instead of addition

## Source Reference

- [[source-clean-architecture|Clean Architecture]], Chapter 8: OCP: The Open-Closed Principle
