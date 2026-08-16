# ReadingNoteVault

Personal vault for AI-assisted book reading notes.

## Structure

- `0-inbox/` - raw source files and temporary inputs; ignored by git
- `1-notes/` - generated and refined markdown notes
  - `concepts/` - focused concept notes
  - `sources/` - source-level notes for books and references
- `2-logs/` - processing logs and reading workflow records
- `3-resource/` - extracted images, figures, and supporting resources
- `_rules/` - workflow, note, linking, logging, update, and question rules
- `notes/` - legacy starter folder; prefer `1-notes/` for active notes

## Git Ignore

The vault ignores local-only content in `0-inbox/` and Obsidian app state in `.obsidian/`.
