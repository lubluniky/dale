---
name: dale-loop
description: Design and run a repeatable agent workflow with observation, bounded action, verification, and resumable state. Use for $dale-loop or requests to keep watching or working toward a defined outcome.
---

# Dale Loop

Use `observe -> decide -> act -> verify -> persist -> wait or stop`.
Choose the smallest loop that fits the work; do not force a PR pipeline.

## Define the contract

Infer the outcome, observation source, trigger or cadence, allowed actions,
direct verifier, durable state, user resource limits, and terminal condition.
Ask only for missing information that changes the outcome or authority. Keep
existing user authorization; a skill invocation does not authorize unrelated
publication, merging, deployment, or messages.

Choose a focused mode when useful:

- `$dale-loop-project`: several independently deliverable PRs.
- `$dale-loop-pr`: one existing PR through review or repair.
- `$dale-loop-repo`: recurring repository maintenance.
- `$dale-loop-watch`: meaningful-change monitoring.
- `$dale-loop-goal`: one sustained objective.

## Execute and resume

During an active run, use subagents for independently useful work and inherited
model settings. Give each a concrete output, exclusive write scope or read-only
scope, verifier, and no further delegation. Keep overlapping mutations sequential.
Do complementary work while workers run. Separate user-owned Codex tasks require
an explicit request for separate tasks; they are not the default work unit.

For future wakeups, use the product's automation mechanism. Persist source and
artifact identities, completed actions, failed signals, and the next condition
in the automation prompt or an authorized durable artifact. Do not assume a
subagent or its conversation survives a wakeup. Re-observe before resuming and
avoid duplicate actions against unchanged state.

Use a goal mechanism only for an explicitly requested goal, within its live
schema; do not fabricate a token budget. Cadence belongs to automations, not a
blocking shell sleep. Stay quiet on unchanged or non-actionable wakes unless the
user requested periodic reports. Notify on meaningful change or required action.

Verify against the actual source, checkout, PR head, or runtime. Agent completion
text alone is insufficient. After repeated unchanged failure, change approach;
stop at a real blocker, terminal condition, or user limit. Disable completed
scheduled work through the supported automation tool; archive the user task
only when requested.

Report meaningful actions, direct evidence, remaining blockers, and the next
scheduled condition. Keep internal scheduling detail out of ordinary updates.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
