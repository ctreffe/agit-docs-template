# Documentation Process

The documentation process is iterative. Each iteration should leave the repository more accurate, structured, and reviewable.

## 1. Setup

Clarify documentation type profile, purpose, audience, language model, Quarto model, source material, sensitivity constraints, visuals, links, output formats, and review expectations.

Setup is complete only when repository identity, maintainer-owned purpose,
scope, audience, initial roadmap, source and versioning rules, publication
model, QA expectations, decision-record needs and retained template files are
recorded consistently. Do not begin large-scale drafting while required setup
decisions remain `TBD`.

## 2. Structure

Define the documentation structure before large-scale drafting. For tutorials, define the starting point, goal, prerequisites, expected result, and verification path before writing the full procedure. The procedure should be understood as the path from the starting point to the goal. The assistant may propose options and identify gaps, but the maintainer owns the structure.

A useful structure should make reader tasks visible, separate current truth from history, and keep reference material easy to find.

## 3. Sources and links

Collect source material deliberately. Do not import sensitive material into the collaboration context unless the maintainer has approved it.

Use descriptive internal and external links. Keep references stable and check links before milestones.

## 4. Drafting

Draft in small increments. Prefer clear, task-oriented sections over long undifferentiated prose.

Use active voice where appropriate. State prerequisites, steps, outcomes, limitations, and verification points explicitly.

## 5. Screenshots and visuals

Use screenshots and diagrams when they clarify real interfaces, states, workflows, or decisions. Review visuals for currency, readability, relevance, and sensitive information.

## 6. Feedback and revision

Use `FEEDBACK_WORKFLOW.md` for direct source review, DOCX comments and Track
Changes, external feedback curation and annotated PDF review. Maintained source
files remain authoritative.

For website documentation, define the reviewed page, chapter, bundle or
snapshot explicitly. Present unresolved external feedback as concise numbered
issues before incorporation. Transfer accepted changes to the source, then
re-render and validate the affected output.

## 7. Quality assurance

Before milestone closure, check:

- Technical correctness.
- Audience fit.
- Structure and navigation.
- Link integrity.
- Quarto render status for required output formats.
- Screenshot and visual quality.
- Terminology consistency.
- Open decisions and follow-up work.

## 8. Harmonization

The maintainer decides when to use `HARMONIZATION_PROMPT.md` to compare the
project with its recorded source template, reconcile internal documentation and
output state, and review roadmap and coverage fit.

## 9. Collaboration retrospective

The maintainer decides when to use `RETROSPECTIVE_PROMPT.md` to evaluate
Maintainer-Agent collaboration, including rules, feedback, decisions, handoffs
and work rhythm. Project-content implications are handed to a later
harmonization; reusable collaboration lessons may become template candidates.

## 10. Milestone closure

Build the milestone through small `docs:`, `fix:` or other appropriate regular
commits as reviewable steps become complete. Update `CHANGELOG.md`, `VERSION`,
project context and relevant decision records only when closing the milestone.
Use a separate descriptive milestone commit summary that includes the completed
version number and provide a description matching the closure diff.

At each meaningful checkpoint, hand off the content ready for review, QA
performed, source or disclosure limitations, maintainer decisions, proposed
next step and commit metadata when the step is ready.
