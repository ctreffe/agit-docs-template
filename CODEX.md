# CODEX.md

This file defines local operating rules for Codex or another AI coding assistant working in this repository.

## Repository role

This repository is a reusable template for AI-assisted technical documentation projects. Keep changes generic unless the maintainer explicitly asks to specialize a derived project.

## Operating rules

- Read repository guidance before substantive edits: `README.md`, `ChatGPT.md`, `DOCUMENTATION.md`, `PROJECT_SETUP.md`, and `DOCS_SETUP.md`.
- Preserve maintainer control over documentation intent, structure, technical correctness, and publication decisions.
- Do not inspect or ingest raw screenshots, logs, exports, configuration files, tickets, or operational data when they may contain sensitive information unless the maintainer confirms that this is appropriate.
- Prefer sanitized derivatives when raw material is not needed.
- Treat assistant access, Git versioning and publication as separate maintainer
  decisions; approval for one does not authorize another.
- Treat automated privacy, secret or content checks as warnings rather than
  proof that an artifact is safe.
- Keep technical documentation task-oriented, precise, and reviewable.
- Treat links, screenshots, diagrams, and generated outputs as documentation artifacts that need provenance and QA.
- Treat maintained Quarto or other repository sources as authoritative over
  rendered or annotated DOCX and PDF review artifacts.
- Inspect supplied annotated DOCX or PDF files only after assistant access has
  been approved. Transfer clear maintainer comments and Track Changes to the
  maintained source; present unresolved external or ambiguous feedback as
  concise numbered issues according to `FEEDBACK_WORKFLOW.md`.
- Review rendered content, interactive elements, embedded resources and file
  metadata for disclosure risks before versioning or publication.
- Record substantial documentation decisions as DDRs.
- Do not create commits, rewrite history, drop stashes, reset branches, push or perform other Git history actions unless the maintainer instruction for that specific action contains a recognized control word: `explicit` or `explicitly` in English, or the German word family `explizit`, including `explizite`, `expliziten`, `expliziter` and `explizites`.

## Commit policy

Every recommendation should contain both a concise commit summary and a
meaningful description. Regular commits should use Conventional Commits and
represent one logical reviewed step. Milestone commits should omit the prefix,
be descriptive, include the completed version number and close work already
recorded in regular commits.

Use concise numbered lists for maintainer decisions, clarification questions,
validation actions, review points and GitHub Desktop steps whenever practical.
