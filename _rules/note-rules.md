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
Summarize the core knowledge introduced in each scope, usually in one or
two sentences. State what the concept does, or use "introduces" when
appropriate. Describe the knowledge directly, rather than saying the source
"develops" it. Keep supporting examples in concept notes. The summary
provides knowledge and navigation, not an account of the author's presentation.

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

### Organize Before Drafting

After selection, internally reduce the retained content to its central
claim, essential relationships, and conditions. Identify what must be
explained before another point makes sense, and which claims each example
supports. Give each relationship one primary place in the note. Combine
source passages that establish the same relationship.

Use this structure to choose headings and representations, then draft from
it. Follow causal and prerequisite order, not the source's paragraph sequence
or a fixed note template. This is an internal step, not another questionnaire
or a detailed planning document.

### Explain The Knowledge

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
whose meaning could be unclear. Keep the essential explanation continuous;
do not make the reader assemble a mechanism from scattered captions.
Use captions to identify each figure's distinct contribution without
repeating the full explanation.

Render generated visuals in temporary storage before writing final vault
files. Inspect labels and layout, and compare the result and surrounding
explanation with the semantic contract and source artifact when present.
Follow the workflow's failure handling if rendering or verification fails.

### Compression And Style

Remove narrative setup, repeated motivation, transitional explanation, and
example detail that does not carry selected knowledge. Preserve technical
meaning and causal links; do not compress into slogans or disconnected keywords.

Merge elements that answer the same review question, preserving unique
detail. Additional sections or representations must carry distinct selected
knowledge. Avoid repeating a mechanism across an introduction, caption,
walkthrough, and conclusion.

Prefer simple subject-verb sentences with concrete technical subjects.
Express one main relationship per sentence. Do not reduce word count by
packing distinct claims into subordinate clauses or semicolon chains.
Keep each paragraph to one review point, usually one to three short
sentences. Use parallel bullets for comparisons, conditions, or distinct
steps; keep connected reasoning in short prose.

Preserve complete statements, causal links, and necessary qualifications
when splitting sentences. Avoid fragments, repeated setup, and extra
explanation. Remove filler and unnecessary hedging without turning
conditional claims into universal ones.

## Final Review

Complete both passes before writing or delivering the note. Fix findings
without waiting for the user to request another review. If a revision changes
meaning or selection, repeat the affected source check.

### Pass 1: Source And Selections

- Compare the draft with the source and resolved selections from
  `question-guide.md`. Preserve selected claims, examples, figures, necessary
  qualifications, and existing knowledge protected by `update-rules.md`.
  Unanswered choices block completion.
- Check the actual assertion: does the note state the source's relationship,
  including relevant subjects, direction, and conditions? Merely naming a
  concept or matching keywords is insufficient. Do not add background lessons
  to satisfy this check. Preserve the source's terminology and certainty.
- Check representations against their semantic contracts and source figures;
  inspect rendered generated visuals. Verify metadata, references, links,
  and asset targets.

### Pass 2: Read The Note Alone

- Follow the explanation in order. Are terms and prerequisites clear before
  use? Are examples attached to their claims? Can the mechanism be understood
  without piecing together scattered paragraphs and captions?
- Read each sentence for immediate understanding. Simplify overloaded clauses,
  split dense paragraphs, and make ambiguous subjects or relationships explicit.
- Remove repeated claims, unnecessary framing, and redundant recaps. Preserve
  distinct selected knowledge. If review still requires following the source's
  full explanatory journey, reorganize and distill the note.
- Check the source summary separately: it states core knowledge and provides
  navigation, without retelling supporting examples.
