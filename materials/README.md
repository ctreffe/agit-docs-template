# Project Materials

Synchronized external materials use provider-neutral `sync:` roots and storage
`external`; see [SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md).

`materials/` contains retained, assistant-readable working files created by the
documentation project or derived by changing content from external files under
`input/`. Git versioning and publication remain separate decisions.

Files under `input/` remain content-unchanged. Cropping, annotation, redaction,
OCR, conversion, optimization, combination or any other content change creates
a new material. Preserve the original input and record its ID under `Based on`
in `CATALOG.md`.

The catalog records three storage states:

- `local`: stored under `materials/local/` and ignored by Git;
- `versioned`: stored under `materials/versioned/` and approved for Git;
- `external`: stored outside the repository and represented by a stable
  logical location in the catalog.

Copy `PATHS.local.example.md` to the ignored `PATHS.local.md` for
device-specific paths. Never version credentials, private share tokens or
absolute local paths.

Examples include cropped screenshots, OCR extracts, converted reference
documents and retained review preparations. Move accepted textual content to
`docs/`; keep reviewed binary documentation material in `materials/versioned/`
after Git approval and preserve its provenance. Presentation source belongs in
`styles/`. Generated review copies and finished publication outputs belong in
the applicable format directory below `output/`; returned annotated review
files remain separate under `review/`.
