# AGIT Documentation Template Idea Backlog

This is the lightweight intake for reusable improvements to this source
template. It is separate from every derived-project roadmap. Capturing an idea
does not approve implementation, create a project commitment or authorize a
cross-repository change.

Derived projects do not require an `IDEAS.md` by default. Project-specific
findings belong in that project's roadmap or Decision Record process. A
retrospective running in this source-template repository may capture a
candidate under normal authorized in-scope edit rules. A derived-project
transfer may enter only with exact cross-repository control-word authorization;
otherwise it remains a `Pending Idea Transfer`.

## Status Model

- **Captured** — retained for later review; no implementation decision exists.
- **Exploring** — alternatives, evidence or constraints are being assessed.
- **Promoted** — accepted into an identified roadmap or decision process.
- **Deferred** — retained but intentionally inactive.
- **Rejected** — closed with a short rationale.

## Entry Format

```markdown
### IDEA-NNNN: Short title

- **Status:** Captured | Exploring | Promoted | Deferred | Rejected
- **Source:** Optional approved project or template evidence
- **Opportunity:** Problem or useful outcome
- **Recurrence:** Why this may matter beyond one project
- **Reusable elements:** Existing patterns or artifacts to assess
- **Benefit:** Expected value
- **Risk:** Adoption or transfer risk
- **Boundaries:** Access, domain and non-goals
- **Next decision:** Smallest maintainer-owned decision
- **References:** Optional durable evidence or promoted destination
```

## Ideas

### IDEA-0001: Multi-document projects and add-document workflow

- **Status:** Promoted
- **Source:** AGIT Windows Guides documentation-structure retrospective on
  2026-08-27, using maintainer-provided non-sensitive workflow evidence
- **Opportunity:** Treat projects derived from the Documentation Template as
  multi-document projects by design even when initialization creates only one
  initial document. Add an explicit `$add-document` skill that establishes a
  bounded scope and lifecycle for each additional maintained document without
  reinitializing the repository.
- **Recurrence:** Documentation projects commonly grow beyond their initial
  guide or report. Without a document-level setup workflow, later documents can
  inherit unsuitable project-wide assumptions or introduce inconsistent
  audience, language, output, review and navigation decisions.
- **Reusable elements:** Build on `$start-project`, `PROJECT_CONTEXT.md`,
  `DOCS_SETUP.md`, the document catalog and lifecycle model, document-type
  profiles and the existing render, revision and review skills. The setup
  contract could capture the document purpose and boundaries, maintainer-owned
  audience statement, authoritative language or bilingual relationship,
  primary and permitted output formats, source and sensitivity constraints,
  navigation placement, validation expectations, initial lifecycle status and
  next action.
- **Benefit:** Makes additional documents predictable, independently scoped and
  compatible with shared project governance while allowing a small project to
  remain a one-document project for as long as that is sufficient.
- **Risk:** A document-level setup contract could duplicate project
  initialization, create conflicting authorities or burden small additions with
  unnecessary metadata. Implicit defaults could also conceal decisions that
  belong to the maintainer.
- **Boundaries:** `$add-document` must not rerun project initialization, invent
  documentation intent, force creation of multiple documents, overwrite an
  existing document or automatically render, publish, commit or push. Project-
  wide authority remains in the established repository guidance; document-
  local scope may refine but must not silently contradict it.
- **Next decision:** Implemented in `DOCUMENTS.md` and the explicit-only
  `$add-document` skill; validate the contract in derived-project use before
  changing its required fields.
- **References:** `$start-project`, `PROJECT_SETUP.md`, `DOCS_SETUP.md`,
  `PROJECT_CONTEXT.md`, `DOCUMENTS.md`, `DOCUMENTATION_PROCESS.md` and
  `DOCUMENTATION_TYPE_PROFILES.md`.

### IDEA-0002: Explicit reusable visual-inspection skill

- **Status:** Promoted
- **Source:** AGIT Windows Guides documentation-validation retrospective on
  2026-08-27, using maintainer-provided non-sensitive workflow evidence
- **Opportunity:** Provide a reusable `$visual-inspection` skill at the
  Documentation Template level. It replaces prompt-shaped visual-QA routing
  with an explicitly invoked inspection workflow and remains separate from
  rendering and routine technical output validation.
