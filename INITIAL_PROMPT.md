# Initial Prompt

Use this as the first prompt after creating a concrete documentation project from this template.

```text
We are initializing a new technical documentation project from the AGIT Documentation Template.

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
- Screenshot, diagram, visual QA, and link expectations.
- Expected feedback channels, the explicit scope of DOCX or PDF review
  artifacts, external-feedback curation, and separate assistant-access, Git
  versioning and publication rules for those artifacts.
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

Do not stage, commit, tag, push, pull, merge, reset, rebase, switch branches or
otherwise modify Git history unless I instruct you to perform that specific Git
action and use a recognized control word: `explicit` or `explicitly` in
English, or the German word family `explizit`.

When the setup state is ready, provide a change summary, checks, limitations, a
suggested commit summary and description, and a concise numbered list of
remaining maintainer decisions or GitHub Desktop steps.
```
