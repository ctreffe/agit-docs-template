---
name: add-document
description: Add one maintained document or language-linked document set to an initialized documentation project with explicit document-local scope, catalog metadata and navigation decisions. Use only when explicitly invoked; do not use for project initialization or ordinary edits to an existing document.
---

# Add Document

Confirm that this is an initialized derived documentation project, not a
source-template maintenance checkout or an uninitialized repository. Inspect
Git read-only and preserve existing work and staging.

1. Read `PROJECT_CONTEXT.md`, `DOCUMENTS.md` and only the project, audience,
   profile, Quarto, source-access and validation guidance needed for the new
   document. Treat project-level decisions as defaults, not facts to duplicate.
2. Confirm the maintainer-owned title, stable document ID and source path;
   purpose, scope and non-goals; dominant type profile; primary audience and
   reader task; language relationship and authoritative language; required and
   permitted output formats; source, access and sensitivity constraints;
   navigation placement; validation and review expectations; initial lifecycle
   status; and next action. Mark an inherited project default explicitly. Stop
   for any missing choice that would change the document's meaning or exposure.
3. Refuse an ID or path collision. Do not overwrite an existing source,
   reinitialize the project or silently contradict project-wide authority.
   Resolve conflicts with the maintainer before editing.
4. After the decisions are confirmed, add one entry to `DOCUMENTS.md`. Create
   the agreed source skeleton or language-linked source set and update
   `_quarto.yml` navigation only when those changes are part of the request.
   Update `PROJECT_CONTEXT.md` only when its catalog pointer, documentation
   structure or current-work summary would otherwise be stale.
5. Check catalog completeness, source-path uniqueness, language relationships,
   navigation references, links and YAML syntax in the narrowest useful scope.
   Report required render, review and Decision Record follow-up separately.

Do not render, publish, commit, push, inspect unapproved sources or grant
versioning or publication approval. Those actions retain their separate local
workflows and authorization requirements.
