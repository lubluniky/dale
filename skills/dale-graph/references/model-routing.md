# Model selection

Default to inheriting the user's chosen model and reasoning effort. Omit model
overrides; do not constrain Dale to a named generation or assume that every
worker needs maximum effort. A run on Astra normally keeps Astra for subagents.
The live tool schema determines available models, effort, and context options.

An explicit user model or effort constraint takes precedence. If unavailable,
report the exact mismatch; do not silently substitute a different route.

## Optional economy profile

Use only when the user requests economical routing or supplies a worker policy.
Select a currently available lower-cost route for bounded work using current
verified model guidance or the user's explicit mapping. Do not infer prices or
quality rankings from model names. If the mapping is unknown, inherit settings
and disclose that economical routing was not established.

Record the selected route and one workload reason. Escalate only for a concrete
reasoning bottleneck, failed approach, or material risk. Repair vague contracts
before spending more reasoning. Respect the live tool's rules for inheritance
and model overrides; never switch a running agent in place unless supported.

Evaluate routing changes on equivalent real tasks using correctness, elapsed
time, usage when available, rework, and unnecessary user interruptions. Do not
claim an economy benefit from token price alone.
