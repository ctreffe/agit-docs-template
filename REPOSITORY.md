# Repository Model

This repository follows a repository-first documentation workflow. Durable context, decisions, and documentation artifacts should be versioned whenever they are part of the project record.

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

Raw inputs and generated outputs should not be committed by default unless the project explicitly needs them and they have been reviewed.

## Git workflow

Use small, reviewable changes. Keep unrelated work out of the same commit.

Regular commits should use Conventional Commits. Milestone commits should omit the prefix, be descriptive, and include the version number.

The assistant must not commit, push, reset, drop stashes, or rewrite history without explicit maintainer instruction.
