# Dale Max contracts

## Work unit

```text
Outcome and criteria: <observable result>
Inputs: <request, raw artifacts, previous failed criteria>
Target: <checkout/revision/runtime>
Read scope: <sources>
Write scope: <exclusive paths or none>
Authority and constraints: <current user and repository instructions>
Evidence required: <direct checks>
Return artifact, changes, evidence, and blockers. Do not spawn agents or tasks.
```

## Independent review

```text
Original requirement: <user intent>
Owned risk or criterion: <falsifiable question>
Raw candidate and identity: <artifact/diff and revision>
Available evidence: <commands/results/sources>
Read scope: <sources>; write scope: none
Try to falsify the criterion; do not assume the maker's conclusion.
Do not create agents or tasks. Return supported findings, rejected hypotheses,
missing evidence, and the smallest justified correction.
```

## Acceptance record

For each criterion retain artifact identity, direct evidence, review findings,
coverage boundary, and PASS/REVISE/REJECT/BLOCKED status. Track only state needed
to resume: current work owner, agent ID if any, attempts on the failed signal,
accepted artifact, unresolved risks, and next action. Invalidate evidence when
its target or relevant dependency changes. Reusing a verdict from a different
revision requires checking that the affected behavior is unchanged.
