# Note Rules

Use these rules when creating or updating final notes.

Good notes transport source knowledge into the vault. They should feel
like reviewable knowledge shaped from the source.

## Dynamic Abstraction

Identify the reusable knowledge contributed by the source, then shape
the note around the relationships needed to understand that knowledge.

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

Use examples where they clarify the reasoning. Treat source examples as
the default source material to transform. Preserve, simplify,
generalize, or replace them according to the question step.

When the user asks to keep a source example or provides source images,
follow the source's explanation path for that example. Use the example
as the backbone of the relevant explanation, then add only the knowledge
needed to understand it.

Place each example beside the idea it makes concrete. Let it carry the
explanation across the relevant reasoning stages, preserving the
details that clarify the mechanism. Give an example its own heading
when the example itself is the knowledge being taught.

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

Reorganize material when that improves clarity while keeping the logic
needed to understand the knowledge. Choose headings that express the
knowledge structure inferred from the source.

Use diagrams or flowcharts when they make the source logic easier to
understand than prose, tables, or the original source artifact.

When embedding a source image, show a short visible caption or filename
near the image so the user can identify it. Introduce what the reader
should notice in the image and connect it to the concept logic.

Embed source images as teaching artifacts. Place each image where it
advances the explanation, state what the reader should examine, and
explain the knowledge carried by its visual relationships.

Give prose, tables, diagrams, and other representations distinct roles.
Let each representation carry the information it expresses best, and
use nearby prose to interpret its contribution to the concept.

Choose headings and format from the concept's logic and the user's
preferences.

Check existing concept notes before creating a new one.

## Style

Keep notes clean, compact, and reviewable.

Use paragraphs, bullets, tables, diagrams, flowcharts, or numbered
chains according to what makes the knowledge easiest to understand.

Keep paragraphs short. Include background only when it directly explains
the knowledge.

Fold practical use signals into the concept explanation as conditions,
tests, consequences, or design responses.

Preserve the source's intended meaning and teaching path when that path
carries the knowledge. Generated examples should follow from the user's
answer or from a missing/weak source example.

## Final Knowledge Check

Before saving a concept note, confirm that:

- the note retains the source's central knowledge contribution
- its structure reflects the useful reasoning inferred from the source
- supporting knowledge follows the agreed note boundaries
- examples function as explanation
- included images are introduced, captioned, and connected to the
  concept
- each section and representation contributes distinct knowledge
- repeated explanations have been consolidated
- background and example detail are proportional to their explanatory
  value
- the result is meaningfully more compact than an explanatory source
- the note can be reviewed efficiently without returning to the source

Create final notes directly.
