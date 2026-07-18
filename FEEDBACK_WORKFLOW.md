# Feedback Workflow

This workflow defines how maintainer and external review feedback is transferred
back into a documentation project without weakening source control, traceability
or maintainer authority.

## Source of truth

Maintained repository sources, normally Quarto files in `docs/`, remain
authoritative. Rendered DOCX and PDF files are review artifacts. Comments,
tracked changes and annotations are not complete until the accepted change has
been applied to the maintained source and validated there.

For website projects, every review artifact must have an explicit scope. Use a
single page, chapter, selected bundle or named snapshot; do not treat an
ambiguous DOCX export as a review of the whole website.

## Feedback channels

### Direct source review

The maintainer may edit or comment on the maintained source directly. This is
the shortest path when no rendered context is needed. Ambiguous or
consequential comments still require clarification.

In Quarto or Markdown source, use a non-rendered comment such as:

```markdown
<!-- Maintainer: Clarify which permissions are required before this step. -->
```

Clear maintainer comments may be implemented directly. Remove resolved
comments after their intent has been incorporated, unless they preserve durable
rationale that belongs in the maintained text or a DDR.

### Maintainer DOCX review

Use DOCX comments and Track Changes primarily for wording, structure,
terminology and local content flow. A maintainer-authored change may be
transferred directly when its intent and source location are unambiguous.

The assistant may inspect a supplied annotated DOCX only after assistant access
has been approved. It should reconcile comments and tracked changes with the
current source rather than replacing the source file with the reviewed export.

### External DOCX review

External comments and tracked changes are review input, not automatic
instructions. The maintainer may curate them in the reviewed document with a
comment beginning `Maintainer:`. Such a comment records the maintainer's
instruction or qualification; the underlying external proposal alone does not.

Uncurated external feedback must be presented as concise numbered issues for
maintainer acceptance, rejection, qualification or deferral before it is
implemented.

### Annotated PDF review

Use PDF annotations primarily for layout, pagination, tables, figures,
captions, print output and other rendered presentation issues. PDF annotations
are less reliably connected to editable source structure than DOCX comments or
tracked changes. The assistant should therefore map annotations to source
locations and present uncertain or external findings as numbered issues before
editing.

Clear maintainer-authored PDF annotations may be implemented directly when the
requested source change is unambiguous. Layout observations must be checked in
the relevant rendered format after the source is changed.

## Review cycle

1. Define the review purpose, authoritative source, artifact scope and expected
   feedback channel.
2. Render or export the named review scope and record the source state or commit
   from which it was produced.
3. Store rendered and annotated review artifacts in the project-defined local
   review location. The template uses `review/rendered/` and
   `review/annotated/`, which are ignored by default.
4. Confirm separately whether the assistant may inspect the artifact, whether
   it may be versioned and whether it may be published or shared.
5. Classify feedback as clear maintainer instruction, maintainer-curated
   external feedback, unresolved external feedback or clarification required.
6. Present unresolved decisions as a concise numbered list and record the
   maintainer's accept, reject, qualify or defer decision.
7. Apply accepted changes to the maintained source in small reviewable steps.
8. Re-render and perform the relevant content, link, visual and disclosure QA.
9. Update `PROJECT_CONTEXT.md` with the active review state and next action.
   Record durable documentation or workflow decisions in a DDR when needed.

## Traceability

At minimum, keep enough context to identify:

- The reviewed source scope and source state.
- The rendered artifact and output format.
- The feedback author or review role.
- Accepted, rejected, qualified, deferred and unresolved items.
- The source changes and validation that closed the review.

A permanent review ledger is optional unless the project requires one. The
current review state belongs in `PROJECT_CONTEXT.md`; durable rationale belongs
in Decision Records or maintained documentation.

## Sensitivity and repository handling

Review artifacts may contain comments, author identities, hidden metadata,
internal URLs, screenshots, document history or unpublished content. Treat
them as potentially sensitive until reviewed.

Assistant access, Git versioning and publication are separate maintainer
decisions. The default ignored locations prevent accidental staging but do not
make an artifact safe. Version a review artifact only after a deliberate need,
sensitivity review and corresponding ignore exception have been established.
