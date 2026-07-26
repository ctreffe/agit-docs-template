# External Files and Sources

Use `input/` for externally supplied documentation files such as screenshots,
exports, tickets, logs, source documents and operational material. New or
uncertain files start in `intake/`; classified files may go directly to
`restricted/`, `local/` or `versioned/`.

Keep their content unchanged. Any OCR, cropping, annotation, conversion or
other content change creates a new file governed through `materials/`.

- `intake/` contains unclassified files and is unavailable to assistants;
- `restricted/` contains ignored files unavailable to assistants;
- `local/` contains ignored files approved for assistant access within a
  documented task;
- `versioned/` contains reviewed files approved for Git and assistant access.

Use `CATALOG.md` for safe metadata about files and unchanged external services,
datasets or URLs, and ignored `CATALOG.local.md` for sensitive local details.
Resolve logical external locations through ignored `PATHS.local.md`. Assistant access, Git
versioning and publication remain separate maintainer decisions.

An approved external file may later become maintained documentation content.
For example, a reviewed screenshot may move to `assets/screenshots/`, while an
accepted source change belongs in `docs/`. Rendered or annotated review files
remain under `review/`. Record the transition in the catalog.
