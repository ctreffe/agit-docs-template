# Continuation Prompt

Use this prompt as the first instruction in a new context window or assistant
session after a documentation project has already been initialized.

When the assistant can access the repository, the maintainer may invoke it with
`Read and execute CONTINUATION_PROMPT.md.` Otherwise, copy the prompt block into
the new context window.

## Prompt

```text
We are continuing an existing technical documentation project in a new context
window.

Do not repeat project initialization and do not rely on earlier chat history.
Reconstruct the maintained documentation state before drafting or revising.

Read the repository in this order:

1. Read CODEX.md and ChatGPT.md for authority, sensitivity, collaboration and
   Git rules.
2. Read PROJECT_CONTEXT.md as the current-state and handoff document.
3. Read README.md, VERSION and the current sections of CHANGELOG.md.
4. Read DOCS_SETUP.md, DOCUMENTATION_PROCESS.md, FEEDBACK_WORKFLOW.md,
   AUDIENCE.md and STYLE_GUIDE.md for the current documentation model.
5. Read the relevant documentation type profile, Quarto rules, screenshot,
   link and visual-QA guidance for the active milestone.
6. Subject to the sensitivity rules below, read the active maintained files in
   docs/ and relevant Decision Records. Treat generated HTML or PDF as review
   output, not as the source of truth. Do not repeat PROJECT_SETUP.md or
   INITIAL_PROMPT.md unless setup is incomplete or relevant to the requested
   work.

Use read-only Git commands to inspect the branch, working tree, recent commits,
latest relevant tag and all staged or unstaged changes. Compare the repository
state with PROJECT_CONTEXT.md and report stale roadmap, audience, language,
render or QA information. Preserve uncommitted work.

Before inspecting screenshots, logs, exports, tickets, internal URLs,
configuration values, operational data, feedback or generated output, apply the
documented sensitivity rules. Assistant access, Git versioning and publication
remain separate decisions. External reviewer comments are review input until
the maintainer accepts, rejects or qualifies them.

Do not ask me to repeat information already documented consistently. Before
substantive edits, provide a concise numbered re-entry report containing:

1. documentation identity, type, audience and authoritative language
2. current version, branch and working-tree status
3. active milestone, active maintained source and latest completed step
4. latest Quarto render, link, screenshot, visual-QA and feedback-review state
5. source, sensitivity, versioning and publication boundaries
6. open DDRs or other decisions, feedback, risks and inconsistencies
7. the smallest useful next documentation step and its QA path
8. only blocking maintainer questions

If my continuation instruction also contains a concrete safe task, proceed
after reconstruction; otherwise wait for confirmation of the next step.

Do not perform Git history actions unless I instruct you to perform the
specific action with a recognized control word: `explicit`, `explicitly` or the
German word family `explizit`.
```
