# Workflow Rules

Read this controller first. Load each supporting rule file when needed;
reuse it during the task unless it changes.

## Routing

- For source-based extraction or substantive knowledge changes, use the
  full workflow below. The user reads first; the assistant reads the same
  scope.
- For wording, formatting, links, or layout maintenance, apply the relevant
  writing, linking, and update rules directly within the user's request.
  Preserve meaning; raise any proposed knowledge change before making it.
- For rule reviews or edits, inspect and change the requested rules
  directly. The note-generation checkpoint and source logs do not apply.

Show the source's meaningful points, their roles and contributions, and
keep/omit choices before proposing the final note organization. Keep
technical bookkeeping, semantic-contract details, paths, logging decisions,
and successful verification internal unless requested. Content selection
belongs to the user; compression and formatting follow `note-rules.md`.
Report verification failures and deviations.

## Steps

1. **Resolve and read the source scope.** Identify the exact source and
   scope. Without a supplied path or URL, look in `0-inbox/` for the
   original reading authority. Ask when the source or scope remains
   unresolved; do not substitute remembered content for inaccessible text.

2. **Analyze and discover.** Use `question-guide.md` to analyze the scope.
   Use Discovery Before Approval in `update-rules.md` to find matching
   notes, and Locations And Metadata in `note-rules.md` to resolve
   prospective paths. Apply the note-writing principles when planning.

3. **Ask and wait.** Follow `question-guide.md` to present all meaningful
   source points and their roles, then ask which optional points to keep.
   Include examples, supporting explanations, and source artifacts in this
   selection checkpoint. Unanswered questions block note drafting and final
   vault writes. Stop and wait for the user's
   answers; continue only independent source reading or discovery. Do not
   choose a recommended option on the user's behalf or treat silence,
   a preselected option, an empty tool response, or elapsed time as an answer.

4. **Plan and authorize.** After selection, give a compact final plan showing
   how the core knowledge and retained points will be organized into notes
   and representations. Follow `note-rules.md` for concision; do not reopen
   selection as questions about depth or formatting. The selections and
   approved plan define the content changes. Authorization to write files
   does not answer content questions. Obtain edit approval unless existing
   authorization covers these confirmed changes. Answers accompanied by
   "go ahead" authorize the resulting plan when they fully determine it;
   state that plan and proceed. Otherwise present the resolved plan for
   approval. Reuse approval of an unchanged plan. Ask again only for
   unresolved content choices or changes outside the authorized scope.
   Permission to use judgment settles only choices explicitly delegated
   for this scope; by itself it does not authorize file edits.

5. **Draft and verify.** Apply Integration After Approval in
   `update-rules.md`, the writing rules and Final Knowledge Check in
   `note-rules.md`, and `linking-rules.md`. Resolve checks before writing
   final files. If a check cannot be completed, report the limitation and
   leave the affected artifact and dependent changes unresolved. Do not
   claim verification passed or silently substitute another representation.

6. **Write and log.** Write verified notes and assets to their vault
   locations. Apply `log-rules.md` to completed changes.
