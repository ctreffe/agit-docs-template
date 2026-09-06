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
> The collaboration model documents documentation practices, AI-assisted documentation workflows, link and visual-inspection discipline and repository conventions for documentation projects.
>
> Its collaboration model is maintained in [COLLABORATION.md](COLLABORATION.md).

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

Use this template when audience, structure, task guidance, links, screenshots, visual inspection and publication format are central from the beginning. It is particularly useful when documentation must remain reviewable across languages, output formats or feedback cycles.

Use the generic Project Template when documentation is one part of a broader project. Use the Dev Template when implementation lifecycle is primary and documentation mainly accompanies software behavior.

## Project Initialization

After creating the repository, the maintainer invokes `$start-project`. The skill reads the repository and all setup guidance, then leads the complete documentation initialization. The maintainer does not need to open or execute `PROJECT_SETUP.md` or `DOCS_SETUP.md` separately.

The simplest instruction to the agent is:

> `$start-project`

There is no initialization prompt to open or copy into the conversation.
Before the normal questionnaire, the agent offers one concise choice between
the normal lean path and the explicit `$grill-me` path for detailed
documentation planning. The choice grants no source-access, rendering or
publication authority.

The agent then:

1. reads the collaboration, documentation, setup, repository and decision rules;
2. inspects the baseline without altering Git history;
3. follows the selected path and, on the lean path, asks no more than six
   unanswered fundamentals covering documentation purpose, audience and use,
   the first useful document outcome and its evidence, current scope and
   non-goals, source access and sensitivity, and only constraints needed now;
4. preserves source, screenshot, feedback, rendering and publication gates
   while allowing nonessential decisions to remain explicitly deferred;
5. adapts only the setup, audience, README, Quarto, source and navigation files needed for the first useful outcome;
6. records its initial document contract in `DOCUMENTS.md` and the current source boundary and template provenance in `PROJECT_CONTEXT.md`;
7. renders or visually inspects only when the requested artifact or necessary evidence requires it; and
8. hands back the initialized state with proportionate checks, unresolved decisions and suggested commit metadata.

`PROJECT_SETUP.md` and `DOCS_SETUP.md` remain agent checklists and initialization provenance. `$start-project` is the single executable entry point that activates them.

For a project that should remain local and have no remote, invoke
`$create-local-project` explicitly in this checked-out template. It creates an
independent local clone without a remote and then invokes `$start-project`.
After successful initialization, inherited template history in `CHANGELOG.md`
and `TASK_HANDOFF.md` is replaced with project-owned state. The template-only
`IDEAS.md`, the project's copy of `$create-local-project` and their references
are removed unless a project-local idea backlog is deliberately established.
The initialization files remain as provenance.

## Adding Maintained Documents

An initialized project may remain a one-document project or grow into a
multi-document set. Invoke `$add-document` explicitly for each additional
maintained document or language-linked document set. The workflow confirms its
document-local contract in `DOCUMENTS.md`, rejects path and ID collisions and
updates agreed source skeletons or navigation without rerunning project
initialization. Rendering, publication and Git actions remain separate.

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

Assistant access, Git versioning and publication are separate decisions. Moving
a file records classification but grants no additional permission. Move
accepted textual content to `docs/`, reviewed binary documentation material
approved for Git to `materials/versioned/`, and returned annotated review
files to `review/`; preserve provenance in the applicable catalog.

For large non-Git files that must remain available across devices, use the
provider-neutral workflow in [SYNCHRONIZED_STORAGE.md](SYNCHRONIZED_STORAGE.md).
Synchronized files remain external storage; synchronization is not Git
versioning, backup, assistant access or publication approval.

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
are discarded, transferred into textual documentation or approved for Git as
maintained binary documentation material.

Register each retained file in `materials/CATALOG.md` with its purpose,
transformation and `Based on` provenance. Use ignored `materials/local/` for
**`local`** files, `materials/versioned/` for **`versioned`** files, and a
stable logical catalog location for **`external`** files. Resolve external
locations per machine in ignored `materials/PATHS.local.md`, copied from
`materials/PATHS.local.example.md`.

Assistant access does not authorize Git versioning or publication. Move
accepted textual content to `docs/`; move reviewed binary documentation
material to `materials/versioned/` only after Git approval. Keep presentation
source in `styles/`, returned annotated review files in `review/` and generated
outputs below `output/`.

Generation method does not determine location. Keep a generated file in
`materials/` when it is a durable working or source file consumed by later
documentation steps. Place it in `output/<format>/` when it is a generated
project result intended for use, review, handoff, publication or delivery.
Disposable generation intermediates remain in `temp/`; maintained `docs/`,
`materials/versioned/` and `styles/` sources keep their authoritative
locations.

## Render Validation and Visual Inspection

