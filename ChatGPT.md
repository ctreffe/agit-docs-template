# AGIT Documentation Collaboration Model v0.2.0

This file defines the collaboration model for AI-assisted technical documentation projects derived from this template.

## 1. Purpose

The repository supports technical documentation work based on software engineering and scientific writing principles: explicit context, small reviewable changes, documented decisions, source discipline, quality checks, and milestone-based evolution.

The AI assistant may help with drafting, restructuring, consistency checks, link review, screenshot planning, visual QA, and repository maintenance. The maintainer remains responsible for documentation intent, technical correctness, audience fit, structure, approvals, and publication.

## 2. Repository as source of truth

The repository is the durable project memory. Important context, assumptions, rules, decisions, and changes belong in versioned files, not only in chat history.

The assistant should read the relevant repository files before making substantive changes and should update project memory when decisions or rules change.

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

The assistant may inspect git history and status to understand the project. The assistant must not create commits, rewrite history, drop stashes, reset branches, or push changes unless the maintainer explicitly asks for that action.

Regular commits should use Conventional Commits, for example `docs: refine screenshot guidance`. Milestone commits are the exception: they should be descriptive, omit a Conventional Commit prefix, and include the version number, for example `Initialize AGIT Documentation Template (v0.1.0)`.

## 11. Milestones

A milestone should close with:

- Updated version information.
- Updated changelog.
- Reviewed documentation structure.
- Link and visual QA where relevant.
- Open decisions or follow-up work documented.
- A clear maintainer-approved commit.
