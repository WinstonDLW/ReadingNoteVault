# Note Rules

Use these rules when creating or updating final notes.

Good notes transport source knowledge into the vault. They should feel
like reviewable knowledge shaped from the source.

## Dynamic Abstraction

Identify the reusable knowledge contributed by the source, then shape
the note around the relationships needed to understand that knowledge.

Let the central knowledge contribution control the note's scope.
Supporting knowledge, examples, and artifacts are explanatory tools
used to carry that contribution. Choose the smallest combination that
makes the knowledge understandable.

Let the source determine the note's structure. Its knowledge may be
best expressed through compact prose, a causal explanation, a
comparison, a sequence, a table, a diagram, or a combination of forms.

Select source material according to the role it plays in conveying the
knowledge. Preserve detail that carries reasoning, distinction, or
explanatory value. Compress background, narration, and repetition to
the amount needed for understanding.

## Locations

Source notes:

```text
1-notes/sources/source-<source-slug>.md
```

Concept notes:

```text
1-notes/concepts/<concept-slug>.md
```

Use stable, readable slugs.

## Metadata

Start each source note with:

```markdown
---
tags: [source]
created: YYYY-MM-DD
---
```

Start each concept note with:

```markdown
---
tags: [concept]
created: YYYY-MM-DD
---
```

When updating an existing note, keep the original created date.

## Source Notes

A source note summarizes the knowledge contribution of one source and
points to related concept notes.

It answers: what useful knowledge does this source add?

When mentioning a concept, link to its concept note.

For a scope centered on an existing or newly created concept note, keep
the source note brief: identify the concept and the source's
contribution in one or two compact sentences.

When one scope mainly introduces one concept, prefer one compact source
entry. Mention the source's angle on the concept. Put mechanisms,
examples, and detailed explanation in the concept note.

Place concept explanation inside concept notes. Place examples inside
concept notes when their purpose is to explain the concept.

Choose the note shape from the content and the user's preferences.
Possible shapes include compact prose, bullets, tables, diagrams,
flowcharts, numbered chains, or combinations.

## Concept Notes

A concept note teaches reusable knowledge independent of the source
where it was learned.

It captures the reusable idea and the relationships that make it
understandable and useful.

Write the body in source-neutral language. Keep source identity in
source references.

Open with the useful knowledge. Start with the central distinction,
problem, mechanism, or consequence that makes the concept worth
remembering.

Prefer source-grounded phrasing over newly invented slogans. Rewrite to
clarify the knowledge while preserving familiar source meaning.

When the source defines a technical relationship, notation, or
direction, preserve its subjects and direction explicitly. Use concrete
technical nouns when a pronoun or placeholder could make the
relationship unclear.

Use examples where they clarify the reasoning. Treat source examples as
the default source material to transform. Preserve, simplify,
generalize, or replace them according to the question step.

When the user asks to keep a source example or provides source images,
follow the source's explanation path for that example. Use the example
as the backbone of the relevant explanation, then add only the knowledge
needed to understand it.

When an example supports a concept, weave its relevant details into the
reasoning that explains that concept. Place each detail beside the
distinction, mechanism, or consequence it makes concrete. Organize
concept-note headings around the knowledge being learned and keep the
example within the relevant explanation.

Teach each relationship once. When an example can establish a
distinction or mechanism, let it carry that explanation and state the
abstraction where it becomes visible.

Place supporting knowledge where it advances the central concept. When
supporting knowledge has several useful treatments, present the options
at the question checkpoint: create or update an individual concept
note, integrate it into the central concept note, or keep it in the
source note.

## Reasoning Flow

Preserve the source's useful causal and explanatory relationships while
shaping them into a compact note. Problems should lead naturally to
their design responses, mechanisms should establish their consequences,
and examples should appear where they support the reasoning.

Preserve prerequisite relationships in the source's explanation.
Introduce the context, distinctions, and terms needed to understand a
mechanism before presenting the mechanism's consequences or artifacts.
Reorganize material when the new order retains those prerequisite
relationships and makes the knowledge easier to follow. Choose headings
that express the knowledge structure inferred from the source.

Use diagrams or flowcharts when they make the source logic easier to
understand than prose, tables, or the original source artifact.

When embedding a source image, show a short visible caption or filename
near the image so the user can identify it. Introduce what the reader
should notice in the image and connect it to the concept logic.

Embed source images as teaching artifacts. Establish the concepts,
terms, or scenario represented by an image immediately before embedding
it. Then state what the reader should examine and explain how its visual
relationships advance the concept.

Give prose, tables, diagrams, and other representations distinct roles.
Let each representation carry the information it expresses best, and
use nearby prose to interpret its contribution to the concept.

Give each part of an embedded visual a distinct job:

- the introduction establishes what the reader should inspect
- the image carries the visual structure
- the caption identifies the image's teaching role
- the follow-up states the conclusion revealed by the image

Choose headings and format from the concept's logic and the user's
preferences.

Check existing concept notes before creating a new one.

## Semantic Compression

After drafting, identify the unique knowledge carried by each
paragraph, list, table, and figure. Consolidate material that carries
the same distinction, relationship, mechanism, or consequence. Retain
the briefest clear representation or combination that preserves the
useful knowledge and reasoning. Prefer readable separation over reducing
word count through dense sentence structure.

Keep the note self-contained at the level of the extracted concept.
Use the source note as the route to source-specific detail, extended
examples, and complete context.

## Style

Keep notes clean, compact, and reviewable.

Use paragraphs, bullets, tables, diagrams, flowcharts, or numbered
chains according to what makes the knowledge easiest to understand.

Keep paragraphs short. Include background only when it directly explains
the knowledge.

Keep most sentences focused on one main distinction, relationship,
mechanism, or consequence. Split independent ideas into separate
sentences.

Use bullets for parallel distinctions, mechanisms, conditions, or
steps. Introduce the list with a complete sentence and give each item a
consistent grammatical form.

Preserve operational guidance when the source explicitly contributes a
procedure, decision method, condition, or failure response. Place it
where the source uses it in the explanation. Let consequences already
established by the concept explanation carry their practical meaning.

Preserve the source's intended meaning and teaching path when that path
carries the knowledge. Generated examples should follow from the user's
answer or from a missing/weak source example.

## Final Knowledge Check

Before saving a concept note, confirm that:

- the note retains the source's central knowledge contribution
- its structure reflects the useful reasoning inferred from the source
- supporting knowledge follows the agreed note boundaries
- enabling principles and mechanisms follow their agreed treatment
- examples function as explanation
- included images are introduced, captioned, and connected to the
  concept
- the placement of supporting knowledge, examples, and artifacts follows
  the proposed knowledge flow
- each section adds a new distinction, relationship, mechanism,
  consequence, or necessary explanation
- each representation contributes knowledge suited to its form
- repeated explanations have been consolidated
- background and example detail are proportional to their explanatory
  value
- prose sentences are complete and focused on one main relationship
- parallel reasoning uses a scannable and grammatically consistent
  structure
- technical subjects and dependency directions remain explicit
- the note contains the minimum source detail needed to understand the
  extracted concept
- the concept is understandable and reviewable on its own, while
  source-specific detail and complete context remain in the source

Create final notes directly.
