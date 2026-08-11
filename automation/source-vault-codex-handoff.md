# Codex Handoff — Private Scripture Source Vault

Work in the primary repository:

`/mnt/f/__ai-projects/scripture-discovery-journey`

Private source folder:

`/mnt/f/-- claude/ministry/bible-study-source-materials`

## Goal

Inventory, verify, classify, and register the private source collection without uploading copyrighted or unapproved originals. Keep source maintenance separate from the active HTML benchmark.

## Required operating rules

1. Read `AGENTS.md`, the master Scripture Journey skill, `sources/README.md`, `sources/registry.yaml`, and `sources/schema/source-record.schema.yaml` before changing files.
2. Preserve the authority order: Scripture compared with Scripture; original-language work; named Reformers; named Adventist pioneers; approved trusted sources; other contemporary material only for a defined supporting purpose.
3. A trusted source is a research starting point, not blanket approval of every claim. Cite the exact work, episode, page, or timestamp.
4. Never infer rights or approval. Unknown rights means link-only or local-only until verified.
5. Never commit source-folder credentials, absolute private paths, executables, duplicate binaries, or unapproved copyrighted originals.
6. Do not modify the master skill during this intake task. Propose any skill change separately.

## Phase 1 — Cheap deterministic inventory

1. Confirm the repository checkout is understood and inspect `git status -sb`. Preserve unrelated work.
2. Update safely from `origin/main` only when the current checkout permits a fast-forward.
3. Run:

   ```bash
   python3 scripts/source_vault_inventory.py \
     --source-root '/mnt/f/-- claude/ministry/bible-study-source-materials' \
     --repo-root '/mnt/f/__ai-projects/scripture-discovery-journey' \
     --write
   ```

4. Review `sources/intake/source-vault-inventory.md` and the complete JSON manifest.
5. Stop and report any unreadable file, executable, unexpected symlink, empty file, or suspicious archive before processing content.

## Phase 2 — Selective review

1. Group exact duplicates by SHA-256. Do not delete anything from the private source folder.
2. Create candidate source records only for files that can be identified accurately.
3. Verify title, author, edition, date, publisher, source URL, provenance, rights, and attribution. Leave unknown fields unknown.
4. Keep candidate records in `sources/intake/`. Only approved records with applicable scope may enter `sources/library/` and `sources/registry.yaml`.
5. Review only files needed for the current task. Do not load the whole vault into model context.

## Stephen Bohr transcript quarantine

The physical transcripts for these series require correction before any repository publication:

- *Prophecy's Repeating Sequence*
- *The Great Prophecies of Daniel and Revelation*

For each transcript:

1. Identify the exact series, episode, speaker, and corresponding official video.
2. Work on one transcript at a time in a private local correction area.
3. Compare the transcript with the recording in manageable sections. Preserve the speaker's meaning; correct transcription errors, punctuation, paragraphing, Bible references, and obvious names only.
4. Mark uncertain words and timestamps. Never guess.
5. Produce a correction log and a review copy for the project owner.
6. Keep status `under-review` until the project owner approves that transcript.
7. Perform a separate rights review. Approval of accuracy does not grant redistribution rights.
8. Commit a full corrected transcript only when redistribution is explicitly permitted. Otherwise commit metadata, notes, citations, and an authorized locator only.

## Seed sources to verify and register

### Approved trusted research starting points

- https://www.youtube.com/@mopt_ministry
- https://www.youtube.com/playlist?list=PLIWJyuxBfZ7h-pKZHMGAkVvQd6UXEGg8p
- https://www.youtube.com/playlist?list=PLIWJyuxBfZ7godSkJ-s20X5ifkfk8lBaZ
- https://www.youtube.com/@heritageandhope — give routing priority to the Sunday Law Updates, while still verifying each dated claim.

### Research tools and collections to verify

- https://www.openbible.info/labs/cross-references/
- https://www.openbible.info/topics/
- https://www.ellenwhite.info/bookswritten.htm
- https://www.ellenwhite.info/books/books-by-egw-others.htm
- https://text.egwwritings.org/allCollection/en
- https://whiteestate.org/
- https://www.amazingfacts.org/study/bible-study-guides/

Treat project PDFs and attached links as intake until individually identified and approved.

## Authority labels supplied by the project owner

Primary subject-matter sources:

1. Scripture
2. Ellen G. White
3. James White

Secondary historical witnesses:

- J. N. Loughborough
- A. T. Jones
- E. J. Waggoner
- Stephen N. Haskell
- E. A. Sutherland
- M. L. Andreasen
- F. C. Gilbert
- Taylor G. Bunch
- William Miller, including his work after the 1844 disappointment

These labels control research routing; they do not make any human source equal to Scripture.

The supplied list ends with `modern trusted sources are` but contains no names after it. Do not guess the missing sources. Report that list as incomplete.

## Study-file review rule

When a study is explicitly selected for rewriting, keep it brief and use plain, everyday language for a reader new to the Bible. Avoid unexplained terms and abbreviations: write `verses 8–11`, not `vv. 8–11`. Explain necessary terms simply. Preserve study-specific required structures, such as local situation, historical era, and promise for each named church, only when the source study actually contains that structure.

Do not rewrite every study during inventory. Review and rewrite only the files the project owner selects.

## Publication gate

Before publishing repository changes:

1. Validate every `record.yaml` against `sources/schema/source-record.schema.yaml`.
2. Confirm `sources/registry.yaml` routes only approved records.
3. Confirm no Stephen Bohr transcript is approved or stored without both accuracy approval and redistribution permission.
4. Inspect the exact Git diff and preserve unrelated work.
5. Commit only the inventory and approved source records. Push a dedicated branch and open a draft pull request unless the project owner has explicitly authorized that exact change set for direct `main` publication.
6. Report `PASS`, `FAIL`, or `BLOCKED` with concise evidence and a list of remaining owner decisions.
