---
name: dale-graph
description: Decompose complex work into an adaptive graph of owned outcomes and evidence, using subagents by default. Use for $dale-graph, a requested task graph, or work with independent implementation or proof boundaries.
---

# Dale Graph

Derive the graph from the requested outcome, dependencies, and write ownership.
Keep the calling agent responsible for integration and delivery. Small or
inseparable work stays local; do not manufacture agents to justify the skill.

## Choose execution

Delegate a bounded work unit when it can progress independently and saves time
or provides a materially independent check. Use collaboration subagents by
default, within the live capacity. While they run, do useful complementary work;
do not repeat their investigation. Read [node-subagents.md](references/node-subagents.md)
before delegating, and [model-routing.md](references/model-routing.md) only when
choosing an explicit model or economy profile. Default to inherited settings.

Use separate Codex tasks only when the user explicitly requests separate tasks,
forks, or a durable handoff. Requesting a graph or selecting this skill alone
selects subagent execution. Read [thread-execution.md](references/thread-execution.md)
only for the explicitly requested task mode. Do not require saved-project
registration for local subagent work.

If delegation is unavailable, complete safe sequential work and disclose the
lack of independent review. Block only the acceptance criterion that actually
requires unavailable independence, authority, or evidence.

## Derive and run the graph

1. Identify the observable outcome, acceptance criteria, current authority,
   existing user changes, and direct evidence needed for completion.
2. Create work units for independently useful artifacts or proof obligations.
   Add edges only for an input, decision, or conflicting mutation target.
3. Merge tightly coupled units. Assign exclusive write scopes; serialize any
   overlapping files or shared mutable resources. Subagents share the checkout
   unless explicit isolation has been established.
4. Show a short description of ready work and why it is split. Keep speculative
   downstream work provisional. This is an update, not an approval checkpoint.
5. Dispatch ready units with concrete inputs, deliverables, scope, and evidence.
   The coordinator also owns useful work. Reuse a worker for focused revisions.
6. Re-evaluate as results arrive: unlock dependencies, remove redundant work,
   and add newly necessary work. Compare each addition with doing it directly.
7. Inspect raw evidence, resolve contradictions, integrate accepted artifacts,
   and verify the final result in the destination checkout or requested system.

For complex dependency or evidence disputes, read
[graph-synthesis.md](references/graph-synthesis.md). Keep the graph lightweight
for ordinary work; do not print a full scheduler ledger on every update.

## Evidence and stopping

Independent review is useful when a concrete failure mode could invalidate the
result. Give the reviewer the original requirement and raw artifact, without
the maker's desired verdict. A separate model is not itself proof.

Run relevant required checks and the narrowest sufficient behavioral validation.
Broaden or repeat only after a change, failure, or unresolved coupling justifies
it. Worker-local green checks do not establish the integrated outcome.

Honor authorization already supplied by the user. Ask only for missing input or
new authority that changes the outcome; continue unaffected work meanwhile.
If two revisions do not move the same primary signal, change the approach.
Stop when criteria are satisfied or a concrete blocker prevents further progress.

Report the delivered result, direct evidence, and remaining limitations. Include
orchestration detail only when requested or needed to explain a failure.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
