# Documentation Architecture

This file explains the documentation model of this template repository and the role of its core files.

## Template layers

The repository separates reusable template guidance from project-specific documentation.

Template files describe how a documentation project should be initialized, maintained, reviewed, and evolved. In a derived project, these files should be adapted to the concrete documentation context.

## Core files

- `README.md` and `README.de.md`: Public-facing template overview in source
  checkouts; project introduction after initialization.
- `TEMPLATE_README.md` and `TEMPLATE_README.de.md`: Adapted workflow guides
  retained only in initialized projects.
- `AGENTS.md`: Automatically loaded entry point that routes AI agents to the
  complete documentation, source-safety and validation guidance.
- `COLLABORATION.md`: Versioned AI collaboration model.
- `PROJECT_SETUP.md`: Initial repository setup workflow.
- `$start-project`: Explicit one-time project initialization skill.
- `$add-document`: Explicit workflow for adding one maintained document or
  language-linked document set after initialization.
- `.agents/skills/`: Scoped automatic lifecycle and explicit specialized
  documentation collaboration workflows.
- `TASK_HANDOFF.md`: Compact versioned task checkpoint.
- `DOCS_SETUP.md`: Documentation-specific setup checklist.
- `DOCUMENTS.md`: Maintained document catalog and document-local contracts.
- `PROJECT_CONTEXT.md`: Project memory template.
- `DOCUMENTATION_PROCESS.md`: Ongoing documentation workflow.
- `FEEDBACK_WORKFLOW.md`: Direct-source, annotated DOCX and annotated PDF
  review workflow.
- `DOCUMENTATION_TYPE_PROFILES.md`: Documentation type profiles and profile-specific QA guidance.
- `QUARTO.md`: Quarto source format, rendering, bilingual structure, and output QA.
- `AUDIENCE.md`: Audience model template.
- `STYLE_GUIDE.md`: Writing and style guidance for technical documentation.
- `SCREENSHOTS.md`: Screenshot and visual-file guidance.
- `LINKS.md`: Internal and external link discipline.
- `REPOSITORY.md`: Repository organization and lifecycle rules.
- `decisions/`: Decision Records, including DDRs, PDRs and ADRs.

## README language policy

In source-template checkouts, `README.md` is the English source text and
`README.de.md` is its close structural and semantic German translation. In
initialized projects this applies independently to the project pair and the
retained guide pair. Both pairs are required; the project introduction and
the guide have different roles and are not translations of one another.

## Project and guide README roles

After initialization, `README.md` and `README.de.md` introduce the actual project
and link early to its workflows and skills. `TEMPLATE_README.md` and
`TEMPLATE_README.de.md` retain adapted inherited operating guidance. Both pairs
are required, have reciprocal language links within the pair and link between
project introduction and guide in the same language. Follow `PROJECT_SETUP.md`
for safe renaming, interrupted setup and final inventory review. Local resident
and domain rules and accepted decisions remain authoritative. Keep guide links,
identity and license wording accurate and omit inherited guide badges. Badge
policy applies to source-template or project introductions, not guides.
Selected upstream README updates map to the guides through `sync-template`,
without replacing the project introductions. Source checkouts retain their
original pair; existing projects are not automatically migrated.

## README badges

Place the badge block directly below the README title and before the AI
Collaboration Note. Use status, version and license in that order, followed
only by badges for real documentation automation such as a site build, render
or link check. Link the standard badges to `VERSION`, `CHANGELOG.md` and
`LICENSE`.

Badges must reflect maintained documentation state rather than decorate the
README. Derived projects replace template values with their own status,
completed version, actual license and available workflows. Avoid a last-commit
badge because activity is not documentation quality or publication readiness.
Keep English and German badge blocks identical and update static badges with
the metadata they represent.

## Current state and history

Derived projects should distinguish between current documentation state and project history. The main documentation should describe what is true now. Historical rationale belongs in decision records, changelog entries, or dedicated notes when needed.

## Documentation files

Technical documentation may contain Quarto Markdown sources, text, diagrams,
screenshots, exported DOCX or PDF files, generated pages, review annotations,
recordings, and structured reference data. The repository should make clear
which files are source material, which are maintained documentation, which
are review files, and which are generated output.

Rendered or annotated DOCX and PDF files do not replace their maintained
sources. Accepted feedback is complete only after it has been transferred to
the authoritative source and validated there.

## Sensitive material

Raw screenshots, logs, exports, configuration values, internal URLs, and user data can be sensitive. They should not be committed or read by the assistant until the maintainer has confirmed that this is appropriate.

If documentation requires evidence from sensitive material, create sanitized derivatives or redacted files whenever possible.
