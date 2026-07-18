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
   - Which artifacts may be published or otherwise shared.
   - Which `.gitignore` rules must exist before source files are added to the
     working tree.
   - Which automated checks may warn about disclosure risks without being
     treated as safety approval.

6. Confirm visual documentation model.
   - Screenshot policy.
   - Diagram policy.
   - Naming and storage rules.
   - Visual QA expectations.

7. Confirm link model.
   - Internal navigation.
   - External references.
   - Link checking expectations.
   - Stable source references.

8. Confirm feedback model.
   - Direct source comments, DOCX comments and Track Changes, annotated PDF or
     project-specific alternatives.
   - Explicit page, chapter, bundle or snapshot scope for generated review
     artifacts.
   - Maintainer curation of external feedback, by default with `Maintainer:`
     comments.
   - Local storage, assistant access, Git versioning and publication rules for
     review artifacts.
   - Transfer of accepted feedback back to authoritative source files.

9. Adapt template files.
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

10. Establish the initial roadmap and review rhythm.
   - Define the first meaningful documentation milestone and its validation or
     publication objective.
   - Identify the next small structure, drafting, review and QA steps.
   - Plan regular Conventional Commits below the milestone and a separate
     milestone closure commit.

11. Confirm initialization completion.
   - Verify that identity, purpose, scope, audience, roadmap, source handling,
     Quarto, feedback and publication model, QA expectations, decision-record
     needs and retained template files are documented consistently.
   - Resolve required `TBD` placeholders before substantive drafting begins.

12. Prepare initialization commit.
   - Review git status.
   - Review generated changes.
   - Normally use a regular `chore:` commit for initialization.
   - Use an unprefixed milestone commit only when initialization also completes
     a genuinely defined and reviewed versioned milestone.

After initialization, retain `CONTINUATION_PROMPT.md` and use it whenever work
continues in a new context window or assistant session.

Retain `HARMONIZATION_PROMPT.md` for maintainer-initiated source-template,
documentation, output and roadmap alignment.

Retain `RETROSPECTIVE_PROMPT.md` for maintainer-initiated, structured reviews
of Maintainer-Agent documentation collaboration.
