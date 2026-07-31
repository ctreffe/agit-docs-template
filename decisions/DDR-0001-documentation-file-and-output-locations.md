# DDR-0001: Documentation File and Output Locations

Status: Accepted
Date: 2026-07-31

## Context

The Documentation Template previously used several overlapping locations:
maintained Quarto source under `docs/`, binary publication files under
`assets/`, retained transformed files under `materials/`, generated website
output under `_site/`, and separate rendered and annotated subdirectories below
`review/`. The overlap made it harder to tell whether a file was maintained
source, retained project material, generated output or a returned review copy.

TVDR-0012 distinguishes files by their project role rather than how they were
generated. TVDR-0014 adds synchronized external storage without prescribing a
permanent repository location for every documentation source type.

## Decision

Use these locations in the Documentation Template and derived projects unless
a documented project need requires a different model:

- maintained Quarto and Markdown source belongs in `docs/`;
- reviewed binary documentation material approved for Git belongs in
  `materials/versioned/` and remains cataloged with its provenance;
- maintained presentation source such as CSS, SCSS, templates or theme
  configuration belongs in `styles/`;
- generated HTML, PDF, DOCX and other formats belong below ignored
  `output/<format>/` directories;
- freshly generated files prepared for review remain in `output/<format>/`;
- returned files with comments, Track Changes or PDF annotations belong
  directly in ignored `review/` without a redundant status subdirectory.

Remove the parallel `assets/` tree. Keep unchanged external files in `input/`
and disposable intermediates in `temp/`. These locations do not change the
separate decisions for assistant access, Git versioning, publication or
external sharing.

## Rationale

One location per file role reduces ambiguity and makes repository inspection,
ignore rules and review handoffs easier to understand. Format-specific output
directories keep generated website trees and document formats separate, while
placing returned annotations directly in `review/` distinguishes received
feedback from newly rendered files without encoding temporary status twice.

## Consequences

- `_quarto.yml` writes the baseline website to `output/html/`.
- `output/README.md` keeps the ignored generated-output hierarchy discoverable.
- Maintained screenshots and figures no longer require a separate `assets/`
  hierarchy.
- Review workflows record scope and source state in `PROJECT_CONTEXT.md`
  rather than relying on `rendered/` and `annotated/` folder names.
- A review file that must become a durable assistant-readable foundation is
  promoted deliberately to `materials/` and cataloged.
- Existing derived projects adopt the structure deliberately; this record does
  not authorize moving or inspecting their files.

## Alternatives considered

- Keep `assets/` beside `materials/versioned/`: rejected because both could
  contain the same maintained binary documentation roles.
- Keep `_site/` and additional top-level export directories: rejected because
  one ignored `output/` hierarchy communicates generated status consistently.
- Keep `review/rendered/` and `review/annotated/`: rejected because rendered
  files already belong to `output/` and every remaining review file is a
  returned annotated copy.

## Follow-up

Keep Quarto configuration, ignore rules, feedback guidance, bilingual READMEs
and Templateverse validation aligned with this model. The record refines the
Documentation Template implementation referenced by TVDR-0014 without changing
the family-wide synchronized-storage decision.
