# Question Guide

Use after reading the requested scope and before drafting notes. Show what
the source contains and ask what to keep. Never infer user preferences.

## Analyze The Source

Identify every distinct knowledge point in the requested scope: definitions,
reasoning, mechanisms, supporting explanations, examples, qualifications,
practices, and figures or other artifacts. Account for all meaningful
points, not every sentence. Combine repetitions of the same claim. Analyze
points individually, but group related optional content for user decisions.
Keep core knowledge separate from optional support. Preserve source order
within the core overview and optional groups so the material is recognizable.

For each point, identify its role and what it contributes. Distinguish its
role in the source from the user's inclusion decision; a source heading,
lengthy discussion, or relevance to the main topic does not make it core.

Qualifications required for accuracy are mandatory whenever their claim
is retained. Only material whose inclusion, compression, or omission leaves
the central contribution accurate and understandable is optional.

Separate the main claim and its essential relationships from the examples,
supporting explanations, and implementation details used to teach them.
Being relevant to the main topic does not make a full supporting treatment
mandatory or remove the need to ask about it.

## Present The Checkpoint

### Core Knowledge

Present a short overview of the core claims and essential relationships,
marked as retained. Include significance only when the source explains it.
Do not ask the user to select these again. Required qualifications accompany
their claims, including optional claims if selected; they are not extra
decisions. Do not label optional support as core to avoid asking about it.

### Optional Content Groups

Compare the core overview and optional groups against each source section
for missing claims, including comparisons and priorities. Listing a
mechanism does not also capture why it matters. Cover all meaningful
content without turning every extracted point into a separate question.

Give one choice per coherent example or supporting explanation. Group its
related stages, consequences, and figures together. List the contents
concisely, including figure numbers and teaching points, so a group decision
has a clear scope. Keep unrelated examples or contributions separate; do
not use broad chapter headings to hide separate choices. There is no fixed
group count. Present the groups before proposing the final note organization:

| No. | Content included | Role and contribution | Selection |
| --- | --- | --- | --- |
| 1 | Recognizable example or explanation, its related points and figures | What this group explains or supports | Keep or omit? |

Use concrete roles such as example, supporting explanation, practice, or
figure, and state what the group contributes. Use source section names
where they aid recognition. State dependencies on other groups beside the
choice. Keep optional examples separate from the core claims they illustrate.

Apply the terminology and style rules in `note-rules.md`. Give enough
source context to recognize each group's actual knowledge without reopening
the chapter.

### Preference Decisions

Ask which optional groups to keep, allowing answers by table number. The
table supplies the questions; do not repeat it as another questionnaire.
Ask only about inclusion. Do not ask for brief versus detailed treatment,
sentence counts, prose versus bullets, or separate-note placement. Apply
the writing rules to retained points and show organization in the final
plan after selection.

Each optional group needs an explicit keep/omit answer or scoped delegation.
The answer covers its listed contents; do not ask again for each subpoint.
Allow exceptions such as "keep 2 without the customer story" or "keep the
example without its figures." Apply explicit exceptions before group
defaults. A recommendation is not an answer. Do not infer selection from
existing notes, previous agent choices, concision preferences, or a general
generation request. Unmentioned groups remain unresolved unless the user
explicitly settles the remainder, for example "omit the rest."

Before drafting, check coverage and resolve selections to individual
contents, associated figures, required qualifications, and user exceptions.
Resolve partial or conflicting answers; never silently discard selected
knowledge or supply an omitted dependency. Follow `workflow-rules.md` to
wait and obtain approval. If there are no optional groups, show the core
overview and proceed to the final plan without inventing questions.

### Artifacts

An artifact is a diagram, image, table, code example, or other
representation. Keeping an example also keeps its associated source figures
by default, unless the user explicitly excludes them. List those figures
inside the example's group with their teaching points; do not create extra
figure questions. Omitting the example also omits its figures unless another
retained group needs them. A standalone artifact without a parent example
can be its own optional group or join a directly related explanation;
identify it explicitly in either case.

Use selected source artifacts as the default. Apply `note-rules.md` for
presentation and show proposed replacements in the final plan. Do not
bundle inclusion with choices about medium or note placement.

For each retained or replacement artifact, record a compact **semantic
contract**: its teaching claim, essential entities, relationship types and
directions, contrasts, invariants, and approved simplifications, as
applicable. Show the teaching claim and any knowledge-affecting
simplifications in the final plan; preserve the user's selected knowledge.

If a selected source visual is accessible and no vault asset exists, plan
its extraction. Request an asset only when the source visual is
inaccessible or a different version is wanted.
