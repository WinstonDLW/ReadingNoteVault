# Log Rules

Use these rules when recording completed note-generation work.

Each source has its own processing log.

## Location And Name

Store logs in:

```text
2-logs/log-<source-slug>.md
```

Use the same source slug as:

```text
1-notes/sources/source-<source-slug>.md
```

## Entry

Create the log if it is missing. Append a new entry when it exists.

Record:

- date
- processed scope
- created notes
- updated notes
- brief change summary
- link to the matching source note

Use this shape:

```markdown
- YYYY-MM-DD | Scope
  - Source: [[source-<source-slug>|<Source Title>]]
  - Created: note list or none
  - Updated: note list or none
  - Summary: brief change summary
```

Keep logs short and traceable.

Reserve Obsidian links for the matching source note.

Write created and updated concept notes as plain text filenames or names,
with Obsidian links reserved for the matching source note.
