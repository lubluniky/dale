---
name: dale-loop-repo
description: Maintain a repository on a requested recurring cadence using bounded priorities and live evidence. Use for recurring engineering triage or repository maintenance.
---

# Dale Loop Repo

Use a product automation for the requested cadence. Record priority sources,
allowed actions, merge authority, direct checks, and terminal condition.
On each wake inspect current repository state, open work, and CI before choosing
an action. Prefer already-started or blocking work to inventing new work.

Select bounded work with observable acceptance criteria. Delegate independent
parts to subagents during the run, inheriting model settings. Give each an
exclusive scope or read-only role and forbid further delegation. Use explicit
worktree isolation for concurrent writers when necessary. Separate Codex tasks
require an explicit user request; unavailable task tools do not block local work.

Persist source/PR identities, actions, findings, and next condition so a future
wake can resume without a living worker. Prevent duplicate dispatch against
unchanged state. Verify reports against live systems and respect publication
and merge authority. Do not expand routine maintenance into unrelated product,
security, deployment, or destructive changes.

Notify only after meaningful action, failure, completion, or required input.
Remain quiet when unchanged. Disable scheduled work at its terminal condition;
archive the user task only when asked. Back off and report repeated blockers.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
