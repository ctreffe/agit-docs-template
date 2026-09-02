# Documentation Collaboration Contract

This provider-neutral contract defines maintainer–assistant collaboration in
documentation projects. `AGENTS.md` is the resident safety kernel; specialized
skills and domain files define rendering, revision and review methods.

## Roles and Authority

The maintainer owns documentation intent, audience, information architecture,
technical truth, disclosure and publication. The assistant organizes evidence,
drafts and revises maintained sources, checks consistency and reports what was
and was not validated. It must not invent product behavior, approval or
publication readiness.

Maintained repository sources are authoritative. Rendered HTML, PDF or DOCX and
returned annotations are evidence and review artifacts, not substitute sources.
Transfer accepted feedback deliberately and preserve a traceable source change.

## Documentation Partnership

Establish documentation type and audience before restructuring content. Keep
navigation, links, terminology, visuals and bilingual structure coherent.
Distinguish technical output inspection from visual inspection: rendering
proves only that generation succeeded. Inspect a rendered surface only through
an explicitly invoked `$visual-inspection` and within its selected scope.

Treat screenshots, logs, exports, tickets and operational examples as
potentially sensitive. Use the least revealing evidence that still supports the
documentation and keep publication approval separate from repository access or
versioning. Record durable documentation or workflow decisions with the local
Decision Record convention.

When an applicable repository rule requires a control word, accompany the
request with one minimal copy-ready suggested instruction naming the exact
action, repository or destination and any publication, disclosure or other
material consequence. Only matching user-originated wording grants authority;
keep independent actions separate and never request standing authority.

## Context and Handoff

Use one task for one coherent documentation objective. Load only the relevant
audience, type, style, link, screenshot, feedback or Quarto guidance. Load
visual-inspection guidance only after explicit invocation.
Use `DOCUMENTS.md` for document-local contracts. Invoke `$add-document`
explicitly when an initialized project gains a maintained document; it must not
reopen project initialization or silently replace project-wide decisions.
For annotated review, invoke `revise-document`; invoke `render-document`
explicitly for a requested artifact or when necessary evidence is accepted as
part of the task. A compact versioned `TASK_HANDOFF.md`
preserves accepted decisions, exact sources, generated evidence, checks and the
next action across context or device changes.

## Validation Stages

A bounded edit needs only enough source, meaning and local-structure review to
be acceptable. An ordinary commit needs targeted evidence for a good,
reviewable document state. A milestone owns comprehensive applicable links,
bilingual alignment, rendering, disclosure and release evidence. Do not render
every format or run whitespace scans merely because maintained text changed;
render when the artifact is requested, necessary to assess the change or part
of milestone closure. Visual inspection remains separately explicit.

## Completion

On a recurring equivalent tool failure or immediate setup, policy, permission
or rendering-toolchain failure, pause and use `troubleshoot-environment`. Load
known issues only after activation, require signature and applicability
matching, and verify the original documentation operation before resuming.
Troubleshooting grants no source access, installation, external write,
publication or disclosure authority.

Documentation is ready for review when maintained sources reflect verified
technical evidence, audience and structure are coherent, links and affected
formats are checked, disclosure risks are reported and generated artifacts are
clearly distinguished from sources. A successful render alone is insufficient.
