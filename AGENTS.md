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
- Retry once if plausibly transient. On recurrence or setup/policy error, pause;
  use `troubleshoot-environment`; authorize, repair, verify and resume.
- `input/intake/` grants no access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; never version temporary
  content or inspect `temp/restricted/`. Synchronization grants no access.

## Routing

- Bounded work uses `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
  `PROJECT_CONTEXT.md` only for project-wide state or unclear scope.
- Read `COLLABORATION.md` for initialization, full review, authority conflicts
  or collaboration-model changes. Load setup, documentation-process, audience,
  style, links, screenshots, Quarto and feedback guidance as needed.
- Task entry, handoff, ordinary commits and Decision Records route
  automatically. Rendering routes only when an artifact is requested or
  supplies necessary evidence. Invoke initialization, document addition,
  visual inspection, review, sync, consistency, retrospective, revision, local
  creation and `commit-milestone` explicitly.

## Validation

Scale evidence by stage: a bounded source change needs the smallest useful
review, an ordinary commit needs targeted evidence for a good reviewable state,
and a milestone owns comprehensive link, bilingual, render and disclosure
checks. Whitespace and all-format rendering are not defaults before the
milestone unless affected or required by a stated risk. Only explicit
`$visual-inspection` inspects selected current renders. Report limits; rendering
alone establishes neither correctness nor publication readiness.
