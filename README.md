# Dale

A focused toolbox for Codex: think through a direction, map a repository,
delegate independent work, verify the result, and resume work when needed.

## Install and update

```sh
curl -fsSL https://borkiss.net/dale-install.sh | sh
```

Run `dale` for the interactive skill picker. For an existing installation:

```sh
dale update --yes
dale list --json
```

Restart Codex after updating. The updater supports plugin-cache and standalone
skill installations and preserves the previous plugin version for rollback.
Headless options and the installer implementation are documented in
[tui/README.md](tui/README.md). Updating skills does not require replacing your
global `AGENTS.md`.

## Execution in 0.5

Dale uses the calling agent and subagents by default. Delegate when a work unit
can progress independently and saves time or supplies meaningful independent
evidence. Small or tightly coupled work stays local. The coordinator works on a
complementary part, integrates accepted artifacts, and verifies the final target.

| Need | Execution |
|---|---|
| Small or sequential work | Calling agent |
| Independent implementation or evidence | Bounded subagents |
| Explicitly requested separate task, fork, or durable handoff | Codex task tools |
| Requested future observation or continuation | Product automation with durable state |

A graph is a set of outcomes, dependencies, and evidence obligations. It does not
require a sidebar task for every node. Workers inherit the chosen model and
reasoning by default, including Astra when it is the calling model. Explicit
user routes override inheritance; economical routing is optional and uses the
live model catalog rather than a hard-coded generation or maximum effort.

Each worker has an observable output, minimal inputs, a read/write boundary,
and an evidence requirement. Overlapping mutations are serialized or explicitly
isolated. Subagents share the checkout by default. The coordinator schedules
one delegation level by default and checks the integrated result.

## Skills

| Skill | Purpose |
|---|---|
| `$dale-brainstorm` | Explore ideas and tradeoffs in conversation; converge or implement when asked |
| `$dale-coach` | Inspect selected recent task history and suggest evidence-backed workflow improvements |
| `$dale-lenses` | Reframe a bounded hard question through a useful falsifiable model |
| `$dale-index` | Create or incrementally refresh six repository knowledge primitives |
| `$dale-graph` | Derive and execute an adaptive graph with subagents where useful |
| `$dale-max` | Complete consequential work with independent review and evidence-based acceptance |
| `$dale-proof` | Verify a technical claim within an explicit evidence boundary |
| `$dale-visualize` | Create a self-contained HTML explanation or interactive artifact |
| `$dale-loop` | Choose and run a resumable workflow |
| `$dale-loop-project` | Coordinate independently reviewable changes and authorized PR delivery |
| `$dale-loop-pr` | Monitor or repair a PR within the requested scope |
| `$dale-loop-repo` | Perform bounded repository maintenance on a requested cadence |
| `$dale-loop-watch` | Notify or act on meaningful source changes |
| `$dale-loop-goal` | Keep one explicitly requested objective moving toward direct proof |

Select a skill in Codex or name it in your request. Coach and Max remain
explicit-invocation workflows. Each skill is independently installable; local
references belong to that skill and do not require another Dale skill.

## Repository knowledge

Index completes or refreshes an established primitive directory in place,
or starts a new set in the repository root:

- `REQ.md`: intent, scope, requirements, acceptance criteria.
- `CONTEXT.md`: architecture, contracts, repository map, operations.
- `STATE.md`: current work, blockers, risks, next actions.
- `TDD.md`: actual test strategy, commands, quality gates, coverage gaps.
- `DESIGN.md`: existing UI language and states, or explicit non-applicability.
- `DECISIONS.md`: evidenced decisions, alternatives, consequences, and dates.

An incremental refresh checks changed claims and affected consumers, including
uncommitted work. Missing baselines trigger broader inspection. Discovery is
read-only; the coordinator writes and checks the final documents. There is no
mandatory worker count or saved-project requirement.

## Evidence and lifecycle

Max retains independent review as an acceptance gate. Its worker may be the
calling agent or a scoped subagent; additional reviewers need a concrete
uncovered risk. If independence is unavailable, useful work can continue but
the Max gate cannot be reported as passed. Review and testing stop when the
required evidence is sufficient; changed artifacts invalidate affected evidence.

Proof distinguishes declared, implemented, tested, and observed behavior. A
worker's completion message or green local checks alone do not prove a deployed
or integrated result. Report what changed, decisive evidence, and limitations;
full orchestration ledgers are available when requested.

Loops persist source identities, actions, evidence, and next conditions. They
re-observe on wake and do not assume subagents survive between runs. Unchanged
monitoring stays quiet. Existing user authorization persists; the workflow does
not invent authority for publication, merge, deployment, or external messages.

## Design basis and validation

The Astra adaptation follows the official
[prompting guidance](https://developers.openai.com/api/docs/guides/latest-model#prompting-best-practices):
explicit delegation conditions, proportionate verification, focused instructions,
and continuation through already-authorized work. Skills retain outcome and
ownership contracts while avoiding compulsory orchestration machinery.

Validate skill frontmatter and references, then exercise realistic scenarios:
small direct changes, independent work with a shared contract, incremental
indexing, unavailable review, monitoring-only requests, and mid-run corrections.
Compare correctness, rework, unnecessary questions, elapsed time, and usage when
available. Static validation alone does not establish speed or cost improvements.

## License

Dale is licensed under the [Mozilla Public License 2.0](LICENSE).
Bundled third-party examples retain their source license notices.
