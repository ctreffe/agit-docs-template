# AGIT Documentation Collaboration Model v0.3.0

This file defines the collaboration model for AI-assisted technical documentation projects derived from this template.

## 1. Purpose

The repository supports technical documentation work based on software engineering and scientific writing principles: explicit context, small reviewable changes, documented decisions, source discipline, quality checks, and milestone-based evolution.

The AI assistant may help with drafting, restructuring, consistency checks, link review, screenshot planning, visual QA, and repository maintenance. The maintainer remains responsible for documentation intent, technical correctness, audience fit, structure, approvals, and publication.

## 2. Repository as source of truth

The repository is the durable project memory. Important context, assumptions, rules, decisions, and changes belong in versioned files, not only in chat history.

The assistant should read the relevant repository files before making substantive changes and should update project memory when decisions or rules change.

At the start of a new context window or assistant session, use
`CONTINUATION_PROMPT.md` to reconstruct the documentation, Git and QA baseline
in a defined order before substantive drafting or revision.

## 3. Maintainer control

The maintainer owns:

- The purpose and scope of the documentation.
- The target audience and required level of detail.
- The documentation structure and navigation model.
- The technical truth and validation standard.
- The decision to publish, archive, or revise documentation.

The assistant may propose structure, identify inconsistencies, and provide feedback, but structural and content decisions remain with the maintainer.

## 4. Documentation type and audience

At initialization, the assistant must ask what type of technical documentation is being created and which documentation type profile should guide the work. Examples include user guide, admin guide, API reference, technical concept, migration guide, troubleshooting guide, operating procedure, release documentation, or a mixed documentation set.

The assistant must also ask who the documentation is for, what they already know, what they should not be expected to know, what tasks they need to complete, and what misunderstandings or operational risks the documentation must prevent. Audience decisions should shape structure, detail level, screenshots, examples, and QA.

For bilingual documentation, the assistant must ask which languages are required, whether one language is authoritative, and how parallel documents should be kept aligned. The default AGIT convention is parallel Quarto files, for example `topic.qmd` and `topic.de.qmd`.

## 5. Quarto documentation format

AGIT documentation projects use Quarto Markdown (`.qmd`) as the preferred internal documentation format unless a project-specific reason argues against it. The assistant should treat `_quarto.yml`, `docs/`, and maintained assets as part of the documentation source system.

Before milestones, the assistant should attempt Quarto rendering when the local toolchain is available and report clearly if rendering was not possible.

## 6. Sensitive information and screenshots

Technical documentation often contains screenshots, URLs, system names, logs, user data, configuration values, tickets, and internal process details. These materials must be treated as potentially sensitive until the maintainer confirms otherwise.

Before reading or incorporating raw sources, screenshots, exports, logs, or operational data, the assistant should ask whether they may contain sensitive or personal information. If needed, the assistant should request sanitized derivatives instead of raw material.

Screenshots and visual artifacts should be reviewed for sensitive information before they are committed or published.

Assistant access to a source or sanitized derivative, Git versioning and
publication or other sharing are separate maintainer decisions. Approval for
one does not imply either of the others.

Sensitive raw sources should remain outside Git by default. Before adding
screenshots, exports, tickets, logs or operational data to the working tree,
define the source inventory, versioning decision, redaction needs and relevant
`.gitignore` rules. Prefer sanitized or reviewed derivatives whenever they are
sufficient. Review new and untracked files for accidental sensitive-source
inclusion before preparing a commit.

Generated documentation can disclose sensitive information through small
tables, screenshots, URLs, labels, hover text, embedded resources, archives or
file metadata even when raw sources are absent. Review these output surfaces
before versioning or publication. Automated privacy, secret or content checks
are warning systems, not proof that an artifact is safe.

## 7. Link and source discipline

Links are part of the documentation evidence model. Internal links should support navigation and maintainability. External links should be explicit, stable where possible, and checked when documentation is prepared for a milestone.

The assistant should avoid vague link text such as "here" when a descriptive label is possible.

## 8. Visual documentation discipline

Screenshots, diagrams, and visual examples should clarify real tasks, states, decisions, or interfaces. They should not be decorative filler.

Visual artifacts should be current, readable, consistently named, and connected to the text that uses them. If a visual is generated or edited, the repository should make that status clear.

## 9. Decisions

Substantive decisions should be recorded in `decisions/` using the record type that matches the decision. A DDR is appropriate when a decision affects documentation structure, audience assumptions, terminology, screenshot policy, link model, visual standards, publication workflow, or milestone scope.

Documentation projects may also use PDRs for project scope, roadmap, collaboration, privacy or repository-structure decisions, and ADRs for Quarto structure, build pipeline, tooling, output model or automation decisions.

Decision records are not a substitute for concise documentation. They preserve why important choices were made.

## 10. Git history

The assistant may inspect git history and status to understand the project. The assistant must not create commits, rewrite history, drop stashes, reset branches, push changes or perform any other Git history action unless the maintainer instruction for that specific action contains a recognized control word.

Recognized control words are `explicit` and `explicitly` in English-language instructions, and the German word family `explizit`, including inflected forms such as `explizite`, `expliziten`, `expliziter` and `explizites`, in German-language instructions. Requests without one of these control words authorize preparation and guidance only.

Every commit recommendation should include a concise summary and a meaningful
description that matches the actual diff. Regular commits should use
Conventional Commits, for example `docs: refine screenshot guidance`.
Descriptions should explain what changed and, when useful, why or how it was
checked; they must not describe future work as completed.

Documentation milestones should progress through small regular commits for
structure, drafting, source integration, review and fixes whenever those are
meaningful separate steps. Milestone commits are the exception: they should be
descriptive, omit a Conventional Commit prefix, and include the version number,
for example `Finalize administrator guide milestone (v0.3.0)`. The milestone
commit closes and harmonizes already reviewed work; it must not be used to
bundle an entire separable documentation milestone into one oversized change.

## 11. Milestones

A milestone should close with:

- Updated version information.
- Updated changelog.
- Reviewed documentation structure.
- Link and visual QA where relevant.
- Open decisions or follow-up work documented.
- A clear maintainer-approved commit.

## 12. Numbered collaboration

When the maintainer needs to decide, review, validate or perform repository
actions, the assistant should use concise numbered lists whenever practical.
Each item should be independently answerable and should clearly distinguish a
decision, question, check, review point or Git action. This convention also
applies during structured project initialization.

At a meaningful checkpoint, the numbered handoff should identify the content
ready for review, QA performed, source or disclosure limitations, decisions
required from the maintainer, the proposed next step and, when ready, a commit
summary and description.

## 13. External feedback

Feedback from external reviewers is review input, not an automatic instruction
to change the maintained documentation. The assistant should summarize external
comments as numbered issues and wait for maintainer acceptance, rejection or
qualification before implementing them. Clear comments written by the
maintainer may be transferred directly; ambiguous or consequential comments
require clarification.
