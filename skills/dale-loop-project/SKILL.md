---
name: dale-loop-project
description: Carry an engineering project through independently reviewable changes and PRs. Use when a requested project needs multiple PRs or explicit end-to-end delivery through merge.
---

# Dale Loop Project

Split by independently deliverable outcome. Group coupled small changes and
record real dependencies, ownership, branch/PR identity, and acceptance checks.

Use subagents for independent work within the current task, inheriting model
settings. Assign one writer per scope and explicitly isolate concurrent changes
in worktrees where needed; agents share a checkout by default. The coordinator
owns integration. Create separate Codex tasks only when the user requests them.

Before publication, identify whether the user authorized commit, push, PR
creation, merge, and branch deletion. Carry out already authorized delivery
without asking again. Prepare reviewable work before asking for any missing
publication authority; do not infer merge or branch deletion from a generic
request to build a feature.

Validate each candidate against requirements and the current diff. Use an
independent reviewer for material risks, supplying raw artifacts and criteria.
Track findings by PR head; changed code invalidates affected review evidence.
Reconcile checks, unresolved reviews, scope, and mergeability with live GitHub.
Repair valid findings within scope; change approach after repeated failures.

When merge is authorized and required checks and review pass, merge in dependency
order using the requested or repository-supported method. Refresh dependent
branches and validate affected integration. Delete branches only if authorized.
Use automations for requested future follow-up, with durable state and quiet
unchanged wakes. Do not assume subagents persist across wakeups.

Report delivered changes, PRs, decisive checks, and any remaining delivery gate.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
