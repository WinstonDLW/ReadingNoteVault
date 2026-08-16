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

A source note records the source's knowledge contribution and links the
concept notes that carry it. For a scope centered on one concept, add
one or two compact sentences describing the source's angle. Keep
mechanisms and explanatory examples in the concept note.

## Concept Notes

A concept note teaches reusable knowledge independently of the source.
Keep the body source-neutral and place source identity in source
references.

Add a source reference when the source meaningfully teaches the
concept.

Let the central knowledge contribution control the note's scope. Use
supporting knowledge, examples, and artifacts only when they help carry
that contribution. Choose the smallest combination that makes the
knowledge understandable.

Derive the structure from the source's useful reasoning. Preserve
causal and prerequisite relationships. Introduce required context before
the mechanisms, consequences, and artifacts that depend on it.
Reorganize only when the new order preserves those relationships and
improves clarity.

Open with the distinction, problem, mechanism, or consequence that
makes the concept worth remembering. Preserve technical subjects,
notation, and dependency direction explicitly. Prefer concrete nouns
when a pronoun or placeholder could be unclear.

### Examples And Supporting Knowledge

Transform source examples according to the agreed treatment. Preserve
the details that carry the source's reasoning.

When an example supports a concept, weave its details into the relevant
distinctions and mechanisms. Let the example carry relationships it
demonstrates instead of explaining them again separately. Organize
concept-note headings around the knowledge being learned.

Place supporting knowledge where it advances the central concept. When
its boundary remains open, follow the treatment agreed at the question
checkpoint.

### Visuals And Other Representations

Use a visual when it carries relationships more clearly than prose.
Establish its context before embedding it.

Give each part a distinct role:

- introduction: what the reader should inspect
- image: the visual structure
- caption: the image's teaching role
- follow-up: the conclusion revealed by the image

Prose, tables, diagrams, and other representations should contribute
different information. Let each carry what it expresses best.

### Compression And Style

After drafting, identify the unique knowledge carried by each section,
paragraph, list, table, and figure. Consolidate semantic repetition.
Retain the briefest clear representation that preserves the useful
knowledge and reasoning.

Keep paragraphs short and sentences focused on one main relationship.
Split independent ideas. Use concrete technical subjects. Use
grammatically parallel bullets when several ideas share the same
explanatory frame.

Preserve operational guidance when the source explicitly contributes a
procedure, decision method, condition, or failure response. Place that
guidance where it advances the explanation.

Keep the note self-contained at the level of the extracted concept. Use
the source note as the route to source-specific detail, extended
examples, and complete context.

## Final Knowledge Check

Before saving, confirm:

1. **Knowledge:** The note retains the central contribution and required
   mechanisms.
2. **Flow:** Its structure follows the useful source reasoning and the
   proposed note flow.
3. **Treatment:** Supporting knowledge, examples, artifacts, links, and
   source references follow their agreed treatments.
4. **Contribution:** Every section and representation adds unique
   knowledge.
5. **Readability:** Sentences are complete, focused, technically precise,
   and scannable.
6. **Compression:** The note contains the minimum detail needed to
   review the extracted concept independently.
