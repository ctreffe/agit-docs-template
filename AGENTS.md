# AGENTS.md

This is the resident contract. Load routed context only when needed.

## Safety

- Inspect repository, branch, worktree and staged state. Preserve existing
  changes and selections.
- Maintainers own intent, information architecture, technical truth and
  publication decisions. Maintained sources outrank generated review files.
- Read-only checks and authorized in-scope edits are allowed. Commits, tags,
  pushes, pulls, merges, rebases, resets, reverts, branch or stash actions,
  destructive restores, publication and direct `.git/` changes require a
  specific instruction using `explicit`, `explicitly` or the German word family
  `explizit`. Authorize every action separately.
- Ask before sensitive sources, installation, privilege, outside writes or data
  transmission. Access, versioning and publication are separate.
- `input/intake/` never grants access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; temporary content is
  never versionable. Never inspect `temp/restricted/`. Synchronization grants
  no access.

## Routing

- For bounded work use `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
  `PROJECT_CONTEXT.md` only for project-wide state or unclear scope.
- Read `COLLABORATION.md` for initialization, full review, authority conflicts
  or collaboration-model changes. Load setup, documentation-process, audience,
  style, links, screenshots, Quarto, feedback and visual-QA guidance as needed.
- Task entry, handoff, ordinary commits, Decision Records and established
  rendering route automatically. Invoke initialization, review, template sync,
  consistency, retrospective, revision, local creation and `commit-milestone`
  explicitly.

## Validation

Review diffs and run `git diff --check`; add link, bilingual, render
and disclosure checks. Visual QA is required only for milestone closure or an
explicit request and must inspect rendered output. Report limits; a successful
render alone does not establish correctness or publication readiness.
