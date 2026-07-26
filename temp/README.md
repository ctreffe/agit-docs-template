# Temporary Working Files

`temp/` contains disposable intermediate documentation files. All contents
outside `restricted/` are assistant-readable. Everything under `temp/` is
local-only, ignored by Git and must never be versioned.

Use `restricted/` for temporary files that assistants must not enumerate or
read. Temporary files are not cataloged. Move a durable file to `materials/`
and catalog it before any later promotion to maintained documentation.
