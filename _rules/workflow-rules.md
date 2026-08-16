# Workflow Rules

Use this controller for requests to generate notes from a book, chapter,
article, section, page range, or similar source scope.

The user reads first. The assistant reads the same scope, negotiates the
note treatment, obtains edit approval, and then writes the notes.

Read this file first. Load the other rule files only when their step
needs them.

## Steps

1. Resolve source and scope.

   Identify the exact source and requested scope. When the user names a
   source without a path or URL, look for the original resource in
   `0-inbox/` and use it as the reading authority. Ask for clarification
   when the source or scope remains unresolved.

2. Read the requested scope.

   Use `question-guide.md` to identify the knowledge contribution,
   reasoning, meaningful content, possible note boundaries, and
   treatments that need user preference.

3. Present the question checkpoint.

   Follow `question-guide.md`. Show the inferred logic, inventory and
   treatment map, proposed note flow, settled decisions, and numbered
   preference questions.

4. Finalize and authorize the changes.

   After receiving the user's preferences or applying requested best
   judgment, restate the final treatment and files to be changed. Wait
   for explicit edit approval unless the user has already approved that
   exact change set.

5. Generate final notes.

   After approval, use `update-rules.md` for existing notes,
   `note-rules.md` for source and concept notes, and `linking-rules.md`
   for Obsidian links. Draft from the agreed treatment and proposed note
   flow.

6. Verify the result.

   Apply the Final Knowledge Check in `note-rules.md`. Reconcile the
   draft with the agreed inventory, treatments, and note flow before
   saving.

7. Record qualifying work.

   Use `log-rules.md` when the completed work meets its logging scope.

## System Shape

Source notes summarize a source's knowledge contribution and provide
source navigation. Concept notes teach reusable knowledge.
