# Changelog

All notable changes to this template will be documented in this file.

## [Unreleased]

## [v0.3.0] - 2026-07-19

### Added

- Dedicated feedback workflow for direct source review, DOCX comments and
  Track Changes, external feedback curation and annotated PDF review.
- Ignored local locations for rendered and annotated review artifacts.
- `RETROSPECTIVE_PROMPT.md` for evidence-based documentation-collaboration
  review and controlled template-learning candidates.
- `HARMONIZATION_PROMPT.md` for source-template comparison, documentation
  consistency review and roadmap alignment.
- `CONTINUATION_PROMPT.md` for reproducible documentation-project re-entry in a
  new context window or assistant session.
- Documentation Collaboration Model v0.3.0 with formal working-commit rhythm,
  structured initialization completion and numbered maintainer collaboration.
- Git history control-word guidance for English and German maintainer instructions.
- AI Collaboration Notes to the English and German READMEs.
- AGIT Templateverse sections to the English and German READMEs.
- Shared `decisions/` Decision Record location with DDR, PDR and ADR templates.
- Setup guidance requiring derived documentation projects to preserve a visible AI Collaboration Note linked to `ChatGPT.md`.
- Concrete AI Collaboration Note wording describing documented documentation practices, AI-assisted workflows, QA discipline and repository conventions.

### Changed

- Define maintained repository sources as authoritative over DOCX and PDF
  review artifacts and require explicit review scope for website exports.
- Make feedback-channel and review-artifact decisions part of structured
  project initialization and continuation.
- Retain initialization artifacts as project provenance and record template
  lineage, lifecycle status and harmonization baselines in `PROJECT_CONTEXT.md`.
- Expand `PROJECT_CONTEXT.md` with current-work, relevant-document and
  next-session fields needed for reliable continuation.
- Separate assistant access, Git versioning and publication approval for raw
  sources, reviewed derivatives and generated documentation.
- Extend disclosure review to rendered and embedded output surfaces and define
  automated checks as warnings rather than safety approval.
- Add a standard checkpoint handoff and maintainer approval gate for external
  review feedback.
- Require human-readable executable Quarto chunks when a project uses them.
- Require consistent commit summaries and meaningful descriptions while
  reserving milestone commits for separate reviewed closure.
- Strengthen safeguards against adding sensitive raw documentation sources to
  Git.

## [v0.2.0] - 2026-07-04

### Added

- Quarto as the preferred internal documentation format with a dedicated `docs/` source directory.
- Quarto CLI installation guidance and official setup link.
- Maintainer setup guidance for Codex-based documentation projects.
- Explicit TinyTeX/TeX guidance for PDF rendering.
- Quarto render scope limited to `docs/**/*.qmd` by default.
- Minimal Quarto website configuration and bilingual starter pages.
- Documentation type profile model with an initial tutorial profile.
- Start-goal framing for tutorials and instructions.
- Bilingual documentation guidance.
- Default convention for parallel German and English Quarto files.

### Changed

- Strengthened audience-first setup and tutorial-specific QA guidance.
- Updated the AGIT Documentation Collaboration Model to v0.2.0.

## [v0.1.0] - 2026-07-04

### Added

- Initial AGIT Documentation Template structure.
- Versioned AI collaboration model for technical documentation.
- Project initialization prompt and setup workflow.
- Documentation-specific setup, process, audience, style, screenshot, link, and visual QA guidance.
- Documentation Decision Record model.
- Repository model and documentation architecture guidance.
