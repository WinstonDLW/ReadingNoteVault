# Log Rules

Each source has a processing log at:

```text
2-logs/log-<source-slug>.md
```

Use the same slug as its source note.

## Logging Scope

Record:

- a newly processed source scope
- created or removed notes
- changes to captured knowledge or note boundaries
- meaningful source-reference changes

Pure formatting, wording, and layout improvements do not require a log
entry.

## Entry

Create the log when missing. Otherwise append a compact entry:

```markdown
- YYYY-MM-DD | Scope
  - Source: [[source-<source-slug>|<Source Title>]]
  - Created: note list or none
  - Updated: note list or none
  - Summary: brief change summary
```

Follow `linking-rules.md` for link treatment.