Routine render and output validation may run Quarto and inspect the generated
HTML technically without opening the Browser skill. It checks build success,
warnings, required files, HTML structure, links, referenced assets and obvious
unrendered source content as relevant. This does not count as visual
inspection.

Invoke `$visual-inspection` explicitly when the agent should inspect named
current renders in maintainer-selected formats. It opens rendered HTML with the
Browser skill or inspects selected PDF/DOCX pages as page images. A milestone,
render or visual change does not trigger this workflow. Missing output is not
rendered or replaced, and the report names inspected pages, routes, viewports,
findings and limitations. Visual inspection does not certify accessibility,
technical correctness, disclosure approval or publication readiness.

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
4. **Annotated PDF review:** layout, pagination, tables, figures and print issues are mapped back to their source locations; the changed source is rendered and technically validated, while agent visual inspection remains a separate, explicitly invoked workflow.
5. **Website review:** every review file names the page, chapter, bundle or snapshot it covers; an ambiguous export is not treated as review of the whole site.

Assistant access, Git versioning and publication of review files are separate decisions. See [FEEDBACK_WORKFLOW.md](FEEDBACK_WORKFLOW.md) for the complete traceable review cycle.

## Git Index and Protected Git Actions

The maintainer controls Git history. Assistants may inspect status, diffs and logs, prepare documentation changes and propose commit boundaries and metadata.

Staging and unstaging are index operations. They do not require a control word, but they may be performed only after a specific maintainer request or authorization of the corresponding commit. Existing staged selections and unrelated changes must be preserved.

Protected actions include commits, amendments, tags, pushes, pulls, merges, rebases, resets, branch changes, stash manipulation and other Git history operations. An assistant may perform a specific protected action only when the instruction for that action contains `explicit` or `explicitly` in English, or the German word family `explizit`. File-edit approval does not authorize Git history changes, and approval for one protected action does not authorize another.

When this rule requires authorization, the assistant proposes one minimum-scope,
copy-ready instruction naming the exact action, repository and material
consequence. The proposal itself is not authorization.

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
- **`DOCUMENTS.md`** catalogs each maintained document or language-linked set,
  its reviewed project-default inheritance, lifecycle and next action.
- **`CHANGELOG.md` and `VERSION`** record completed template or documentation milestones. They should reflect a reviewed state rather than work that has merely begun.

### Collaboration, Setup and Process

- **`AGENTS.md`** is the compact resident safety and routing contract for AI agents.
- **`COLLABORATION.md`** defines provider-neutral documentation authority, evidence, feedback and publication boundaries.
- **`PROJECT_SETUP.md` and `DOCS_SETUP.md`** establish repository identity, documentation type, audience, languages, source model, Quarto system and QA expectations. `PROJECT_SETUP.md` remains as initialization provenance.
- **`.agents/skills/`** provides lean automatic task lifecycle, commit and
  environment-troubleshooting workflows plus explicit initialization, neutral
  document addition, visual inspection, review, synchronization, consistency,
  document revision and retrospective workflows. The `$grill-me` path and its
  `grilling` primitive are explicit-only and never replace normal lean
  initialization.
- **`TROUBLESHOOTING.md`** stores portable focused-resolution problems and
  verified repairs; ignored `TROUBLESHOOTING.local.md` stores host-specific
  facts. A quick exit loads or records neither.
- **`TASK_HANDOFF.md`** carries the compact versioned task checkpoint across
  sessions and computers.
- **`IDEAS.md`** is a source-template backlog for reusable documentation
  candidates and is removed during normal project initialization unless a
  project-local backlog is deliberately retained.

### Documentation Rules and Decisions

- **`DOCUMENTATION.md` and `DOCUMENTATION_PROCESS.md`** define document roles and the ongoing path from setup through drafting, review, QA and milestone closure.
- **`DOCUMENTATION_TYPE_PROFILES.md`** adapts structure, depth, tone, examples and checks to tutorials, guides, references, concepts and other documentation types.
- **`AUDIENCE.md` and `STYLE_GUIDE.md`** make reader knowledge, tasks, risks, terminology and writing expectations explicit.
- **`LINKS.md` and `SCREENSHOTS.md`** govern navigation, external evidence, visual capture, sensitivity and source-level visual rules; `$visual-inspection` carries its rendered-surface criteria directly.
- **`FEEDBACK_WORKFLOW.md`** defines source-authoritative DOCX, PDF and website review cycles and the handling of maintainer versus external feedback.
- **`decisions/`** contains DDR, PDR and ADR templates and accepted durable decisions in derived projects.

### Quarto Sources, Materials, Outputs and Review Files

- **`_quarto.yml`** defines the documentation website, navigation, output directory and render scope. Derived projects adapt its title, pages, languages and required formats.
- **`docs/`** contains the maintained Quarto documentation sources, including English and German entry pages in the baseline. These sources are authoritative over rendered output.
- **`input/`** classifies incoming external files and records their provenance before they enter maintained documentation workflows.
- **`materials/`** catalogs retained assistant-readable documentation working
  files in local, versioned or external storage.
