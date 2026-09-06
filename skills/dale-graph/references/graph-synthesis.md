# Runtime graph synthesis

Derive a graph from required work, not from remembered graph shapes.

## Synthesis procedure

### 1. Derive proof obligations

Convert the request into observable acceptance criteria. For each criterion,
identify:

- the artifact that could satisfy it;
- the evidence that could prove it;
- the source or runtime that owns the truth;
- the authority needed to read or mutate it;
- the failure that would disprove completion.

Unknown proof obligations become explicit discovery work. Do not hide them in a
generic research role.

### 2. Generate work units

Create a candidate work unit for each distinct artifact or evidence boundary.
Split a unit only when its result can be produced and evaluated without another
unit's unfinished context. Merge units when separating them would require
constant cross-reading or duplicate the same decision.

Generate the role name from the owned outcome:

```text
<system or artifact> + <action or lens>
```

Use the task vocabulary; a fixed roster is unnecessary.

### 3. Generate edges

Every edge must carry a reason:

| Edge reason | Meaning |
|---|---|
| artifact | The destination consumes a concrete output from the source |
| decision | The destination cannot proceed until the source resolves a choice |
| conflict | The nodes share a mutation target and must not run together |
| revision | Failed proof returns an artifact to its owning work unit |

Do not add order merely because a sequence feels tidy. Nodes without a real
dependency belong in the same ready frontier.

### 4. Generate proof boundaries

For each artifact, decide whether its evidence can be trusted from the producing
node. Create separate proof work when independence changes confidence,
especially for:

- high-impact or irreversible changes;
- authentication, authorization, privacy, or secrets;
- user-visible and contract-level behavior;
- cross-layer consistency;
- unstable external facts;
- claims based on interpretation rather than direct output.

Proof work may occur before, between, or after production nodes. Multiple
artifacts may share a proof node only when the same evidence and failure modes
apply.

### 5. Normalize

Repeat until stable:

1. Remove nodes with no distinct deliverable.
2. Merge nodes with inseparable context.
3. Split nodes with independent outputs or write owners.
4. Remove unjustified edges.
5. Add missing artifact, decision, conflict, and revision edges.
6. Confirm every acceptance criterion has an evidence path.
7. Confirm every mutating node has exclusive ownership while running.
8. Leave downstream nodes provisional when their role or deliverable depends on
   evidence that does not exist yet.
9. If only one coherent unit survives, return a direct-work recommendation
   instead of manufacturing a graph.

## Graph state

Track only what the current graph needs:

```yaml
objective: user-visible outcome
criteria:
  - id: criterion-id
    proof: direct evidence required
nodes:
  - id: stable-id
    deliverable: observable artifact
    depends_on: []
    executor: coordinator | subagent | explicitly-requested-task
    executor_id: exact returned ID when applicable
    read_scope: sources
    write_scope: exclusive paths or none
    artifact_identity: revision or output identity
    status: provisional | ready | running | passed | revise | rejected | blocked
    evidence: []
edges:
  - from: node-id
    to: node-id
    reason: artifact | decision | conflict | revision
```

Use the worker contract in [node-subagents.md](node-subagents.md). For proof,
include the original requirement, raw artifact and identity, and a falsifiable
question. Keep the reviewer read-only and do not supply the intended verdict.

Add work when a result reveals a necessary artifact or evidence gap; remove it
when it cannot affect acceptance. Re-evaluate as any result arrives. Update
workers after user corrections and reject stale outputs. Expand the graph only
when separate ownership or evidence justifies the coordination cost.
