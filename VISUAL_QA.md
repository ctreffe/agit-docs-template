# Visual QA

Visual QA means an agent-performed inspection of the actually rendered visual
surface. For HTML documentation, the assistant opens and inspects the rendered
site with the Browser skill. For PDF or DOCX, it renders and inspects page
images with the appropriate visual tool. Rendering successfully, reading HTML,
checking links or inspecting source and output structure do not count as visual
QA.

Perform this visual QA only before milestone closure or when the maintainer
explicitly requests it. A screenshot, diagram, layout or other visual change
does not by itself trigger agent visual QA; the maintainer owns visual
inspection during ordinary work. If the required visual tool or output is not
available, report that visual QA was not performed.

## Routine render and output validation

Routine validation may run `quarto render` and inspect generated HTML without
using the Browser skill. Check render success, warnings, required files, basic
HTML structure, links, referenced assets and obvious unrendered source content
as relevant. Report this as render or output validation, never as visual QA.

## Screenshots

- Screenshot is current.
- Screenshot shows the intended state.
- Important text is readable.
- Cropping does not remove necessary context.
- Sensitive information has been removed or approved.
- Filename is stable and descriptive.
- Screenshot is referenced from the relevant text.

## Diagrams

- Diagram reflects the current technical model.
- Labels are readable.
- Terminology matches the documentation.
- Diagram is not more detailed than the reader needs.
- Source or generation method is documented when relevant.

## Quarto rendered outputs

When Quarto is used, run `quarto render` before milestone closure if the local
toolchain is available. HTML is the default baseline render. PDF render checks
require a TeX toolchain such as TinyTeX. During milestone visual QA, inspect the
required generated HTML through the Browser skill and any required PDF or DOCX
through rendered page images.

## Rendered outputs

- Headings, lists, tables, code blocks, and images render correctly.
- Navigation works.
- Internal links resolve.
- External links are checked.
- Images have appropriate alt text or surrounding explanation.
- Layout works in the expected output format.

## Publication readiness

- No unintended draft notes remain.
- No sensitive visual information remains.
- Visuals support real reader tasks.
- Open visual issues are documented if they cannot be resolved before the milestone.
