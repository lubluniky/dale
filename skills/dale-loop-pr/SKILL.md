---
name: dale-loop-pr
description: Monitor or repair one existing pull request using current review and CI evidence. Use for PR babysitting, scoped fixes, or carrying a PR to merge-ready state.
---

# Dale Loop PR

Resolve the exact PR, current head, repository instructions, checks, review
findings, scope, and mergeability. Record artifact identity and current blockers.

Use a read-only subagent for independent review when it adds meaningful coverage;
inherit model settings and supply the requirement, diff, and evidence. Do not
prime its verdict or allow further delegation. The coordinator or one scoped
worker repairs valid findings and PR-caused failures. Create separate Codex
tasks only when explicitly requested.

Preserve unrelated changes. Commit and push only within the user's publication
authority; do not treat a monitoring-only request as permission to repair.
After a changed head, refresh GitHub state and re-review affected risks. Retain
valid evidence for unchanged behavior only after confirming the dependency scope.

Declare merge-ready only when required checks pass, review has no unresolved
actionable findings or active change requests, scope is correct, and the PR is
mergeable. Merge only when requested. Change approach after repeated unchanged
failure; report concrete blockers without treating silence as approval.

Use an automation for requested later checks. Persist head, findings, actions,
and terminal condition; re-observe on wake and stay quiet while unchanged.
Do not assume workers remain alive between wakeups.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
