# AGIT Documentation Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/agit-docs-template?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/agit-docs-template)](LICENSE)

> [!NOTE]
> **AI Collaboration**
>
> This repository maintains the AGIT Documentation Template.
>
> The AGIT Documentation Template is the documentation-oriented specialization of the AGIT template family.
>
> The collaboration model documents documentation practices, AI-assisted documentation workflows, link and visual QA discipline and repository conventions for documentation projects.
>
> Its collaboration model is maintained in [ChatGPT.md](ChatGPT.md).

[Deutsche Dokumentation](README.de.md) · The English README is authoritative; the German README is maintained as a close translation.

## Contents

- [Overview](#overview)
- [Core Principle](#core-principle)
- [AGIT Templateverse](#agit-templateverse)
- [When to Use This Template](#when-to-use-this-template)
- [Project Initialization](#project-initialization)
- [Recommended Workflows](#recommended-workflows)
- [Git Index and Protected Git Actions](#git-index-and-protected-git-actions)
- [Decision Records](#decision-records)
- [Repository Structure](#repository-structure)
- [Template and Derived Project Files](#template-and-derived-project-files)
- [How to Use This Template](#how-to-use-this-template)
- [Maintainer Tool Setup](#maintainer-tool-setup)
- [Continuous Improvement](#continuous-improvement)
- [License](#license)

## Overview

The AGIT Documentation Template is a starting point for technical documentation projects that require explicit context, clear ownership, reproducible collaboration, documented decisions and reviewable publication milestones. It supports user guides, administrator guides, tutorials, operating procedures, migration and troubleshooting guides, technical concepts, architecture documentation and mixed documentation sites.

Quarto Markdown is the preferred maintained source format. The baseline renders a bilingual HTML website and can be adapted for DOCX or PDF review outputs when a project needs them. Links, screenshots, diagrams and generated outputs are treated as documentation artifacts with provenance, sensitivity review and quality assurance.

## Core Principle

The maintainer owns documentation purpose, scope, structure, technical correctness, audience fit and publication decisions. The assistant may help draft, restructure, check consistency, plan visuals and review outputs, but it does not replace maintainer judgment or make publication decisions.

Maintained repository sources are authoritative. Rendered websites, DOCX files, PDFs and annotated returns are outputs or review artifacts until accepted feedback has been transferred back to the source and validated there.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

## When to Use This Template

Use this template when audience, structure, task guidance, links, screenshots, visual QA and publication format are central from the beginning. It is particularly useful when documentation must remain reviewable across languages, output formats or feedback cycles.

Use the generic Project Template when documentation is one part of a broader project. Use the Dev Template when implementation lifecycle is primary and documentation mainly accompanies software behavior.

## Project Initialization

Initialization establishes the documentation system before large-scale drafting begins.

1. Create a repository from this template and establish the authoritative local baseline.
2. Start with [INITIAL_PROMPT.md](INITIAL_PROMPT.md) and follow [PROJECT_SETUP.md](PROJECT_SETUP.md).
3. Complete [DOCS_SETUP.md](DOCS_SETUP.md) with documentation identity, purpose, scope and publication model.
4. Select the dominant documentation type profile and any secondary profiles.
5. Define the primary and secondary audiences, prior knowledge, reader tasks and preventable risks in [AUDIENCE.md](AUDIENCE.md).
6. Decide which languages are published, whether one is authoritative and how parallel documents remain aligned.
7. Establish source sensitivity, screenshot, link, feedback and visual-QA rules before importing raw materials.
8. Adapt `_quarto.yml`, `docs/` and the project-specific navigation model.
9. Complete [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) with the roadmap, current work, source model, review model and template provenance.
10. Render and inspect the initial documentation baseline before the initialization commit.

Initialization is incomplete while required purpose, audience, structure, source, publication or QA choices remain `TBD`.

## Recommended Workflows

### Documentation Workflow

```text
Setup -> Structure -> Sources -> Draft -> Visuals -> Review -> QA -> Milestone closure
```

Define the reader's starting point, goal and prerequisites before writing a tutorial procedure. Draft in small sections, validate technical truth and navigation, review links and visuals and keep current documentation separate from historical explanation.

The complete ongoing process is documented in [DOCUMENTATION_PROCESS.md](DOCUMENTATION_PROCESS.md), with profiles in [DOCUMENTATION_TYPE_PROFILES.md](DOCUMENTATION_TYPE_PROFILES.md).

### Feedback Workflows

The project supports complementary review channels:

1. **Direct source review:** maintainers edit or comment directly in Quarto or Markdown source.
2. **Maintainer DOCX review:** comments and Track Changes are transferred back to the maintained source when their intent is clear.
3. **External DOCX review:** uncurated external feedback is presented as numbered issues until the maintainer accepts, rejects, qualifies or defers it.
4. **Annotated PDF review:** layout, pagination, tables, figures and print issues are mapped back to their source locations and revalidated in the rendered format.
5. **Website review:** every artifact names the page, chapter, bundle or snapshot it covers; an ambiguous export is not treated as review of the whole site.

Assistant access, Git versioning and publication of review artifacts are separate decisions. See [FEEDBACK_WORKFLOW.md](FEEDBACK_WORKFLOW.md) for the complete traceable review cycle.

## Git Index and Protected Git Actions

The maintainer controls Git history. Assistants may inspect status, diffs and logs, prepare documentation changes and propose commit boundaries and metadata.

Staging and unstaging are index operations. They do not require a control word, but they may be performed only after a specific maintainer request or authorization of the corresponding commit. Existing staged selections and unrelated changes must be preserved.

Protected actions include commits, amendments, tags, pushes, pulls, merges, rebases, resets, branch changes, stash manipulation and other Git history operations. An assistant may perform a specific protected action only when the instruction for that action contains `explicit` or `explicitly` in English, or the German word family `explizit`. File-edit approval does not authorize Git history changes, and approval for one protected action does not authorize another.

Regular documentation commits normally use `docs:` or another fitting Conventional Commit prefix. Milestone commits omit the prefix, include the completed version and close documentation already drafted, reviewed and corrected in regular steps.

## Decision Records

Choose the record type by decision subject:

- **DDR — Documentation Decision Record:** information architecture, audience assumptions, terminology, bilingual model, screenshot policy, link model, visual standards, publication workflow or milestone scope.
- **PDR — Project Decision Record:** project scope, roadmap, collaboration, privacy, source governance or repository structure.
- **ADR — Architecture Decision Record:** Quarto structure, build pipeline, tooling, output model, automation or another durable technical documentation-system decision.

Templates live in [decisions/](decisions/). Create a record only when the rationale and consequences will matter to future maintainers; ordinary wording changes and routine corrections do not need one.

## Repository Structure

### Entry Points and Project Memory

- **`README.md` and `README.de.md`** explain the template, initial setup and ongoing use. English is authoritative, while German is maintained as a close translation.
- **`PROJECT_CONTEXT.md`** records documentation purpose, audience, source and sensitivity model, current work, roadmap, review state and next session. It is the primary re-entry point rather than a substitute for the documentation itself.
- **`CHANGELOG.md` and `VERSION`** record completed template or documentation milestones. They should reflect a reviewed state rather than work that has merely begun.

### Collaboration, Setup and Process

- **`ChatGPT.md`** defines maintainer authority, repository-first documentation work, milestones, feedback and publication boundaries.
- **`CODEX.md`** defines local assistant access, sensitive-source handling, rendering, Git and delivery rules.
- **`PROJECT_SETUP.md`, `INITIAL_PROMPT.md` and `DOCS_SETUP.md`** establish repository identity, documentation type, audience, languages, source model, Quarto system and QA expectations. The first two normally remain as initialization provenance.
- **`CONTINUATION_PROMPT.md`** reconstructs the source, review, QA and Git baseline in a later session.
- **`HARMONIZATION_PROMPT.md`** aligns a derived documentation project with its recorded template baseline, internal sources, outputs and roadmap.
- **`RETROSPECTIVE_PROMPT.md`** evaluates collaboration practices separately and controls how reusable lessons become template candidates.

### Documentation Rules and Decisions

- **`DOCUMENTATION.md` and `DOCUMENTATION_PROCESS.md`** define document roles and the ongoing path from setup through drafting, review, QA and milestone closure.
- **`DOCUMENTATION_TYPE_PROFILES.md`** adapts structure, depth, tone, examples and checks to tutorials, guides, references, concepts and other documentation types.
- **`AUDIENCE.md` and `STYLE_GUIDE.md`** make reader knowledge, tasks, risks, terminology and writing expectations explicit.
- **`LINKS.md`, `SCREENSHOTS.md` and `VISUAL_QA.md`** govern navigation, external evidence, visual capture, sensitivity, readability and publication readiness.
- **`FEEDBACK_WORKFLOW.md`** defines source-authoritative DOCX, PDF and website review cycles and the handling of maintainer versus external feedback.
- **`decisions/`** contains DDR, PDR and ADR templates and accepted durable decisions in derived projects.

### Quarto Sources, Assets and Review Artifacts

- **`_quarto.yml`** defines the documentation website, navigation, output directory and render scope. Derived projects adapt its title, pages, languages and required formats.
- **`docs/`** contains the maintained Quarto documentation sources, including English and German entry pages in the baseline. These sources are authoritative over rendered output.
- **`assets/`** contains deliberately maintained images, diagrams and other publication assets. Each artifact should have a clear purpose, provenance and sensitivity status.
- **`review/`** documents local review locations. Rendered and annotated artifacts are ignored by default because review access, Git versioning and publication require separate decisions.

## Template and Derived Project Files

In a derived documentation project:

- replace placeholder identity, audience and documentation pages with concrete project content;
- complete `DOCS_SETUP.md`, `AUDIENCE.md` and `PROJECT_CONTEXT.md`;
- adapt `_quarto.yml`, `docs/`, style, link, screenshot and visual-QA guidance;
- retain `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` as initialization provenance;
- retain the continuation, harmonization and retrospective prompts for later use;
- maintain `DOCUMENTATION.md`, `REPOSITORY.md` and `FEEDBACK_WORKFLOW.md` as active project rules;
- keep rendered and annotated artifacts local by default and version them only after deliberate review;
- create real Decision Records only for durable project, documentation or architecture choices.

Record the initial template version and commit, last harmonization baseline, lifecycle status and intentional deviations in `PROJECT_CONTEXT.md`. Concrete audience decisions and accepted Decision Records remain authoritative over later generic template changes.

## How to Use This Template

1. Initialize the repository through `INITIAL_PROMPT.md`, `PROJECT_SETUP.md` and `DOCS_SETUP.md`.
2. Select the documentation type profile and define audience, language and publication requirements.
3. Establish the source inventory and sensitivity boundaries before opening screenshots, logs, exports, tickets or operational data.
4. Define the information architecture before large-scale drafting.
5. Maintain documentation in `docs/` and connect every visual and link to a real reader task or evidence need.
6. Draft, render and review in small increments.
7. Transfer accepted DOCX, PDF or website feedback back to the maintained source and revalidate it there.
8. Record consequential DDRs, PDRs or ADRs in `decisions/`.
9. Keep `PROJECT_CONTEXT.md` current and use `CONTINUATION_PROMPT.md` for later sessions.
10. Close milestones only after technical, audience, link, visual, render and disclosure QA.

## Maintainer Tool Setup

For the standard Quarto workflow:

1. Install the [Quarto CLI](https://quarto.org/docs/get-started/) and verify it with `quarto --version`.
2. Open the repository as the active local workspace and run `quarto render` to validate the HTML baseline.
3. Install a TeX toolchain such as TinyTeX only when direct PDF output is required.
4. Install LibreOffice when DOCX outputs must be rendered to PDF or page images for visual QA.
5. Use R and RStudio only when the documentation includes R code, data analysis, plots or R-based Quarto extensions; they are not required for ordinary Markdown documentation.

Keep generated sites, previews, raw captures and review artifacts in the ignored locations defined by `.gitignore` unless the project deliberately approves a versioned artifact.

## Continuous Improvement

Use harmonization to reconcile a derived documentation project with relevant template developments, current audience needs, maintained sources, outputs and roadmap. Use retrospectives separately to evaluate collaboration, handoffs and review practices.

Reusable improvements should be integrated across affected guidance instead of appended as isolated notes. A single project observation is not automatically a template rule, and publication decisions remain with the maintainer.

## License

This template is distributed under the [MIT License](LICENSE).
