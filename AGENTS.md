# AGENTS.md

This file is the automatically loaded entry point for AI agents working in an
AGIT Documentation Template repository. Keep it concise: it routes agents to
the repository's authoritative guidance and does not replace that guidance.

## Before Substantive Work

1. Read `CODEX.md` in full before using tools or changing files. It defines the
   local operating policy, sensitive-source boundaries and protected Git actions.
2. Read `ChatGPT.md` for the documentation collaboration model.
3. Read `README.md`, `PROJECT_CONTEXT.md`, `REPOSITORY.md`, `DOCUMENTATION.md`,
   `PROJECT_SETUP.md` and `DOCS_SETUP.md` as relevant to the task.
4. Read the affected domain guidance, including `DOCUMENTATION_PROCESS.md`,
   `DOCUMENTATION_TYPE_PROFILES.md`, `FEEDBACK_WORKFLOW.md`, `QUARTO.md`,
   `AUDIENCE.md`, `STYLE_GUIDE.md`, `SCREENSHOTS.md`, `LINKS.md` and
   `VISUAL_QA.md` where applicable.
5. For initialization, continuation, harmonization or retrospective work,
   follow the corresponding prompt file instead of reconstructing its workflow.
6. To create a locally versioned project without a remote, use
   `CREATE_LOCAL_PROJECT_PROMPT.md` from this checked-out template.

If repository guidance appears inconsistent, report the conflict and ask for a
maintainer decision when it could materially affect the result.

## Working Agreement

- Confirm the active repository and inspect its current Git state before edits.
- Preserve existing staged selections, working-tree changes and unrelated work.
- Treat documentation intent, information architecture, technical truth and
  publication decisions as maintainer-owned.
- Treat maintained repository sources as authoritative over rendered or
  annotated DOCX, PDF and website review files.
- Do not inspect potentially sensitive screenshots, logs, exports, tickets or
  operational material without maintainer approval.
- Classify new external files through `input/`; presence in `input/intake/`
  never authorizes assistant access.
- Keep audience, navigation, links, visuals, feedback handling and maintained
  source synchronized across affected documentation.
- Follow the authorization rules in `CODEX.md`; an edit request does not by
  itself authorize protected Git actions or publication.

## Validation and Handoff

Run checks proportionate to the affected formats: local-link validation, Quarto
rendering, technical review, visual QA and disclosure review where applicable.
At minimum, review the diff and run `git diff --check`. Compare English and
German structure when bilingual documentation is affected.

Report the outcome, changed files, checks performed, limitations or skipped
checks and suitable commit metadata. A successful render alone does not prove
technical correctness, audience fitness or publication readiness.