- **`temp/`** holds ignored, never-versioned documentation intermediates, with
  `temp/restricted/` as the inaccessible exception.
- **`materials/versioned/`** contains reviewed binary documentation material
  approved for Git. Every file needs a clear purpose, provenance and
  sensitivity status; publication remains separate.
- **`styles/`** contains maintained presentation source when needed.
- **`output/`** contains ignored generated results separated by format, such as
  `output/html/`, `output/pdf/` or `output/docx/`.
- **`review/`** contains ignored returned annotated review files directly;
  generated review outputs remain under `output/<format>/`.

## Template and Derived Project Files

In a derived documentation project:

- replace placeholder identity, audience and documentation pages with concrete project content;
- retain and adapt `AGENTS.md` as the automatic agent entry point;
- complete `DOCS_SETUP.md`, `AUDIENCE.md`, `PROJECT_CONTEXT.md` and the initial
  `DOCUMENTS.md` entry;
- adapt `_quarto.yml`, `docs/`, style, link, screenshot and visual-inspection guidance;
- retain `PROJECT_SETUP.md` as initialization provenance;
- retain the applicable repository skills for later workflows;
- invoke `$add-document` explicitly for each later maintained document or
  language-linked document set;
- invoke `$visual-inspection` explicitly only for named current renders and
  maintainer-selected formats;
- maintain `DOCUMENTATION.md`, `REPOSITORY.md` and `FEEDBACK_WORKFLOW.md` as active project rules;
- keep generated outputs and returned annotated review files local by default
  and version them only after deliberate review;
- create real Decision Records only for durable project, documentation or architecture choices.

Record the initial template version and commit, last harmonization baseline, lifecycle status and intentional deviations in `PROJECT_CONTEXT.md`. Concrete audience decisions and accepted Decision Records remain authoritative over later generic template changes.

## How to Use This Template

1. Create a repository from the template and invoke `$start-project`.
2. Choose the normal lean path or explicitly opt into `$grill-me`; on the lean
   path, answer no more than six unanswered documentation fundamentals while
   the agent applies the retained setup guidance automatically.
3. Review the initialized documentation state, render checks and proposed first commit.
4. Select the documentation type profile and confirm audience, language and publication requirements with the agent.
5. Establish the source inventory and sensitivity boundaries before opening screenshots, logs, exports, tickets or operational data.
6. Define the information architecture before large-scale drafting, then draft, render and review in small increments.
7. Connect every visual and link to a real reader task or evidence need.
8. Transfer accepted feedback back to the maintained source and revalidate it there.
9. Record consequential decisions, keep `PROJECT_CONTEXT.md` current and use
   `start-task` with `TASK_HANDOFF.md` for later bounded tasks.
10. Close milestones only after technical, audience, link, visual, render and disclosure QA.

## Maintainer Tool Setup

For the standard Quarto workflow:

1. Install the [Quarto CLI](https://quarto.org/docs/get-started/) and verify it with `quarto --version`.
2. Open the repository as the active local workspace and run `quarto render` to validate the HTML baseline.
3. Follow Quarto's [TinyTeX and PDF-engine guidance](https://quarto.org/docs/output-formats/pdf-engine) only when direct PDF output is required.
4. Install [LibreOffice](https://www.libreoffice.org/download/instructions/) when an explicitly selected current DOCX output must be converted to page images for `$visual-inspection`.
5. Use [R](https://cran.r-project.org/) and [RStudio](https://posit.co/downloads/) only when the documentation includes R code, data analysis, plots or R-based Quarto extensions; they are not required for ordinary Markdown documentation.

Keep generated sites, previews, unreviewed captures and review files in the ignored locations defined by `.gitignore` unless the project deliberately approves a versioned file or output.

## Continuous Improvement

Use `$sync-template` to compare a derived documentation project with its verified source-template baseline and adopt selected developments. Use `$check-consistency` separately for contradictions among audience needs, maintained sources, outputs and roadmap, and `$perform-retrospective` for collaboration, handoffs and review practices.

Treat feedback patterns, navigation problems, rendering failures, visual-inspection findings and publication lessons as evidence for possible improvement. A single project observation is not automatically a template rule; consider audience, documentation type, output format and maintenance cost before generalizing it.

The maintainer coordinates cross-template evolution in a private governance repository named `agit-templateverse`. It records shared conventions, deliberate specializations and evidence from derived projects. The repository is intentionally not linked because template users do not need access to it.

Governance coordination does not create hidden documentation requirements. Every change that affects this template must be represented here through maintained guidance, Documentation Decision Records where appropriate, the changelog and release history. Reusable improvements should be integrated across affected source, feedback, rendering and QA guidance, while publication decisions remain with the maintainer.

## License

This template is distributed under the [MIT License](LICENSE).
