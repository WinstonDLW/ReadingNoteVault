# Agent Instructions

For any reading-note task, read the current `_rules/workflow-rules.md`
first.

Follow its rule routing. Load other rule files only when the current step
needs them. Always use the latest rule files on disk.

Use `_rules/question-guide.md` before writing notes.

Treat user file changes as intentional. If a note was deleted, do not
restore it from Git history, backups, logs, or memory unless the user
explicitly asks for restoration.

For a new source scope, use the requested source material and the current
rules as the authority. Do not use other generated notes, previous
chapter notes, or old note versions as content or style references.

Open existing notes only when the current routed step requires updating
that exact source note or exact concept note. Existing notes should not
override the current rules or the user's current instructions.
