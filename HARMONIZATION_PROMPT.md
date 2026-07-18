# Harmonization Prompt

Use this prompt for a deliberate documentation-project harmonization. It
compares a derived project with its recorded source template, checks internal
documentation consistency and reviews the documentation roadmap.

Harmonization concerns project content, not Maintainer-Agent collaboration or
lessons for the source template.

Invoke it with `Read and execute HARMONIZATION_PROMPT.md.`

## Prompt

```text
Perform a structured content harmonization of this documentation project.

The concrete documentation project, maintainer-owned documentation intent,
audience decisions and Decision Records remain authoritative. Never copy
template changes blindly.

1. Read CODEX.md and ChatGPT.md for authority, safety and Git rules.
2. Read PROJECT_CONTEXT.md, including repository role, source template,
   baselines, intentional deviations and roadmap.
3. Read README.md, current CHANGELOG.md sections, DOCUMENTATION.md,
   DOCUMENTATION_PROCESS.md, DOCS_SETUP.md, AUDIENCE.md, STYLE_GUIDE.md,
   QUARTO.md, SCREENSHOTS.md, LINKS.md, VISUAL_QA.md and relevant Decision
   Records and documentation sources.
4. Inspect branch, working tree, recent commits, relevant tags and staged or
   unstaged changes with read-only Git commands. Preserve uncommitted work.
5. Apply source-sensitivity, screenshot, internal-link, embedded-resource and
   publication rules before opening or rendering materials.

For a derived project, locate the exact source template and last recorded
harmonization baseline, then establish the latest verifiable template baseline.
Do not assume that a local template clone is current; use authoritative
read-only remote evidence when it is available and permitted. If freshness or
a baseline cannot be verified, stop the external comparison at metadata level
and ask for the missing path, version or commit. Do not compare with an
unrelated template.

Classify each material template change as adopt, adapt, reject or defer. Record
the rationale, affected files and governing Decision Records or deviations.
Project audience, documentation purpose, publication model and validated
project rules override template defaults. Present conflicts as numbered
maintainer decisions before editing. Never modify the source template during
project harmonization.

If this repository is itself a template, do not infer a parent template. Skip
the external comparison.

Check internal consistency across:

- project identity, status, version or milestone and changelog
- documentation purpose, scope, audience and type profile
- roadmap, current work, completed states and next-session guidance
- navigation, structure, terminology, links and cross-references
- screenshots, diagrams, captions, alt text and visual QA
- Quarto configuration, source files, rendered outputs and publication state
- source provenance, sensitivity, derivatives and disclosure boundaries
- Decision Records and intentional deviations
- actual validation evidence versus documented claims

Review whether the documentation roadmap still fits audience tasks, current
coverage, publication needs and remaining work. Propose project-content changes
without inventing technical facts or maintainer-owned publication decisions.

Harmonization is not a retrospective. Do not evaluate collaboration or derive
template improvements. Defer collaboration observations to a future
retrospective and do not implement template feedback.

Before edits, provide a concise numbered report:

1. repository role and project/template baselines
2. template comparison matrix with adopt/adapt/reject/defer classifications
3. documentation and repository consistency findings
4. roadmap and coverage findings
5. render, link, visual, sensitivity and publication checks required
6. proposed edit sequence
7. collaboration observations deferred to a retrospective
8. blocking maintainer decisions

Apply findings only when my instruction clearly authorizes implementation, and
only after reporting. After approved edits, run the relevant link, render and
visual checks. Update PROJECT_CONTEXT.md with the last harmonization baseline
and deviations only after the comparison and integration actually succeed.

Do not perform a Git history action unless I instruct you to perform that
specific action with a recognized control word: `explicit`, `explicitly` or the
German word family `explizit`.
```
