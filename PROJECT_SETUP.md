# Project Setup

Use this file when creating a concrete documentation project from the template.

Keep `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` in derived projects as
documentation of the initialization method. Record completion, source-template
baseline and later harmonizations in `PROJECT_CONTEXT.md`; remove either file
only as a deliberate, documented maintainer exception.

## Initialization checklist

1. Confirm repository identity.
   - Project name.
   - Repository URL.
   - Maintainer.
   - License model.

2. Confirm documentation type.
   - User guide, admin guide, technical concept, API reference, migration guide, troubleshooting guide, release documentation, operating procedure, or mixed documentation set.

3. Confirm documentation scope.
   - What is included.
   - What is out of scope.
   - What existing material should be reused.

4. Confirm audience.
   - Primary users.
   - Technical background.
   - Tasks they need to perform.
   - Risks the documentation should prevent.

5. Confirm source and sensitivity model.
   - Raw screenshots, logs, exports, tickets, URLs, configuration files, or source documents.
   - Sensitive or personal information.
   - Sanitization or redaction requirements.
   - Which raw sources or reviewed derivatives the assistant may inspect.
   - Which reviewed derivatives and generated outputs may be versioned.
   - Which files may be published or otherwise shared.
   - Which `.gitignore` rules must exist before source files are added to the
     working tree.
   - Which automated checks may warn about disclosure risks without being
     treated as safety approval.

6. Confirm visual documentation model.
   - Screenshot policy.
   - Diagram policy.
   - Naming and storage rules.
   - Visual QA expectations.

7. Confirm the external-file and project-material model.
   - Keep external content in `input/` unchanged.
   - Catalog retained created or transformed working files in `materials/`.
   - Treat registered materials as assistant-readable and decide local,
     versioned or external storage separately from publication.
   - Preserve provenance when promoting material to `docs/` or `assets/`.
   - Use ignored `temp/` for disposable, never-versioned intermediates and
     `temp/restricted/` when assistants must not inspect them.

8. Confirm link model.
   - Internal navigation.
   - External references.
   - Link checking expectations.
   - Stable source references.

9. Confirm feedback model.
   - Direct source comments, DOCX comments and Track Changes, annotated PDF or
     project-specific alternatives.
   - Explicit page, chapter, bundle or snapshot scope for generated review
     files.
   - Maintainer curation of external feedback, by default with `Maintainer:`
     comments.
   - Local storage, assistant access, Git versioning and publication rules for
     review files.
   - Transfer of accepted feedback back to authoritative source files.

10. Adapt template files.
   - Retain and adapt `AGENTS.md` as the automatic agent entry point.
   - Preserve an AI Collaboration Note directly below the README title and badges, if badges are present.
   - Keep the note visible, factually correct for the derived project, and linked to `ChatGPT.md`.
   - Include one concrete sentence describing what the collaboration model documents for the derived documentation project, such as documentation practices, collaboration workflows, link discipline, visual QA or repository conventions.
   - Update `PROJECT_CONTEXT.md`.
   - Complete `DOCS_SETUP.md`.
   - Adapt `FEEDBACK_WORKFLOW.md`, `AUDIENCE.md`, `STYLE_GUIDE.md`,
     `SCREENSHOTS.md`, `LINKS.md`, and `VISUAL_QA.md`.
   - Keep `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` as initialization provenance.
   - Record the initial template version and commit, initialization status,
     later harmonization baseline and intentional deviations in
     `PROJECT_CONTEXT.md`.

11. Establish the initial roadmap and review rhythm.
   - Define the first meaningful documentation milestone and its validation or
     publication objective.
   - Identify the next small structure, drafting, review and QA steps.
   - Plan regular Conventional Commits below the milestone and a separate
     milestone closure commit.

12. Confirm initialization completion.
   - Verify that identity, purpose, scope, audience, roadmap, source handling,
     Quarto, feedback and publication model, QA expectations, decision-record
     needs and retained template files are documented consistently.
   - Resolve required `TBD` placeholders before substantive drafting begins.

13. Prepare initialization commit.
   - Review git status.
   - Review generated changes.
   - Normally use a regular `chore:` commit for initialization.
   - Use an unprefixed milestone commit only when initialization also completes
     a genuinely defined and reviewed versioned milestone.

## README badge policy

Place the badge block directly below the README title and before the AI
Collaboration Note. Use status, version and license in that order, followed
only by badges for real build, test or documentation automation.

Derived documentation projects must adapt the template badges to the concrete
project. Status must have a documented meaning, version must represent the
latest completed documentation state and license must match the repository.
Use release, site-build or link-check badges only when the corresponding
workflow exists. Avoid a last-commit badge because repository activity is not
documentation quality or publication readiness.

Keep English and German badge blocks identical when both READMEs are present.
Record the Documentation Template version and commit in `PROJECT_CONTEXT.md`,
not as the derived project's version badge.

After initialization, retain `CONTINUATION_PROMPT.md` and use it whenever work
continues in a new context window or assistant session.

Retain `HARMONIZATION_PROMPT.md` for maintainer-initiated source-template,
documentation, output and roadmap alignment.

Retain `RETROSPECTIVE_PROMPT.md` for maintainer-initiated, structured reviews
of Maintainer-Agent documentation collaboration.
