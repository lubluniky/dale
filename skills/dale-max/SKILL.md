---
name: dale-max
description: Run consequential work through implementation, independent review, evidence-based acceptance, and focused revision. Use only for explicit $dale-max or a direct request to run Dale Max.
---

# Dale Max

Use a high-assurance review loop for explicitly requested consequential work.
The calling agent owns the plan, integration, and final gate. Use subagents for
independent implementation or review; separate Codex tasks are optional only
when the user explicitly requests them.

## Establish the acceptance contract

Define the outcome, authority, criteria, exact target, direct evidence, and
material failure modes. Respect user-specified resource limits. Do not impose
unlimited review or a fixed number of reviewers. Read
[contracts.md](references/contracts.md) for worker and reviewer contracts.
Default to inherited model and effort; read
[model-routing.md](references/model-routing.md) only for an explicit routing choice.

## Implement and review

The coordinator may implement directly or assign a bounded worker with exclusive
write scope. Use live collaboration tools and capacity. Workers do not spawn
more agents or separate tasks. Keep overlapping writes sequential and preserve
unrelated changes. Reuse the implementer for focused revisions.

Run a fresh independent reviewer against the original requirement, raw artifact,
and evidence, without the implementer's intended verdict. Delegate distinct
review questions only when each covers a material failure mode that could change
acceptance. A separate preflight review is useful for costly or hard-to-reverse
plans; do not require it for every cycle. The coordinator performs complementary
work while review runs.

If independent review is unavailable, continue implementation and direct checks
that remain useful, but report the Max independence gate as unavailable. Do not
claim a same-agent review is independent or issue final PASS without the gate.

## Accept or revise

Resolve findings by direct evidence, target identity, freshness, and coverage.
Keep a compact criterion-to-evidence record. Integrate accepted changes and run
required checks plus sufficient behavioral validation in the destination.
An isolated worker's success does not prove delivery.

Use these internal outcomes:

- PASS: material criteria have direct evidence and independent review is complete.
- REVISE: a concrete bounded correction could satisfy failed criteria.
- REJECT: the approach cannot credibly satisfy the outcome.
- BLOCKED: required input, authority, independence, or evidence is inaccessible.

On revision, send failed criteria and supporting evidence to the owning worker.
Recheck affected risks; reuse still-valid evidence for unchanged artifacts.
A fresh reviewer is warranted when independence or changed failure modes require
it, not merely because a cycle counter advanced. If two revisions fail to move
the same primary signal, re-plan instead of repeating them.

Stop after acceptance, a rejected approach with no credible alternative, a real
blocker, a user limit, or interruption. Additional review needs a named uncovered
risk; passing required checks is not an invitation to broaden tests indefinitely.
Ask for new authority only when needed; existing authorization persists.

Report the result, decisive evidence, unresolved risks, and any unmet gate.
Keep detailed cycle and agent accounting for a requested audit, not every reply.
The legacy image in `assets/` illustrates an older thread topology and is not
an execution requirement.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
