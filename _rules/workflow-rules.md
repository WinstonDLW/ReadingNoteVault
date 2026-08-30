# Workflow Rules

Use this controller for requests to generate notes from a book, chapter,
article, section, page range, or similar source scope. The user reads
first. The assistant reads the same scope, negotiates the note treatment,
obtains edit approval, verifies the draft, and then writes the notes.

Read this file first. Load the other rule files only when their step
needs them.

## Steps

1. Resolve source and scope.

   Identify the exact source and requested scope. When the user names a
   source without a path or URL, look for the original resource in
   `0-inbox/` and use it as the reading authority. Ask for clarification
   when the source or scope remains unresolved.

2. Analyze the scope and discover affected notes.

   Use `question-guide.md` to identify the knowledge contribution,
   reasoning, meaningful content, possible note boundaries, and
   treatments that need user preference. Use only the Discovery Before
   Approval section of `update-rules.md` to find the matching source note
   and concept notes with the same or closely related meanings. Use the
   Locations And Metadata section of `note-rules.md`, plus the log path
   and Logging Scope in `log-rules.md`, to determine the prospective file
   changes. Keep source-role classification, treatment bookkeeping, file
   changes, and logging decisions internal unless the user asks for them.

3. Present the question checkpoint.

   Follow `question-guide.md`. Show the source's general contribution, an
   ordered general note plan, and numbered preference questions. The plan
   should explain what the note will introduce and how definitions,
   mechanisms, examples, consequences, qualifications, and representations
   will build on one another. Ask separately about every optional example,
   qualification, supporting topic, or representation that could be
   included, compressed, or omitted without losing the central knowledge.
   Do not show an inventory table, decision statuses, prospective file
   changes, or logging details unless requested.

4. Finalize and authorize the changes.

   After receiving the user's preferences or applying requested best
   judgment, show the final general note plan and content decisions. For
   each retained or replacement artifact, state the knowledge it will
   teach and any simplification that affects that knowledge. Keep the
   detailed semantic contract and implementation change set internal. The
   approved note plan forms the content boundary for drafting. Wait for
   explicit edit approval unless the user has already approved that final
   note plan.

5. Draft and verify the notes.

   After approval, use the integration rules in `update-rules.md`, the
   writing rules in `note-rules.md`, and `linking-rules.md` for Obsidian
   links. Draft from the approved content decisions and final note plan.
   Apply the Final Knowledge Check in `note-rules.md`. Render generated
   visuals and compare them with their semantic contracts. Return to the
   checkpoint before adding meaningful knowledge outside the approved
   content boundary. Keep successful verification internal; report
   failures or deviations.

6. Write the verified result.

   After verification passes, write the final notes and assets to their
   vault locations.

7. Record qualifying work.

   Use `log-rules.md` when the completed work meets its logging scope.
