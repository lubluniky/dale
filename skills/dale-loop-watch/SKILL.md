---
name: dale-loop-watch
description: Monitor a changing source or condition on a cadence, persist the last meaningful observation, and notify or act only when a user-defined change occurs. Use for watching pull requests, issues, releases, prices, availability, feeds, pages, dashboards, or other external state.
---

# Dale Loop Watch

Build a change detector, not a scheduled summary generator.

## Workflow

1. Define the source, cadence, baseline, meaningful-change predicate, allowed action, notification destination, expiry, and failure limit.
2. Confirm the source can be read reliably and that the action does not exceed the user's authority.
3. Persist the minimum comparable state: timestamp, normalized observation, source identity, and last emitted event.
4. On each wakeup, fetch fresh state and compare it to the baseline. Ignore formatting noise, reordered data, and unchanged results.
5. If no meaningful change occurred, update only necessary health metadata and remain quiet.
6. If the predicate matches, capture evidence, perform the authorized action or notify once, update the baseline, and decide whether to continue.
7. Back off and escalate after repeated source/auth failures. Never interpret inability to read the source as “no change.”
8. Disable scheduled work when the expiry or terminal condition is reached; archive the user task only when requested.

Use the product's automation mechanism. Do not implement cadence with a blocking shell loop.
