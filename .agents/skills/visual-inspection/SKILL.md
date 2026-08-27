---
name: visual-inspection
description: Inspect named current rendered HTML, PDF or DOCX documentation surfaces with format-appropriate visual tools and report exact coverage, findings and limitations. Use only when explicitly invoked; do not use for rendering, routine technical validation, accessibility certification or publication approval.
---

# Visual Inspection

Run only when the maintainer explicitly invokes `$visual-inspection`. Establish
the named document, exact current render, selected formats and intended routes,
pages and viewports. Read `DOCUMENTS.md` and only the applicable format,
screenshot and disclosure guidance. Preserve source, output and Git state.

Refuse missing, stale, ambiguous or unselected output. Do not render a missing
documentation format or infer another format from project configuration. Page
images created temporarily from an existing selected PDF or DOCX are inspection
evidence, not an additional documentation output.

- Inspect HTML through the Browser skill at the selected routes and viewports.
- Inspect selected PDF or DOCX pages as rendered page images with the
  appropriate visual tool.
- Record each finding against a route, page, viewport or visual element. Do not
  change maintained source automatically; return findings for maintainer review
  and a separately authorized correction step.

Apply the relevant visual criteria to each inspected surface:

- Headings, lists, tables, code blocks and images have the intended visual
  hierarchy without clipping, overlap or broken layout.
- Text, labels, navigation and controls are readable and usable at the selected
  viewport or page size. Do not treat this as a complete link or interaction
  check.
- Screenshots show the intended current state, retain necessary context, remain
  readable and reveal no unapproved sensitive information. Annotations clarify
  rather than obscure the interface.
- Diagrams have readable labels, consistent terminology, appropriate detail and
  no missing or cropped elements.
- No unintended draft notes or other visible release concerns remain. Visuals
  support the named reader task, and every unresolved visual issue is recorded.

Report the document and exact output paths, formats, routes or pages, viewports,
inspection method, findings, uninspected surfaces and tool or evidence limits.
Keep visual inspection distinct from render success, link checking, content or
technical correctness, accessibility validation, disclosure approval and
publication readiness.
