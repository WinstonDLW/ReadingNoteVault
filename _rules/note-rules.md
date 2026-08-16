# Note Rules

Use these rules when creating or updating final notes.

Good notes transport source knowledge into the vault. They should feel
useful for review, not like rewritten chapters, invented essays, or
filled templates.

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

Place concept explanation inside concept notes. Place examples inside
concept notes when their purpose is to explain the concept.

Choose the note shape from the content and the user's preferences.
Possible shapes include compact prose, bullets, tables, diagrams,
flowcharts, numbered chains, or combinations.

## Concept Notes

A concept note teaches reusable knowledge independent of the source
where it was learned.

It answers: what is this idea, how does it work, and when is it useful?

Write the body in source-neutral language. Put source identity only in
source references.

Open with the central distinction, rule, mechanism, or consequence
rather than repeating the title.

Prefer source-grounded phrasing over newly invented slogans. Rewrite to
clarify the knowledge, not to create a new expression the user must
learn again.

Use examples where they clarify the reasoning. Treat source examples as
the default source material to transform. Preserve, simplify,
generalize, or replace them according to the question step.

When the user asks to keep a source example or provides source images,
follow the source's explanation path for that example. Use the example
as the backbone of the relevant explanation, then add only the knowledge
needed to understand it.

Integrate supporting knowledge where it explains the core concept.
Use a separate supporting-knowledge section as a fallback when the user
asks for it or when integration would make the concept harder to follow.

Use diagrams or flowcharts when they make the source logic easier to
understand than prose, tables, or the original source artifact.

When embedding a source image, show a short visible caption or filename
near the image so the user can identify it.

Choose headings and format from the concept's logic and the user's
preferences.

Check existing concept notes before creating a new one.

## Style

Keep notes clean, compact, and reviewable.

Use paragraphs, bullets, tables, diagrams, flowcharts, or numbered
chains according to what makes the knowledge easiest to understand.

Keep paragraphs short. Include background only when it directly explains
the knowledge.

Preserve the source's intended meaning and teaching path when that path
carries the knowledge. Generated examples should follow from the user's
answer or from a missing/weak source example.

Create final notes directly.
