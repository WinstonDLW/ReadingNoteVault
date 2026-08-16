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

2. Read the requested scope.

   Identify the source logic, knowledge contribution, meaningful source
   content, possible note formats, and decisions that need the user's
   preference.

3. Prepare questions.

   Use `question-guide.md`. Briefly show the inferred logic, compact
   content inventory, and treatment plan. Separate rule-settled
   decisions from decisions that need user preference, then ask numbered
   questions only for the preference decisions.

4. Wait for the user's answer.

   Continue when the user answers or explicitly asks the assistant to
   use best judgment.

5. Generate final notes.

   Use `update-rules.md` when existing notes may be affected.
   Use `note-rules.md` for source and concept notes.
   Use `linking-rules.md` before adding Obsidian links.

6. Record the work.

   Use `log-rules.md`.

## System Shape

Source notes summarize a source's knowledge contribution and link to
concept notes.

Concept notes teach reusable knowledge.

The vault has no separate index files; source notes act as source
navigation.
