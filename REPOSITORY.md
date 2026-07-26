# Repository Model

This repository follows a repository-first documentation workflow. Durable context, decisions, and documentation files should be versioned whenever they are part of the project record.

Use `CONTINUATION_PROMPT.md` at the start of a new context window or assistant
session to reconcile `PROJECT_CONTEXT.md`, maintained documentation and current
read-only Git evidence.

## Expected structure

- `README.md`: Repository overview.
- `README.de.md`: German overview.
- `AGENTS.md`: Automatic AI-agent entry point.
- `ChatGPT.md`: AI collaboration model.
- `CODEX.md`: Assistant rules.
- `PROJECT_SETUP.md`: Initialization workflow.
- `DOCS_SETUP.md`: Documentation setup checklist.
- `PROJECT_CONTEXT.md`: Project-specific context template.
- `DOCUMENTATION_PROCESS.md`: Ongoing process.
- `AUDIENCE.md`: Audience model.
- `STYLE_GUIDE.md`: Documentation style guide.
- `SCREENSHOTS.md`: Screenshot policy.
- `LINKS.md`: Link and reference rules.
- `VISUAL_QA.md`: Visual QA checklist.
- `decisions/`: Decision Records, including DDRs, PDRs and ADRs.
- `CHANGELOG.md`: Version history.
- `VERSION`: Current template or project version.
- `_quarto.yml`: Quarto project configuration.
- `input/`: Intake and catalog for unchanged external files and sources.
- `docs/`: Maintained Quarto source files.
- `assets/`: Maintained screenshots, figures, and diagrams.

## README badge policy

Use a compact badge block directly below the README title and before the AI
Collaboration Note. The standard order is status, version and license, followed
only by badges for real documentation automation such as a site build or link
check.

Status links to `VERSION`, version links to `CHANGELOG.md` and license links to
`LICENSE`. Public templates may use dynamic GitHub metadata. Avoid a
last-commit badge because activity does not establish documentation quality or
publication readiness.

Derived documentation projects adapt the badges to their own documented
status, completed version, actual license and available workflows. They must
not retain the Documentation Template version as their project version or show
automation that does not exist. English and German badge blocks remain
identical when both READMEs are maintained.

## External files, maintained documentation and outputs

Use `input/intake/`, `input/restricted/`, `input/local/` and
`input/versioned/` to classify external screenshots, logs, exports, tickets,
source documents and operational data. Record safe provenance and handling
status in `input/CATALOG.md`; use the ignored `input/CATALOG.local.md` for
sensitive names, paths or details.

Maintained Quarto and Markdown sources belong in `docs/`, publication images
and diagrams in `assets/`, and local review files in `review/`. Generated HTML,
PDFs and previews remain outputs. Moving an approved file into one of these
locations communicates its durable role but does not grant publication rights.

Assistant access, Git versioning and publication or other sharing are separate
decisions. Before preparing a commit, review new and untracked files for
personal data, internal system details, secrets, confidential information,
licensing restrictions and unredacted visuals.

Rendered pages, screenshots, tables, interactive elements, embedded resources,
archives and file metadata may disclose sensitive information even when raw
sources are absent. Review them before versioning or publication. Automated
checks may identify risks, but a clean result does not authorize access,
versioning or publication.

## Temporary working files

`temp/` is fully ignored and never versioned. All contents outside
`temp/restricted/` are assistant-readable disposable documentation intermediates; assistants must not
enumerate or read `temp/restricted/`. Promote retained files to `materials/`.

## Project materials

Keep `input/` content unchanged. Store retained OCR text, transformed
screenshots, converted references and other working foundations in
`materials/`, with provenance and `local`, `versioned` or `external` storage
recorded in `materials/CATALOG.md`. Every registered material is
assistant-readable, but versioning and publication remain separate decisions.
Promote it to `docs/` or `assets/` only when it becomes maintained content.

## Git workflow

Use small, reviewable changes. Keep unrelated work out of the same commit.

Every commit should include a concise summary and a meaningful description that
matches the actual diff. Regular commits should use Conventional Commits and
represent one logical documentation step.

A milestone should normally be built through multiple regular commits when
structure, drafting, review and correction can be separated meaningfully.
Milestone commits should omit the prefix, be descriptive, include the completed
version number and primarily close already reviewed work. They must not hide
unreviewed content or bundle a whole separable milestone into one change.

Staging and unstaging are index operations and do not require a control word.
They require a specific maintainer request or authorization of the corresponding
commit, and existing staged selections and unrelated changes must be preserved.

The assistant must not commit, amend, tag, push, pull, merge, rebase, reset,
switch branches, manipulate stashes, rewrite history or perform another
protected Git action unless the maintainer instruction for that specific action
contains a recognized control word: `explicit` or `explicitly` in English, or
the German word family `explizit`, including `explizite`, `expliziten`,
`expliziter` and `explizites`.
