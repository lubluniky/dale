---
name: dale-index
description: Create or refresh evidence-backed REQ.md, CONTEXT.md, STATE.md, TDD.md, DESIGN.md, and DECISIONS.md repository primitives. Use for $dale-index, repository mapping, context recovery, or stale project documentation.
---

# Dale Index

Build a compact source of truth from the repository as it exists now. The
calling agent integrates and writes; independent discovery uses read-only
subagents where repository scope justifies parallel work.

## Bound the refresh

Inspect applicable instructions, Git state, manifests, entrypoints, tests,
schemas, and existing primitives. Preserve unrelated edits and hand-written
content unless current evidence disproves it. No saved Codex project is needed.

For an initial index, cover the repository's material boundaries. For a refresh,
use the last documented revision and actual changes to inspect affected claims
and their consumers. Include uncommitted changes. When the baseline is missing
or unreliable, broaden inspection rather than claiming incremental coverage.

## Own each fact once

| File | Owns |
|---|---|
| REQ.md | Product intent, users, scope, requirements, acceptance criteria |
| CONTEXT.md | Architecture, repository map, contracts, constraints, operations |
| STATE.md | Current work, blockers, risks, next actions |
| TDD.md | Test strategy, actual commands, quality gates, missing coverage |
| DESIGN.md | Existing visual language, components, states, accessibility |
| DECISIONS.md | Dated decisions, alternatives, evidence, consequences, status |

Use the established primitive directory even when its set is incomplete. Add
missing documents there and preserve relative links. Use the repository root
only when no established location exists; resolve competing locations from
repository conventions before writing. Use `assets/primitives/`
for new files, removing scaffold placeholders. Link to the fact's owning file.
Mark non-UI projects explicitly in DESIGN.md. Keep STATE volatile and DECISIONS
durable; do not invent dates, owners, product intent, or historical decisions.

## Discover and integrate

Work directly for small repositories or a narrow refresh. Delegate independent
areas when that saves time or improves coverage; there is no required worker
count. Read [index-roles.md](references/index-roles.md) when splitting discovery.
Its roles are coverage suggestions, not mandatory agents.

Use `spawn_agent` with the minimum context, read-only scope, one evidence
output, and no further delegation. Inherit model and effort. Continue a distinct
inspection or integration preparation while workers run. Read
[model-routing.md](references/model-routing.md) only for requested routing changes.
Separate tasks are optional only when explicitly requested by the user.

Label material claims verified, inferred, unknown, or stale. Source, tests, and
runtime observations outrank unsupported documentation; distinguish implemented
behavior from exercised behavior. Include compact path/symbol/command evidence.

For consequential contradictions or a broad initial synthesis, use a fresh
read-only verifier on raw claims and source evidence. For a small refresh, the
coordinator can check the affected claims directly. If independent verification
is unavailable, disclose the limitation and finish supported documentation;
do not invent a verifier or block accessible indexing merely for tool absence.

Only the coordinator writes primitives. Resolve conflicting claims by evidence
quality and freshness, preserve unknowns, and inspect the final diff.

## Validate and report

Check that the six documents coexist, referenced paths and commands exist or
are labeled unverified, no scaffold remains, and cross-document claims agree.
Map known acceptance criteria to available checks. Record revision and coverage
so the next refresh can be scoped. Do not run broad builds solely for indexing.

Report created or refreshed documents, material unknowns, and checks performed.

## Cancellation and changed scope

On cancellation or revoked scope, interrupt affected workers immediately before
other work, invalidate pending outputs, and preserve existing changes. Update
or disable related scheduled work only within the user's cancellation scope.
For a correction, stop conflicting work first, then send the revised contract;
accept subsequent results only against the current request and artifact state.
