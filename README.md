# AGIT Documentation Template

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

Template for AI-assisted technical documentation in AGIT contexts, with repository-first workflows, link discipline, screenshots, visual QA, and documented decisions.

This repository provides a starting point for technical documentation projects that should be maintained with the same rigor as software and scientific writing projects: explicit context, clear ownership, reproducible collaboration, documented decisions, and reviewable milestones.

German README: [README.de.md](README.de.md)

## Core principle

The maintainer owns the documentation intent, structure, technical correctness, audience fit, and final publication decision at all times. The AI assistant supports drafting, consistency checks, link discipline, screenshot and visual QA, structural feedback, and repository maintenance, but does not replace maintainer judgment.

## What this template is for

Use this template for documentation projects such as:

- User guides, admin guides, and operating procedures.
- Technical concepts, architecture notes, and implementation documentation.
- Troubleshooting, migration, setup, and release documentation.
- Documentation systems that combine prose, screenshots, diagrams, links, and generated output.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

Start from the Documentation Template when audience, structure, screenshots, links, visual QA and publication format are central from the beginning. Start from the generic Project Template when documentation is only one part of a broader project.

## Repository workflow

1. Start from [INITIAL_PROMPT.md](INITIAL_PROMPT.md).
2. Complete [PROJECT_SETUP.md](PROJECT_SETUP.md) and [DOCS_SETUP.md](DOCS_SETUP.md).
3. Define project-specific context in [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md).
4. Establish documentation type, audience, bilingual needs, Quarto structure, link, screenshot, and visual QA rules.
5. Draft documentation in small, reviewable increments.
6. Record substantial decisions in `decisions/`, usually as DDRs.
7. Close meaningful milestones with changelog, version, and consistency review.

## Maintainer setup

For a new Codex-based documentation project, use this setup sequence:

1. Create a new repository from this template and clone it locally.
2. Open the repository as the active Codex workspace.
3. Install the Quarto CLI from <https://quarto.org/docs/get-started/>.
4. Open a new terminal and verify Quarto with `quarto --version`.
5. If PDF output is required, install a TeX toolchain, for example with `quarto install tinytex`.
6. Verify the Quarto baseline with `quarto render`.
7. Start project initialization with [INITIAL_PROMPT.md](INITIAL_PROMPT.md).
8. Complete [PROJECT_SETUP.md](PROJECT_SETUP.md), [DOCS_SETUP.md](DOCS_SETUP.md), and [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md).

R and RStudio are useful when the documentation includes R code, data analysis, plots, or R-based Quarto extensions, but they are not required for simple Markdown-based documentation.

## Important files

- [ChatGPT.md](ChatGPT.md): Versioned AI collaboration model.
- [CODEX.md](CODEX.md): Local assistant operating rules.
- [DOCUMENTATION.md](DOCUMENTATION.md): Documentation architecture and file roles.
- [PROJECT_SETUP.md](PROJECT_SETUP.md): Initialization workflow for derived projects.
- [DOCS_SETUP.md](DOCS_SETUP.md): Documentation-specific setup checklist.
- [DOCUMENTATION_PROCESS.md](DOCUMENTATION_PROCESS.md): Ongoing documentation workflow.
- [DOCUMENTATION_TYPE_PROFILES.md](DOCUMENTATION_TYPE_PROFILES.md): Documentation type profiles, including the tutorial profile.
- [QUARTO.md](QUARTO.md): Quarto as the preferred internal documentation format.
- [AUDIENCE.md](AUDIENCE.md): Audience model template.
- [STYLE_GUIDE.md](STYLE_GUIDE.md): Technical documentation style principles.
- [SCREENSHOTS.md](SCREENSHOTS.md): Screenshot and visual evidence rules.
- [LINKS.md](LINKS.md): Link and reference discipline.
- [VISUAL_QA.md](VISUAL_QA.md): Visual QA checklist.
- [decisions/](decisions/): Decision Records, including DDRs, PDRs and ADRs.

## License

This template is distributed under the MIT License. See [LICENSE](LICENSE).
