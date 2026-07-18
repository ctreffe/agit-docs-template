# Documentation Architecture

This file explains the documentation model of this template repository and the role of its core files.

## Template layers

The repository separates reusable template guidance from project-specific documentation.

Template files describe how a documentation project should be initialized, maintained, reviewed, and evolved. In a derived project, these files should be adapted to the concrete documentation context.

## Core files

- `README.md` and `README.de.md`: Public-facing overview of the template.
- `ChatGPT.md`: Versioned AI collaboration model.
- `CODEX.md`: Local operating rules for the assistant.
- `PROJECT_SETUP.md`: Initial repository setup workflow.
- `INITIAL_PROMPT.md`: Reproducible first prompt for project initialization.
- `CONTINUATION_PROMPT.md`: Reproducible re-entry prompt for a new context
  window or assistant session.
- `DOCS_SETUP.md`: Documentation-specific setup checklist.
- `PROJECT_CONTEXT.md`: Project memory template.
- `DOCUMENTATION_PROCESS.md`: Ongoing documentation workflow.
- `DOCUMENTATION_TYPE_PROFILES.md`: Documentation type profiles and profile-specific QA guidance.
- `QUARTO.md`: Quarto source format, rendering, bilingual structure, and output QA.
- `AUDIENCE.md`: Audience model template.
- `STYLE_GUIDE.md`: Writing and style guidance for technical documentation.
- `SCREENSHOTS.md`: Screenshot and visual artifact guidance.
- `LINKS.md`: Internal and external link discipline.
- `VISUAL_QA.md`: Visual documentation QA checklist.
- `REPOSITORY.md`: Repository organization and lifecycle rules.
- `decisions/`: Decision Records, including DDRs, PDRs and ADRs.

## Current state and history

Derived projects should distinguish between current documentation state and project history. The main documentation should describe what is true now. Historical rationale belongs in decision records, changelog entries, or dedicated notes when needed.

## Documentation artifacts

Technical documentation may contain Quarto Markdown sources, text, diagrams, screenshots, exported PDFs, generated pages, recordings, and structured reference data. The repository should make clear which artifacts are source material, which are maintained documentation, and which are generated output.

## Sensitive material

Raw screenshots, logs, exports, configuration values, internal URLs, and user data can be sensitive. They should not be committed or read by the assistant until the maintainer has confirmed that this is appropriate.

If documentation requires evidence from sensitive material, create sanitized derivatives or redacted artifacts whenever possible.