- **Recurrence:** Derived documentation projects may need actual inspection of
  rendered HTML, PDF or DOCX surfaces, but the required document and format
  scope varies by task. Automatic milestone inspection can therefore perform
  unnecessary work or inspect formats the maintainer did not select.
- **Reusable elements:** Reuse the existing visual criteria and evidence model,
  Browser-based inspection for HTML, rendered-page image inspection for PDF or
  DOCX and the format-specific output locations established by
  `$render-document`. Retain truthful reporting of inspected pages, viewports,
  formats, findings and limitations.
- **Benefit:** Gives derived projects one consistent opt-in workflow for visual
  review while keeping format selection maintainer-owned and preventing visual
  inspection from being inferred merely from a milestone or visual change.
- **Risk:** Existing milestone and visual-QA guidance may continue to trigger
  inspection automatically unless all affected references are migrated.
  Inspection could also be mistaken for accessibility validation, technical
  correctness or publication approval.
- **Boundaries:** Configure the skill with
  `allow_implicit_invocation: false`. Run it only when the maintainer explicitly
  invokes `$visual-inspection`, and inspect only named current renders in the
  formats selected for the document. The skill must not render missing output,
  infer additional formats, change source files automatically or grant
  accessibility, disclosure or publication approval.
- **Next decision:** Implemented as the self-contained explicit-only
  `$visual-inspection` workflow; validate the contract in derived-project use
  before changing its scope fields, criteria or format methods.
- **References:** `$visual-inspection`, `$render-document`, `AGENTS.md`,
  `COLLABORATION.md` and `DOCUMENTATION_PROCESS.md`.

### IDEA-0003: Explicit-only maintained-document rendering

- **Status:** Captured
- **Source:** Maintainer-directed retrospective from the derived
  `agit-admin-guides` project on 2026-09-01, reviewing the first document-review
  and example-file revision cycle from 2026-08-28 through 2026-09-01
- **Opportunity:** Stop automatically routing every maintained QMD change
  through `render-document`. Keep the skill available, and allow the assistant
  to recommend rendering when it would provide useful evidence, but invoke it
  only after an explicit maintainer request. Ensure that `AGENTS.md`,
  `COLLABORATION.md`, `DOCUMENTATION_PROCESS.md`, `revise-document`,
  `commit-changes` and `commit-milestone` do not reintroduce an implicit nested
  render path.
- **Recurrence:** Documentation work often includes several small wording or
  metadata revisions before a maintainer wants a new review artifact. The
  current automatic established-rendering route can regenerate every configured
  format after each QMD edit even when source-level checks are sufficient.
- **Reusable elements:** Change skill routing from automatic to explicit;
  retain the current narrow-render, output-location and technical-inspection
  contract after invocation; add a concise suggestion rule based on changed
  structure, executable content, cross-references, layout-sensitive content or
  a requested review artifact; and record rendering as pending or not requested
  without implying failure. Decide how a separately explicit milestone request
  interacts with required render evidence instead of silently treating
  milestone invocation as render authorization.
- **Benefit:** Gives the maintainer direct control over artifact generation,
  reduces repeated Quarto/LaTeX execution and output carried in context, and
  supports batching several source edits into one deliberate review render.
- **Risk:** Syntax, reference or layout defects may remain undiscovered longer,
  and a maintainer may expect a current PDF when only the QMD changed. Explicit
  status reporting and clear render suggestions are needed to prevent stale
  artifacts from being mistaken for current output.
- **Boundaries:** Do not weaken source-level checks that are indispensable for
  the change, claim an old render represents current sources, perform visual
  inspection without its own trigger or treat a rendering suggestion as
  authorization. Capture does not approve immediate changes to the skill or
  template routing.
- **Next decision:** Decide the exact control words or invocation syntax for
  rendering, the suggestion criteria and milestone interaction, then review the
  affected routing and lifecycle files before implementation.
- **References:** `.agents/skills/render-document/SKILL.md`, `AGENTS.md`,
  `COLLABORATION.md`, `DOCUMENTATION_PROCESS.md`, and the derived project
  retrospective recorded through `perform-retrospective`.
