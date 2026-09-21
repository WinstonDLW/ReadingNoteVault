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

This controller owns sequencing and authorization. `question-guide.md`
owns content choices; `note-rules.md` owns organization, writing, and review.
Keep analysis, technical bookkeeping, and successful verification internal
unless requested. Report verification failures and deviations.

## Steps

1. **Resolve and read the source scope.** Identify the exact source and
   scope. Without a supplied path or URL, look in `0-inbox/` for the
   original reading authority. Ask when the source or scope remains
   unresolved; do not substitute remembered content for inaccessible text.

2. **Analyze and discover.** Use `question-guide.md` to analyze the scope.
   Use Discovery Before Approval in `update-rules.md` to find matching
   notes, and Locations And Metadata in `note-rules.md` to resolve
   prospective paths.

3. **Ask and wait.** Present the grouped selection checkpoint from
   `question-guide.md` before proposing note organization. Unanswered choices
   block drafting and final vault writes. Stop and wait; continue only
   independent source reading or discovery. Do not
   choose a recommended option on the user's behalf or treat silence,
   a preselected option, an empty tool response, or elapsed time as an answer.

4. **Organize and authorize.** Apply Organize Before Drafting in
   `note-rules.md` internally. Show only a compact plan of the resulting
   notes and representations. If existing authorization covers these confirmed
   changes, state the plan and proceed. Complete selections accompanied by
   "go ahead" also authorize the resulting plan. Otherwise obtain approval.
   Ask again only for unresolved choices or changes outside the approved scope.
   File-edit permission does not settle content choices; delegated judgment
   settles only the named choices and does not itself authorize file edits.

5. **Draft and review.** Apply Integration After Approval in `update-rules.md`,
   the writing rules in `note-rules.md`, and `linking-rules.md`. Complete both
   Final Review passes in `note-rules.md` before writing final files or
   delivering the note. If a check cannot be completed, report the limitation and
   leave the affected artifact and dependent changes unresolved. Do not
   claim verification passed or silently substitute another representation.

6. **Write and log.** Write verified notes and assets to their vault
   locations. Apply `log-rules.md` to completed changes.
