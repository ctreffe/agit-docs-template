# Project Setup

Use this file when creating a concrete documentation project from the template.

Keep `PROJECT_SETUP.md` in derived projects as documentation of the
initialization method. Record completion, source-template baseline and later
harmonizations in `PROJECT_CONTEXT.md`; remove it
only as a deliberate, documented maintainer exception.

## Lean initialization contract

Before the normal questionnaire, `$start-project` asks one concise,
unnumbered routing choice: use the normal lean path or explicitly select
`$grill-me` for detailed initialization and planning. The routing choice is
not one of the six project questions. The skill is never invoked from a
suggestion; a suggestion is not consent. The maintainer may decline or stop
grilling and return to the lean path, and neither path changes any access,
versioning, transmission, publication or protected-action authority.

`$start-project` begins with no more than six fundamental maintainer
questions. Each numbered item is one coherent decision, not a container for a
hidden questionnaire:

1. What is the documentation project's identity and purpose?
2. Who is the primary audience, and what should it be able to do?
3. What is the first useful document outcome, and what minimum evidence will
   show that it serves the audience?
4. What is currently in scope, and what are the explicit non-goals?
5. Which sources or materials may the assistant access now, and which
   sensitivity boundary applies?
6. Which delivery or operating constraint must be fixed before authoring
   begins?

Use repository evidence for answers already established. The last question
includes only a constraint that is consequential now; do not bundle structure,
screenshots, links, feedback, formats, rendering, storage and publication into
one survey. Keep safe template defaults for nonessential choices or mark them
explicitly undecided. Create only the initial document contract needed for the
first outcome; clarify later documents and detailed production choices through
their concrete workflows. Source access, transmission, publication and visual
approval remain separate gates when triggered.

## Initialization checklist

The checklist below guides implementation after the lean questionnaire. It is
not an instruction to ask every item during the initial maintainer turn.

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
   - Visual-inspection expectations. Routine renders receive technical output
     validation without the Browser skill. Agent inspection occurs only
     through an explicitly invoked `$visual-inspection` for named current
     renders and maintainer-selected formats.

7. Confirm the external-file and project-material model.
   - Keep external content in `input/` unchanged.
   - Catalog retained created or transformed working files in `materials/`.
   - Treat registered materials as assistant-readable and decide local,
     versioned or external storage separately from publication.
   - Preserve provenance when moving accepted text to `docs/` or approving
     maintained binary documentation material for `materials/versioned/`.
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
   - Generated review outputs below `output/<format>/` and returned annotated
     files directly below ignored `review/`.
   - Transfer of accepted feedback back to authoritative source files.

10. Adapt template files.
   - Retain and adapt `AGENTS.md` as the automatic agent entry point.
   - Preserve an AI Collaboration Note directly below the README title and badges, if badges are present.
   - Keep the note visible, factually correct for the derived project, and linked to `COLLABORATION.md`.
   - Include one concrete sentence describing what the collaboration model documents for the derived documentation project, such as documentation practices, collaboration workflows, link discipline, visual inspection or repository conventions.
   - Update `PROJECT_CONTEXT.md`.
   - Complete `DOCS_SETUP.md`.
   - Complete the initial document contract in `DOCUMENTS.md`.
   - Adapt `FEEDBACK_WORKFLOW.md`, `AUDIENCE.md`, `STYLE_GUIDE.md`,
     `SCREENSHOTS.md` and `LINKS.md`.
   - Keep `PROJECT_SETUP.md` as initialization provenance.
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
   - Verify that the six fundamentals, first useful document contract, current
     source boundary, safe defaults and retained template state are documented
     consistently.
   - Nonessential roadmap, Quarto, feedback, publication, QA and later-document
     fields may remain explicitly undecided. Resolve a `TBD` only before the
     concrete drafting, source, render or publication work it governs.

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

After successful initialization, replace the inherited source-template
maintenance history in `CHANGELOG.md` with a project-owned changelog beginning
at `Unreleased`. Replace `TASK_HANDOFF.md` with a project-owned initialization
handoff containing only current documentation-project state, decisions, checks
and the next step. Preserve template lineage in `PROJECT_CONTEXT.md`, not in
either active project-history file. If initialization is incomplete, leave
both resets pending and identify the inherited content as non-authoritative.

After initialization, retain the repository skills and `TASK_HANDOFF.md`.
Routine tasks use `start-task`; invoke `$review-project`, `$sync-template`,
`$check-consistency`, `$add-document`, `$revise-document` and
`$perform-retrospective` explicitly only when their specialized outcome is
needed. Remove the project copy of `$create-local-project` after successful
initialization.

## Synchronized external storage

If large screenshots, recordings, video, audio, exports or reference files must
be available on several devices without entering Git, apply
`SYNCHRONIZED_STORAGE.md`. Decide provider transmission, stable project ID,
input and material scope, optional external outputs, availability checks,
conflict handling and backup. Create ignored `sync:` mappings on every device,
keep maintained `docs/`, approved `materials/versioned/` files and presentation
source in `styles/` authoritative, and do not synchronize `temp/`.

## Required local runtime setup

During initialization, check only what the first concrete outcome needs.
Reuse established answers; defer later tooling and do not add a mandatory
questionnaire. General optimization has no dedicated skill; concrete recurring
environment problems route through `troubleshoot-environment`.

Check the runtime needed for the selected outcome and the actual interpreter
used by its commands. A new clone/device does not inherit ignored environments;
missing local setup is not evidence of damage. Reuse the project's established
manager and isolation model. When Python is required and no suitable managed
environment exists, prepare a clone-local ignored .venv; do not create one for
a project without Python needs or copy one from another clone.

Track dependencies and lockfiles using existing project conventions (for
example requirements-tools.txt for Python helpers). Document reproducible setup
and explicit interpreter or manager commands. Prepare only needed local setup,
reuse existing approval and obtain any missing installation/download authority
before applying it. Verify the interpreter and a minimal relevant import or
original command; defer optional tools without blocking unrelated work.

Check Python only for required documentation helpers; Quarto use alone does not
require a new Python environment. Use non-sensitive synthetic verification.
