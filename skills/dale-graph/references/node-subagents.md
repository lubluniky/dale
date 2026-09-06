# Subagent execution contract

The calling agent is the single scheduler and integrator. Delegation is useful
for independent evidence surfaces, disjoint implementation scopes, or a fresh
attempt to falsify a consequential claim. A sequential bottleneck stays local.
Use the live collaboration tools and capacity rather than assuming a fixed count.

## Dispatch

Give each agent this minimal contract, filled from the current work:

```text
Outcome: <one observable result>
Inputs: <necessary context and raw artifacts>
Read scope: <relevant sources>
Write scope: <exclusive paths or none>
Constraints: <user authority and applicable repository instructions>
Evidence: <how the result will be checked>
Stop: <complete, disproven, or concrete blocker>
Return the artifact, evidence, changed files, and material uncertainty.
Do not create agents or Codex tasks. Report necessary work outside your scope.
```

Share only needed context. Use fresh context for independent reviewers; include
the original intent and relevant facts, but not the expected verdict. Inherit
model and reasoning settings unless the user selected another route or an
explicit economy profile applies. Follow live context-fork and override rules.

Workers do not expand permissions. Overlapping paths, database rows, services,
Git operations, or other shared mutations must be serialized. Worktree isolation
must be created explicitly; spawning an agent does not provide it.

## Coordinate

Continue complementary work while agents run. Do not dispatch an agent and
then perform its assigned investigation yourself. Inspect its evidence when
integrating; that verification is distinct from duplicating the work.

Use messages to steer running agents, follow-up tasks for idle workers, and
bounded waits when no useful work is ready. Keep the user informed of meaningful
changes. Track agent IDs, ownership, dependencies, and accepted artifacts.
On cancellation or revoked scope, interrupt affected workers immediately and
invalidate pending outputs. On a correction, stop conflicting work before
sending revised instructions; preserve existing changes and reject stale results.

Default to one delegation level. Nested delegation requires a concrete benefit,
explicit coordinator assignment, and available runtime capacity; it must not
create a second scheduler for the same work. The default worker contract above
keeps nesting disabled.

Before completion, ensure workers have finished or been interrupted, inspect
the integrated diff, and validate the requested outcome. Claims are accepted
by directness, freshness, and coverage of evidence, not by votes or agent count.
