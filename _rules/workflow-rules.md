# Workflow Rules

Use this controller whenever the user asks to generate notes from a
book, chapter, article, section, page range, or similar source scope.

The user reads first. The assistant reads the same scope afterward,
shows the proposed note decisions, asks preference questions, then
writes final notes.

Read this file first. Load other rule files only when the current step
needs them.

## Steps

1. Resolve source and scope.

   Identify the exact source and requested scope. Ask a short
   clarification question if either is unclear.

   When the user names a source without giving a path or URL, look for
   the original resource in `0-inbox/`. Use the original resource file as
   the reading authority.

   When the matching resource cannot be found in `0-inbox/`, ask the
   user for the file path, URL, or corrected source name.

2. Read the requested scope.

   Identify:

   - the source's knowledge contribution
   - the reasoning flow that makes that knowledge understandable
   - central and supporting concepts
   - enabling principles or mechanisms used to establish the central
     knowledge
   - examples and the roles they play in the explanation
   - diagrams and other teaching artifacts
   - background or context that directly supports the knowledge
   - possible note boundaries and treatments that need the user's
     preference

3. Prepare questions.

   Use `question-guide.md`. Briefly show the inferred logic, compact
   content inventory, item-to-treatment mapping, proposed note flow, and
   settled treatment. Separate rule-settled decisions from decisions
   that need user preference, then ask numbered questions only for the
   preference decisions.

4. Wait for the user's answer.

   Continue when the user answers or explicitly asks the assistant to
   use best judgment.

5. Generate final notes.

   Use `update-rules.md` when existing notes may be affected.
   Use `note-rules.md` for source and concept notes.
   Use `linking-rules.md` before adding Obsidian links.

   Draft from the inferred logic, content inventory, proposed knowledge
   flow, and agreed treatments.

   Before saving, reconcile the draft with the analysis and treatment
   plan:

   - compare the actual structure and order with the proposed note flow
   - confirm that supporting knowledge, examples, and artifacts appear
     at their planned reasoning points
   - identify the unique knowledge contributed by each section and
     representation
   - consolidate material that carries knowledge already established
     elsewhere in the note
   - confirm that every inventory item received its agreed treatment
   - confirm that prose sentences are complete and focused on one main
     relationship
   - split dense sentences when separation improves scanning
   - replace vague references with concrete technical subjects
   - express parallel reasoning with consistent bullets when that shape
     is clearer than prose

6. Record the work.

   Use `log-rules.md`.

## System Shape

Source notes summarize a source's knowledge contribution, link to
concept notes, and act as source navigation.

Concept notes teach reusable knowledge.
