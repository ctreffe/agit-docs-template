# AGENTS.md

Resident contract.

## Safety

- Inspect repository, branch, worktree and staging; preserve changes and
  selections.
- Maintainers own intent, information architecture, technical truth and
  publication decisions. Maintained sources outrank generated review files.
- Authorized reads and edits are allowed. Commits, tags, pushes, pulls, merges,
  rebases, resets, reverts, branches, stashes, destructive restores,
  publication and direct `.git/` changes each require an instruction containing
  `explicit`, `explicitly` or German `explizit`.
- Ask before sensitive sources, installation, privilege, outside writes or
  transmission; access, versioning and publication are separate.
- After a failure, retry once only if plausibly transient. On recurrence or any
  setup/policy error, pause; diagnose, seek an authorized durable fix, verify
  it, then resume.
- `input/intake/` grants no access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; never version temporary
  content or inspect `temp/restricted/`. Synchronization grants no access.

## Routing

- Bounded work uses `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
  `PROJECT_CONTEXT.md` only for project-wide state or unclear scope.
- Read `COLLABORATION.md` for initialization, full review, authority conflicts
  or collaboration-model changes. Load setup, documentation-process, audience,
  style, links, screenshots, Quarto, feedback and visual-QA guidance as needed.
- Task entry, handoff, ordinary commits, Decision Records and established
  rendering route automatically. Invoke initialization, review, template sync,
  consistency, retrospective, revision, local creation and `commit-milestone`
  explicitly.

## Validation

Review diffs and run `git diff --check`; add link, bilingual, render and
disclosure checks. Visual QA is required for milestone closure or an
explicit request and inspects rendered output. Report limits; a successful
render alone does not establish correctness or publication readiness.
