# Initial Prompt

Use this as the first prompt after creating a concrete documentation project from this template.

For normal initialization, the maintainer only needs to give the prompt below to the assistant. The assistant applies `AGENTS.md`—automatically loaded where supported—reads and applies `PROJECT_SETUP.md`, `DOCS_SETUP.md` and the other setup files, presents every required maintainer decision and performs the repository updates; the maintainer does not execute those files separately.

```text
We are initializing a new technical documentation project from the AGIT Documentation Template.

Apply AGENTS.md as the durable repository operating baseline. If it was not
loaded automatically, read it first. This prompt defines the one-time
initialization workflow; do not treat AGENTS.md alone as an instruction to
initialize or modify the template.

Please first read the complete repository and all relevant project rules, especially README.md, ChatGPT.md, CODEX.md, DOCUMENTATION.md, REPOSITORY.md, PROJECT_SETUP.md, DOCS_SETUP.md, PROJECT_CONTEXT.md, DOCUMENTATION_TYPE_PROFILES.md, QUARTO.md, FEEDBACK_WORKFLOW.md, AUDIENCE.md, STYLE_GUIDE.md, SCREENSHOTS.md, LINKS.md, VISUAL_QA.md, and the DDR guidance.

Then perform a structured initialization following PROJECT_SETUP.md and DOCS_SETUP.md.

Before reading or incorporating any raw screenshots, logs, exports, tickets, source documents, internal URLs, configuration values, or operational data, ask whether they may contain sensitive or personal information. If needed, request sanitized derivatives instead of raw material.

Ask me for all missing maintainer decisions, including:

- Documentation type and documentation type profile.
- Whether the project is bilingual, and if so, which language is authoritative.
- Documentation purpose and scope.
- For tutorials or instructions: the concrete starting point and goal.
- Target audience and expected prior knowledge.
- Required outputs and publication context.
- Quarto project type, output formats, CLI availability, PATH status, and render expectations.
- Existing source material and sensitivity constraints.
- Which raw sources, reviewed derivatives and generated outputs may be tracked
  in Git, and which ignore rules must exist first.
- Screenshot, diagram, link and output-validation expectations, including any
  deliberate deviation from the default that Browser- or page-image-based
  visual QA occurs only before milestone closure or when I explicitly request it.
- Expected feedback channels, the explicit scope of DOCX or PDF review
  files, external-feedback curation, and separate assistant-access, Git
  versioning and publication rules for those files.
- The first roadmap milestone, its validation objective and the first small
  reviewable steps below it.
- Initialization provenance: keep PROJECT_SETUP.md and INITIAL_PROMPT.md under
  their original names, and record initialization status and date, the source
  template version and commit, the latest template harmonization baseline and
  intentional deviations in PROJECT_CONTEXT.md. Remove an initialization file
  only if I make a deliberate exception and the reason is documented.
- Ongoing project rules and domain files that should be adapted and maintained.

After collecting the required information, update the repository files to
reflect the concrete project, including `_quarto.yml` and the files in `docs/`
when Quarto is used. Confirm that the structured initialization is complete and
that required placeholders have been resolved before large-scale drafting.

Adapt AGENTS.md only where the concrete project's commands, directory layout or
validation procedures differ from the template. Preserve its role as a concise
router to authoritative guidance, including its safety and documentation
boundaries.

Establish the external-file workflow during initialization. Place unclassified
arrivals in `input/intake/`, classify them into `input/restricted/`,
`input/local/` or `input/versioned/`, and maintain safe metadata in
`input/CATALOG.md`. Treat assistant access, Git versioning and publication as
separate decisions. Move accepted textual content to `docs/`, reviewed binary
documentation material approved for Git to `materials/versioned/`, and
returned annotated review files to `review/` only when their durable role is
clear. Keep generated outputs below `output/` in format-specific directories.

Keep `input/` content unchanged. Establish `materials/` and its catalog for
retained created or transformed documentation working files. Registered
materials are assistant-readable; decide local, versioned or external storage
separately and preserve provenance when accepted text moves to `docs/` or
reviewed binary material is approved for `materials/versioned/`.

Establish ignored `temp/` for disposable documentation intermediates. All
contents outside `temp/restricted/` are assistant-readable and never
versionable; that directory is unavailable to assistants.

When large non-Git files must be available on several devices, apply
`SYNCHRONIZED_STORAGE.md`. Decide provider transmission separately, establish
the stable project ID and provider-neutral `sync:` roots, create only ignored
per-device mappings, verify local availability and keep `temp/` device-local.
Do not create or populate synchronized storage without the maintainer's
project-specific approval.

Staging and unstaging do not require a control word, but perform them only when
I specifically request the index action or authorize the corresponding commit.
Preserve existing staged selections and unrelated changes.

Only after initialization has completed successfully, remove
`CREATE_LOCAL_PROJECT_PROMPT.md` from this project and remove its template-only
references from `AGENTS.md`, `README.md` and `README.de.md` where those files
exist. This creation helper belongs to the source template and is not retained
project provenance. Keep `INITIAL_PROMPT.md`, `PROJECT_SETUP.md` and the other
initialization files. If initialization stops or remains incomplete, leave the
creation prompt and its references in place and report the cleanup as pending.
Validate local Markdown references after the cleanup.

Do not commit, amend, tag, push, pull, merge, reset, rebase, switch branches,
manipulate stashes or perform another protected Git action unless I instruct
you to perform that specific Git
action and use a recognized control word: `explicit` or `explicitly` in
English, or the German word family `explizit`.

When the setup state is ready, provide a change summary, checks, limitations, a
suggested commit summary and description, and a concise numbered list of
remaining maintainer decisions or GitHub Desktop steps.
```
