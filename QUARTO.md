# Quarto Documentation Format

AGIT documentation projects use Quarto Markdown (`.qmd`) as the preferred internal documentation format unless a project-specific reason argues against it.

Quarto is useful for technical documentation because it combines readable Markdown sources with structured metadata, cross-references, executable code support when needed, and multiple output formats such as HTML, PDF, DOCX, RevealJS slides, websites, and books.

## Installation

Install the Quarto CLI before rendering Quarto projects. Use the official Quarto download and setup page:

- <https://quarto.org/docs/get-started/>

After installation, open a new terminal and verify that Quarto is available:

```powershell
quarto --version
```

On Windows, if Quarto is installed but not yet visible in the current terminal session, close and reopen the terminal. If needed, verify the default installation path:

```powershell
& 'C:\Program Files\Quarto\bin\quarto.exe' --version
```

PDF rendering requires a TeX toolchain in addition to the Quarto CLI. HTML rendering works without TeX, but `quarto render --to pdf` will fail until TeX is available. Quarto can install TinyTeX when needed:

```powershell
quarto install tinytex
```

## Standard structure

This template uses a dedicated `docs/` directory for maintained Quarto source files.

```text
_quarto.yml
docs/
  index.qmd
  index.de.qmd
assets/
  screenshots/
  figures/
```

`_quarto.yml` defines project-level rendering and navigation. `docs/` contains maintained documentation sources. `assets/` contains maintained screenshots, figures, and diagrams that are safe to version.

The default render scope is limited to Quarto source files in `docs/`:

```yaml
project:
  render:
    - docs/**/*.qmd
```

This prevents repository governance files such as `README.md`, `ChatGPT.md`, or `PROJECT_CONTEXT.md` from being rendered as website pages by default.

## Executable source readability

When a documentation project uses executable Quarto chunks, write the QMD for
a human source reader. Give every substantive chunk a unique descriptive label,
keep one coherent reviewable purpose per chunk and place explanatory prose
immediately above it. The prose should state why the chunk exists, what it uses
and what result the reader should expect. Split overloaded chunks, but do not
fragment a short coherent operation into trivial pieces.

## Default outputs

HTML is the default practical output for most technical documentation projects and is the default format in this template.

PDF is supported when a printable or archival output is needed, but it requires a local TeX toolchain such as TinyTeX. Derived projects should enable PDF output in `_quarto.yml` only when PDF rendering is required and the toolchain is available. If PDF is part of milestone QA, verify TinyTeX or another TeX distribution during project setup.

Other Quarto outputs may be used if the project requires them, but they should be documented in `DOCS_SETUP.md` and tested before milestone closure.

## DOCX and PDF review outputs

DOCX may be generated as a bounded review format for wording, structure,
terminology, comments and Track Changes. It is not the default website output
and must not silently broaden the reviewed scope. A derived project should
define and validate a project-specific render command or profile for the named
page, chapter, selected bundle or snapshot before relying on DOCX review.

PDF is preferred when review depends on layout, pagination, tables, figures,
captions or print behavior. PDF annotations are less reliably mapped back to
editable source structure, so uncertain findings require explicit source
mapping and maintainer confirmation.

In both cases, Quarto files and other maintained repository sources remain
authoritative. Follow `FEEDBACK_WORKFLOW.md` when rendering, receiving,
interpreting and closing feedback artifacts.

## Bilingual documentation

The template starts with parallel English and German entry points:

- `docs/index.qmd`
- `docs/index.de.qmd`

The default convention is to maintain German and English as parallel files. The English file uses the base name, for example `index.qmd`; the German file adds `.de`, for example `index.de.qmd`.

A concrete project must decide whether one language is authoritative and how terminology, screenshots, links, and structure are kept aligned. If the project uses a different bilingual structure, document that decision in `PROJECT_CONTEXT.md` and consider recording a DDR.

## Screenshots and assets

Maintained screenshots and figures belong in `assets/screenshots/` and `assets/figures/` unless the project defines a different structure.

Raw, unreviewed, or sensitive captures should not be stored there. Use a local ignored location such as `screenshots/raw/` or `captures/raw/` until the material is reviewed and sanitized.

## Rendering

Before a documentation milestone, run Quarto rendering when the toolchain is available:

```powershell
quarto render
```

To render a specific format:

```powershell
quarto render --to html
quarto render --to pdf
```

If PDF output is required, confirm that the local PDF toolchain is available. If rendering cannot be performed, document the reason in the final work summary or milestone notes.

## QA expectations

Quarto output should be checked for:

- Successful render.
- Correct navigation.
- Working internal links and cross-references.
- Correct external links, where feasible.
- Correct rendering of callouts, tables, code blocks, figures, and screenshots.
- No sensitive information in rendered output.
- No unintended disclosure through hover text, embedded resources or file
  metadata.
- Consistency between English and German outputs when both are maintained.

## Project exceptions

A project may choose a different internal format, but that decision should be explicit in `PROJECT_CONTEXT.md` and, if consequential, recorded as a DDR.
