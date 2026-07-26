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

<br>

**[Link zur deutschen README](README.de.md)**

<br>

## Contents

- [Overview](#overview)
- [Core Principle](#core-principle)
- [AGIT Templateverse](#agit-templateverse)
- [When to Use This Template](#when-to-use-this-template)
- [Project Initialization](#project-initialization)
- [External Files and Sources](#external-files-and-sources)
- [Temporary Working Files](#temporary-working-files)
- [Project Materials](#project-materials)
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

Quarto Markdown is the preferred maintained source format. The baseline renders a bilingual HTML website and can be adapted for DOCX or PDF review outputs when a project needs them. Links, screenshots, diagrams and generated outputs are treated as documentation files with provenance, sensitivity review and quality assurance.

## Core Principle

The maintainer owns documentation purpose, scope, structure, technical correctness, audience fit and publication decisions. The assistant may help draft, restructure, check consistency, plan visuals and review outputs, but it does not replace maintainer judgment or make publication decisions.

Maintained repository sources are authoritative. Rendered websites, DOCX files, PDFs and annotated returns are outputs or review files until accepted feedback has been transferred back to the source and validated there.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

## When to Use This Template

Use this template when audience, structure, task guidance, links, screenshots, visual QA and publication format are central from the beginning. It is particularly useful when documentation must remain reviewable across languages, output formats or feedback cycles.

Use the generic Project Template when documentation is one part of a broader project. Use the Dev Template when implementation lifecycle is primary and documentation mainly accompanies software behavior.

## Project Initialization

After creating the repository, the maintainer needs to invoke only [INITIAL_PROMPT.md](INITIAL_PROMPT.md). The agent reads the repository and all setup guidance, then leads the complete documentation initialization. The maintainer does not need to open or execute `PROJECT_SETUP.md` or `DOCS_SETUP.md` separately.

The simplest instruction to the agent is:

> Read `INITIAL_PROMPT.md` in full and carry out the initialization prompt it contains.

There is no need to open the file and copy its prompt into the conversation.

The agent then:

1. reads the collaboration, documentation, setup, repository and decision rules;
2. inspects the baseline without altering Git history;
3. presents concise questions about purpose, scope, documentation type, audiences, languages, publication and QA;
4. asks for source-sensitivity, screenshot, feedback and visual-review decisions before importing raw material;
5. adapts `DOCS_SETUP.md`, `AUDIENCE.md`, the README files, `_quarto.yml`, `docs/` and navigation after the maintainer answers;
6. records the roadmap, source model, review model and template provenance in `PROJECT_CONTEXT.md`;
7. renders and inspects the initial documentation baseline; and
8. hands back the initialized state with checks, unresolved decisions and suggested commit metadata.

`PROJECT_SETUP.md` and `DOCS_SETUP.md` remain agent checklists and initialization provenance. `INITIAL_PROMPT.md` is the single user-facing entry point that activates them.

For a project that should remain local and have no remote, begin in this
checked-out template with [CREATE_LOCAL_PROJECT_PROMPT.md](CREATE_LOCAL_PROJECT_PROMPT.md).
It verifies the destination, creates an independent local clone without a
remote, then invokes `INITIAL_PROMPT.md`; it is not a second initialization.

## External Files and Sources

Place newly received screenshots, exports, logs, tickets, reference documents and other external files in `input/intake/` before deciding how they may be used. Record safe metadata, provenance and classification in `input/CATALOG.md`; use the ignored `input/CATALOG.local.md` when filenames, paths or details are themselves sensitive.

Catalog unchanged external services, datasets and URLs even when their content
remains outside the repository. Use stable public URLs directly and resolve
logical private or device-specific locations through ignored
`input/PATHS.local.md`.

- **`input/intake/`** is the ignored arrival area for unclassified files. Presence never authorizes assistant access.
- **`input/restricted/`** is ignored and reserved for files that only the maintainer, or explicitly approved local checks, may inspect.
- **`input/local/`** is ignored and holds files the assistant may process locally but that must not enter Git.
- **`input/versioned/`** contains reviewed external files that may be committed.

Assistant access, Git versioning and publication are separate decisions. Moving a file records classification but grants no additional permission. Once an approved file becomes maintained documentation, a publication asset or a review input, move it to `docs/`, `assets/` or `review/` when that location better communicates its role, and preserve its provenance in the catalog.

## Temporary Working Files

Use `temp/` for disposable documentation intermediates. All contents outside
`temp/restricted/` are assistant-readable; that restricted directory must not
be enumerated or read. All temporary content is ignored, must never be versioned
and is not cataloged. Promote retained files to `materials/` before any later
promotion to maintained documentation.

## Project Materials

Keep files in `input/` unchanged. OCR text, cropped or annotated screenshots,
converted references and other edited copies are new project materials.
`materials/` retains these assistant-readable working foundations until they
are discarded or deliberately promoted into maintained documentation or
publication assets.

Register each retained file in `materials/CATALOG.md` with its purpose,
transformation and `Based on` provenance. Use ignored `materials/local/` for
**`local`** files, `materials/versioned/` for **`versioned`** files, and a
stable logical catalog location for **`external`** files. Resolve external
locations per machine in ignored `materials/PATHS.local.md`, copied from
`materials/PATHS.local.example.md`.

Assistant access does not authorize Git versioning or publication. Review and
promote files to `docs/` or `assets/` only when they become maintained
documentation content; keep review packages, caches and final publication
outputs in their established locations.

Generation method does not determine location. Keep a generated file in
`materials/` when it is a durable working or source file consumed by later
documentation steps. Place it in `output/` or the documented publication
location when it is a project result intended for use, review, handoff,
publication or delivery. Disposable generation intermediates remain in
`temp/`; maintained `docs/` sources and publication `assets/` keep their
authoritative locations.

## Render Validation and Visual QA

Routine render and output validation may run Quarto and inspect the generated
HTML technically without opening the Browser skill. It checks build success,
warnings, required files, HTML structure, links, referenced assets and obvious
unrendered source content as relevant. This does not count as visual QA.

Visual QA means that the agent actually inspects rendered HTML with the Browser
skill or rendered PDF/DOCX page images with the appropriate visual tool. The
agent performs it only before milestone closure or when the maintainer
explicitly requests it. Visual or layout changes alone do not trigger agent
visual QA; the maintainer owns visual inspection during ordinary work. If the
required tool or output is unavailable, the agent reports that visual QA was
not performed.

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
4. **Annotated PDF review:** layout, pagination, tables, figures and print issues are mapped back to their source locations; the changed source is rendered and technically validated, while agent visual QA follows the milestone-or-explicit-request rule.
5. **Website review:** every review file names the page, chapter, bundle or snapshot it covers; an ambiguous export is not treated as review of the whole site.

Assistant access, Git versioning and publication of review files are separate decisions. See [FEEDBACK_WORKFLOW.md](FEEDBACK_WORKFLOW.md) for the complete traceable review cycle.

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

- **`README.md` and `README.de.md`** explain the template, initial setup and ongoing use in English and German.
- **`PROJECT_CONTEXT.md`** records documentation purpose, audience, source and sensitivity model, current work, roadmap, review state and next session. It is the primary re-entry point rather than a substitute for the documentation itself.
- **`CHANGELOG.md` and `VERSION`** record completed template or documentation milestones. They should reflect a reviewed state rather than work that has merely begun.

### Collaboration, Setup and Process

- **`AGENTS.md`** is the concise, automatically loaded entry point for AI agents. It routes them to the complete documentation, source-safety and validation guidance without duplicating it.
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

### Quarto Sources, Assets and Review Files

- **`_quarto.yml`** defines the documentation website, navigation, output directory and render scope. Derived projects adapt its title, pages, languages and required formats.
- **`docs/`** contains the maintained Quarto documentation sources, including English and German entry pages in the baseline. These sources are authoritative over rendered output.
- **`input/`** classifies incoming external files and records their provenance before they enter maintained documentation workflows.
- **`materials/`** catalogs retained assistant-readable documentation working
  files in local, versioned or external storage.
- **`temp/`** holds ignored, never-versioned documentation intermediates, with
  `temp/restricted/` as the inaccessible exception.
- **`assets/`** contains deliberately maintained images, diagrams and other publication files. Each file should have a clear purpose, provenance and sensitivity status.
- **`review/`** documents local review locations. Rendered and annotated review files are ignored by default because review access, Git versioning and publication require separate decisions.

## Template and Derived Project Files

In a derived documentation project:

- replace placeholder identity, audience and documentation pages with concrete project content;
- retain and adapt `AGENTS.md` as the automatic agent entry point;
- complete `DOCS_SETUP.md`, `AUDIENCE.md` and `PROJECT_CONTEXT.md`;
- adapt `_quarto.yml`, `docs/`, style, link, screenshot and visual-QA guidance;
- retain `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` as initialization provenance;
- retain the continuation, harmonization and retrospective prompts for later use;
- maintain `DOCUMENTATION.md`, `REPOSITORY.md` and `FEEDBACK_WORKFLOW.md` as active project rules;
- keep rendered and annotated review files local by default and version them only after deliberate review;
- create real Decision Records only for durable project, documentation or architecture choices.

Record the initial template version and commit, last harmonization baseline, lifecycle status and intentional deviations in `PROJECT_CONTEXT.md`. Concrete audience decisions and accepted Decision Records remain authoritative over later generic template changes.

## How to Use This Template

1. Create a repository from the template and give the agent the instruction in `INITIAL_PROMPT.md`.
2. Answer the numbered questions the agent presents; it reads and applies `PROJECT_SETUP.md`, `DOCS_SETUP.md` and the remaining setup guidance automatically.
3. Review the initialized documentation state, render checks and proposed first commit.
4. Select the documentation type profile and confirm audience, language and publication requirements with the agent.
5. Establish the source inventory and sensitivity boundaries before opening screenshots, logs, exports, tickets or operational data.
6. Define the information architecture before large-scale drafting, then draft, render and review in small increments.
7. Connect every visual and link to a real reader task or evidence need.
8. Transfer accepted feedback back to the maintained source and revalidate it there.
9. Record consequential decisions, keep `PROJECT_CONTEXT.md` current and use `CONTINUATION_PROMPT.md` for later sessions.
10. Close milestones only after technical, audience, link, visual, render and disclosure QA.

## Maintainer Tool Setup

For the standard Quarto workflow:

1. Install the [Quarto CLI](https://quarto.org/docs/get-started/) and verify it with `quarto --version`.
2. Open the repository as the active local workspace and run `quarto render` to validate the HTML baseline.
3. Follow Quarto's [TinyTeX and PDF-engine guidance](https://quarto.org/docs/output-formats/pdf-engine) only when direct PDF output is required.
4. Install [LibreOffice](https://www.libreoffice.org/download/instructions/) when DOCX outputs must be rendered to PDF or page images for visual QA.
5. Use [R](https://cran.r-project.org/) and [RStudio](https://posit.co/downloads/) only when the documentation includes R code, data analysis, plots or R-based Quarto extensions; they are not required for ordinary Markdown documentation.

Keep generated sites, previews, unreviewed captures and review files in the ignored locations defined by `.gitignore` unless the project deliberately approves a versioned file or output.

## Continuous Improvement

Use harmonization to reconcile a derived documentation project with relevant template developments, current audience needs, maintained sources, outputs and roadmap. Use retrospectives separately to evaluate collaboration, handoffs and review practices.

Treat feedback patterns, navigation problems, rendering failures, visual-QA findings and publication lessons as evidence for possible improvement. A single project observation is not automatically a template rule; consider audience, documentation type, output format and maintenance cost before generalizing it.

The maintainer coordinates cross-template evolution in a private governance repository named `agit-templateverse`. It records shared conventions, deliberate specializations and evidence from derived projects. The repository is intentionally not linked because template users do not need access to it.

Governance coordination does not create hidden documentation requirements. Every change that affects this template must be represented here through maintained guidance, Documentation Decision Records where appropriate, the changelog and release history. Reusable improvements should be integrated across affected source, feedback, rendering and QA guidance, while publication decisions remain with the maintainer.

## License

This template is distributed under the [MIT License](LICENSE).
