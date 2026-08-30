# Note Rules

Use these rules when creating or updating final source and concept
notes after edit approval.

## Locations And Metadata

Source notes:

```text
1-notes/sources/source-<source-slug>.md
```

```markdown
---
tags: [source]
created: YYYY-MM-DD
---
```

Concept notes:

```text
1-notes/concepts/<concept-slug>.md
```

```markdown
---
tags: [concept]
created: YYYY-MM-DD
---
```

Use stable, readable slugs. Keep the original creation date when
updating an existing note.

## Source Notes

A source note records the source's knowledge contribution, provides a
route to the original source and processed scope, and links the concept
notes that carry reusable knowledge. For a scope centered on one concept,
add one or two compact sentences describing the source's angle. Keep
reusable mechanisms and explanatory examples in concept notes. Retain
material only in the source note when it is source-specific context or
navigation rather than reusable conceptual knowledge.

## Concept Notes

A concept note teaches reusable knowledge independently of the source.
Keep the body source-neutral and place source identity in source
references. Source-neutral writing removes dependence on the source's
narrative context while preserving its demonstrated knowledge.

Add a source reference when the source meaningfully teaches the
concept.

Let the central knowledge contribution control the note's scope. Use
supporting knowledge, examples, and artifacts only when they help carry
that contribution. Choose the smallest combination that makes the
knowledge understandable.

Treat the approved general note plan, supported by the internal content
inventory and treatments, as the note's content boundary. Give each
section a distinct knowledge contribution from that boundary. This
approved boundary, rather than the source's section hierarchy or
emphasis, determines inclusion in the concept note.

Derive the structure from the source's useful reasoning. Preserve
causal and prerequisite relationships. Introduce required context before
the mechanisms, consequences, and artifacts that depend on it.
Reorganize only when the new order preserves those relationships and
improves clarity.

Open with a direct thesis: state the distinction, problem, mechanism, or
consequence itself. Avoid introductory framing such as "this note
explains," "the source argues," or "the concept says" when the knowledge
can be stated directly. Include why the concept matters only when that
consequence adds necessary knowledge. State the core relationship in
plain language before introducing formal notation. Use notation when it
improves precision without obscuring the point. Preserve technical
subjects, relationship types, and relationship directions explicitly.
Prefer concrete nouns when a pronoun or placeholder could be unclear.

Preserve the source's technical vocabulary and distinctions. Use one
stable term for each concept. When the source changes terminology to
mark a broader abstraction, state that transition once. Define an
overloaded technical term when readers could mistake its ordinary
meaning for its role in the source.

### Examples And Supporting Knowledge

Transform source examples exactly according to the agreed treatment.
Compression keeps the details needed to carry the reasoning.
Generalization keeps the causal scenario with broader details. Omission
removes the scenario and retains only the knowledge it establishes.

When an example supports a concept, weave its details into the relevant
distinctions and mechanisms. Let the example carry relationships it
demonstrates instead of explaining them again separately. Organize
concept-note headings around the knowledge being learned.

Place supporting knowledge where it advances the central concept. When
its boundary remains open, follow the treatment agreed at the question
checkpoint.

When several source examples establish breadth, express the shared
category they demonstrate. Retain named technologies when they establish
a meaningful boundary or contrast.

### Visuals And Other Representations

Follow the agreed representation treatment. When it selects a visual,
connect the visual to the explanation and state its teaching point once.
Choose the minimum framing needed from an introduction, caption, or
follow-up. Add another element when it contributes a relationship that
the visual and existing explanation do not already make clear.

Treat a replacement visual as a change of medium. Preserve its agreed
semantic contract and apply only approved simplifications. Choose a
notation whose conventions match the represented knowledge. Distinguish
relationship types and label them when their meaning could be unclear.

Assign each relationship to the prose, example, table, diagram, code, or
other representation that expresses it most clearly. Let supporting
representations add context, evidence, mechanism, or consequence.

Render each generated visual before saving. Inspect its labels, layout,
entities, relationship types and directions, contrasts, and invariants.
Confirm that the rendered visual, surrounding explanation, source
artifact, and agreed semantic contract teach the same relationship.

### Compression And Style

Use the approved note plan and internal inventory to set the note's
knowledge budget. Assign each claim or relationship to one primary
passage or representation. After drafting, merge elements that answer the
same review question, carrying any unique detail into the clearest one.
Retain an additional representation when it adds a distinct relationship,
mechanism, or consequence.

Keep paragraphs short and sentences focused on one main relationship.
Prefer concise, assertive declarative prose. Remove unnecessary hedging,
filler transitions, and repeated framing. Preserve qualifiers required by
the source's scope, conditions, causality, or uncertainty; assertiveness
must not turn a conditional claim into a universal one. Split independent
ideas. Use concrete technical subjects. Use grammatically parallel bullets
when several ideas share the same explanatory frame.

Operational guidance must correspond to a procedure, diagnostic method,
decision criterion, condition, or failure response explicitly taught by
the source. Preserve its original function and place it where it
advances the explanation.

Keep the note self-contained by providing the minimum context and
reasoning needed to understand the extracted concept without reopening
the source. Use the source note as the route to source-specific detail,
extended examples, and complete context.

## Final Knowledge Check

Before writing final vault files, confirm:

1. **Knowledge:** The note retains the central contribution and required
   mechanisms.
2. **Flow:** Its structure follows the useful source reasoning and the
   approved general note plan.
3. **Treatment:** Supporting knowledge, examples, artifacts, links, and
   source references follow their agreed treatments.
4. **Representation fidelity:** Every representation preserves its
   approved entities, relationship types and directions, contrasts, and
   invariants. Generated visuals pass rendered inspection.
5. **Contribution:** Every section and representation adds unique
   knowledge, and each relationship has one clearest primary expression.
6. **Readability:** Sentences are complete, direct, concise, assertive,
   technically precise, and scannable.
7. **Compression:** The note contains the minimum detail needed to
   review the extracted concept independently, with no removable
   semantic overlap.
