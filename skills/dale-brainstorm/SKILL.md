---
name: dale-brainstorm
description: Think through ideas, alternatives, and tradeoffs with the user without prematurely starting implementation. Use for $dale-brainstorm or a request to brainstorm or explore a direction.
---

# Dale Brainstorm

Think with the user in the current conversation. Build on their language,
values, and constraints. Explore meaningfully different possibilities before
converging; adapt to their requested phase rather than imposing rounds.

Keep live options, criteria, assumptions, and rejected alternatives in the
conversation. Summarize when useful, not after every exchange. Ask at most one
substantive question per response when its answer changes the discussion.
State the strongest credible counterargument before endorsing a direction.
Separate evidence, inference, and preference.

## Gather evidence without taking over

Read relevant authorized sources directly when a quick check grounds the idea.
For a substantial, separable factual question, a read-only subagent may help
while the conversation continues. Give it a concrete evidence output and
minimum context; inherit model and effort and forbid further delegation.
Do not create agents merely to simulate opinions, taste, or disagreement.
Use a separate Codex task only when the user explicitly asks for one.
Read [model-routing.md](references/model-routing.md) only for requested routing.

## Converge when asked

A request to recommend, choose, summarize, or plan authorizes that phase.
A request to implement authorizes leaving brainstorming for the requested work;
do not demand a special exit phrase or repeat permission already given.
Otherwise keep this discussion from turning into file edits, tickets, external
messages, or an assumed implementation commitment.

When asked for a recommendation, give the leading direction, concrete reasons,
strongest counterargument, and material uncertainties. Provide an implementation
plan only when requested. Persist a discussion artifact only when requested.
Do not automatically hand off to another Dale workflow.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
