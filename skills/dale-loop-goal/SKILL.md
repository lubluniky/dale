---
name: dale-loop-goal
description: Keep one requested goal progressing until an observable completion condition is satisfied. Use for a sustained objective that does not require multiple PRs or a changing project graph.
---

# Dale Loop Goal

Keep one objective coherent across work and resumptions. State the completion
predicate and current evidence, then take the smallest useful next action.
Use subagents only when independent work emerges; inherit model settings and
keep a single coordinator. Do not turn sequential work into a swarm.

Use the goal tool only when a goal was explicitly requested. Follow its live
status and blocking rules; set a token budget only if the user supplied one.
For a requested later wakeup, use an automation instead of a blocking sleep.
Persist enough state to re-observe the actual target before the next action.

Continue through authorized work. Ask for missing authority or a consequential
choice only when needed and finish unaffected work meanwhile. When the same
failure repeats without new evidence, change approach rather than retry harder.
Honor user limits and the goal tool's exact completion/blocking semantics.

Finish with the outcome, direct evidence, and any actual unmet condition.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
