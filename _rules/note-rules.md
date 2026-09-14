# Note Rules

Use these standards when planning, creating, or updating notes. Follow
`workflow-rules.md` for authorization and routing.

## Reading Note Standard

A reading note distills selected knowledge for quick review after reading
the resource. The reader should recover the central claim, its essential
reasoning, and its conditions with substantially less reading effort.
Preserve knowledge, not the source's paragraph sequence or full teaching
explanation. A paragraph-by-paragraph paraphrase fails this standard even
when accurate and shorter than the source.

Start with the core claim. Organize the remaining knowledge into compact
relationships, distinctions, conditions, or source-taught rules. Use short
prose, bullets, or a table according to the knowledge; changing prose into
bullets without distilling it is not compression. The user selects which
points to retain; these rules govern their concision, wording, and format.
Keeping a point or example does not require its full source explanation.

## Locations And Metadata

| Artifact | Location | Required tag |
| --- | --- | --- |
| Source note | `1-notes/sources/source-<source-slug>.md` | `source` |
| Concept note | `1-notes/concepts/<concept-name>.md` | `concept` |
| Final asset | `3-resource/<source-slug>-<descriptive-name>.<ext>` | None |

Both note types use YAML frontmatter with `tags: [source]` or
`tags: [concept]` and `created: YYYY-MM-DD`. Use the local creation date
for new notes; preserve existing creation dates and filenames.

For new files, use lowercase, hyphen-separated source slugs and asset
names. Concept filenames use the lowercase standard concept name with
spaces, following existing notes. Avoid invalid filename characters and
resolve collisions without overwriting unrelated content. Reuse suitable
existing assets. Temporary artifacts follow `AGENTS.md`.

## Source Notes

A source note records the source's contribution and provides navigation.
Identify the title and author when available, link the original file or
URL, and record each processed scope with links to its concept notes.
For scope centered on one concept, use one or two sentences describing
the source's angle. Keep reusable mechanisms and explanatory examples in
concept notes; retain only source-specific context and navigation here.

## Concept Notes

A concept note captures reusable knowledge independently of the source's
narrative. Keep the body source-neutral and put provenance in a source
reference linking the source note and identifying the relevant chapter,
section, or pages. Include a reference when that source meaningfully
teaches the concept. Distinguish printed page numbers from file page
indices when they differ.

Follow the approved content changes and the preservation rules in
`update-rules.md`. Let the central contribution control scope, not the
source's headings or emphasis. Abstract knowledge from the resource,
retaining the essential relationships and conditions needed to review the
selected concept. Independent review does not require reproducing the full
lesson or walkthrough. Do not estimate or ask about the user's background
knowledge, or add prerequisite teaching to fill assumed gaps. Use source
references for full explanations and unretained detail.

Preserve causal and prerequisite relationships while organizing for quick
retrieval of the selected knowledge. Combine source passages that establish
one relationship; retain essential reasoning without repeating each step
of the source's exposition. Organize headings around knowledge.

Open with a direct thesis: state the distinction, problem, mechanism, or
consequence itself. Avoid framing such as "this note explains" or "the
source argues" when knowledge can be stated directly. Include why it
matters when that consequence adds necessary knowledge. Explain the core
relationship plainly before using notation; use notation for precision.
Make technical subjects and relationship types and directions explicit.

In notes and selection checkpoints, preserve the resource's terminology,
named entities, technical distinctions, tone, and degree of certainty.
Use its recognizable terms rather than new umbrella labels. Distill the
prose while retaining its directness; remove narrative padding and added
commentary. Use one stable term per concept; explain once when terminology
changes to mark a broader abstraction. Define overloaded terms using their
meaning in the resource when ambiguity would distort the knowledge.

### Examples And Supporting Knowledge

Apply the user's inclusion decisions:

- **Retained point:** Distill its claim and essential reasoning without
  dropping distinct selected knowledge.
- **Retained example:** Keep the source's scenario and the minimum details
  that demonstrate its selected teaching point. Do not add a walkthrough
  merely because the user kept the example.
- **Omitted example:** Remove its scenario while preserving independently
  selected claims it establishes.
- **Omitted point:** Exclude it from the new content. Preserve independently
  selected knowledge and existing knowledge protected by `update-rules.md`.

Weave retained examples and supporting points into the relationships they
explain. Combine repeated claims across examples while preserving the
distinct contribution of each selected example. Keep source names and
details that establish a meaningful boundary or contrast.

Operational guidance must correspond to a procedure, diagnostic method,
decision criterion, condition, or failure response explicitly taught by
the source. Preserve its function and place it where it advances the
explanation.

### Visuals And Other Representations

Follow the selected artifacts, final plan, and semantic contract defined
in `question-guide.md`. A replacement visual changes the medium while
preserving that contract. Use suitable notation and label relationships
whose meaning could be unclear. Connect visuals to the explanation with
the minimum introduction, caption, or follow-up needed.

Render generated visuals in temporary storage before writing final vault
files. Inspect labels and layout, and compare the result and surrounding
explanation with the semantic contract and source artifact when present.
Follow the workflow's failure handling if rendering or verification fails.

### Compression And Style

Before composing prose, reduce the agreed content to its claims, essential
relationships, and necessary qualifications. Draft from that distilled
content, not by rewriting each source paragraph. Remove narrative setup,
repeated motivation, transitional explanation, and example detail that
does not carry selected knowledge. Preserve technical meaning and causal
links; do not compress into vague slogans or disconnected keywords.

Give each claim or relationship one clearest primary expression in prose,
an example, table, diagram, code, or another representation. Merge elements
that answer the same review question, preserving unique detail. Keep an
additional section or representation only when it carries distinct,
confirmed knowledge. Do not explain the same mechanism in an introduction,
caption, walkthrough, and concluding paragraph. A retained example should
carry its selected teaching point with the least detail that preserves it.

Keep paragraphs short and sentences focused on one main relationship.
Use complete, direct, concise, assertive declarative prose and concrete
technical subjects. Remove unnecessary hedging, filler, and repeated
framing. Preserve qualifiers required by scope, conditions, causality,
or uncertainty; never turn conditional claims into universal ones. Split
independent ideas; use parallel bullets for ideas sharing a frame.

## Final Knowledge Check

Before writing final vault files, confirm:

1. **Knowledge:** Central claims, required mechanisms, accuracy-critical
   qualifications, and existing knowledge protected by the update rules
   are preserved.
2. **Flow:** Structure preserves useful reasoning and follows the approved
   changes.
3. **Selection:** All meaningful source points were presented with their
   roles and contributions. Every optional point has an explicit inclusion
   decision or scoped delegation; the draft preserves the selected knowledge.
   An unanswered inclusion question fails this check.
4. **Fidelity:** Representations meet their semantic contracts; generated
   visuals pass rendered inspection.
5. **Distillation:** The note enables substantially faster review of the
   selected knowledge. If it still follows source paragraphs or requires
   reading through a similar explanatory journey, redraft it. Added lessons,
   commentary, and repeated explanations are removed. Do not shorten by
   dropping confirmed knowledge or accuracy-critical qualifications.
6. **Readability:** Prose is complete, direct, concise, technically precise,
   and scannable; source terminology and tone are preserved, and the concept
   can be reviewed independently.
7. **Navigation:** Required metadata and scope references are present;
   note links, source routes, and asset embeds resolve to intended targets.
