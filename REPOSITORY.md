# Repository Model

This repository follows a repository-first documentation workflow. Durable context, decisions, and documentation artifacts should be versioned whenever they are part of the project record.

Use `CONTINUATION_PROMPT.md` at the start of a new context window or assistant
session to reconcile `PROJECT_CONTEXT.md`, maintained documentation and current
read-only Git evidence.

## Expected structure

- `README.md`: Repository overview.
- `README.de.md`: German overview.
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
- `docs/`: Maintained Quarto source files.
- `assets/`: Maintained screenshots, figures, and diagrams.

## Inputs, maintained files, and outputs

Separate these categories clearly:

- Raw inputs: screenshots, logs, exports, tickets, notes, source documents, and operational data.
- Sanitized inputs: redacted or transformed versions that may be used safely.
- Maintained documentation: Quarto source files and supporting Markdown that represent the project documentation.
- Generated outputs: rendered HTML, PDFs, screenshots, previews, or release artifacts.

Raw inputs and generated outputs should not be committed by default unless the project explicitly needs them and they have been reviewed. Assistant access, Git versioning and publication or other sharing are separate approval decisions; none implies another.

Establish `.gitignore` rules and a source inventory before placing sensitive
raw inputs in the repository working tree. Before preparing a commit, review
new and untracked files for personal data, internal system details, secrets,
confidential information, licensing restrictions and unredacted visuals.

Rendered pages, screenshots, tables, interactive elements, embedded resources,
archives and file metadata may disclose sensitive information even when raw
sources are absent. Review them before versioning or publication. Automated
checks may identify risks, but a clean result does not authorize access,
versioning or publication.

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

The assistant must not commit, push, reset, drop stashes, rewrite history or perform other Git history actions unless the maintainer instruction for that specific action contains a recognized control word: `explicit` or `explicitly` in English, or the German word family `explizit`, including `explizite`, `expliziten`, `expliziter` and `explizites`.
