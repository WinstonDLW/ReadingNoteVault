# Log Rules

Each source's log is `2-logs/log-<source-slug>.md`, using its source note's
slug. Decide logging from completed work.

## Logging Scope

Record newly processed scope, created or removed notes, changes to captured
knowledge or note boundaries, and meaningful source-reference changes.
Pure formatting, wording, layout, unchanged reprocessing, and rule edits
need no source-log entry.

## Entry

Create the log when qualifying work has no log; otherwise append:

```markdown
- YYYY-MM-DD | Scope
  - Source: [[source-<source-slug>|<Source Title>]]
  - Created: note list or none
  - Updated: note list or none
  - Summary: brief knowledge or scope change
```

Add `Removed: note list` when applicable. List note filenames without
extensions; exclude the log itself. Follow `linking-rules.md` for links.
