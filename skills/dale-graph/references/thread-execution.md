# Optional separate-task execution

Use only when the user explicitly requests separate Codex tasks, a fork, or a
durable task handoff. Subagents remain the default for parts of the current task.
Do not create separate tasks automatically because a subagent tool is missing.

Inspect the live task tools. Resolve a saved project with `list_projects` before
`create_thread`. Follow its Git/worktree defaults and the user's explicit target.
Use `fork_thread` for an explicitly requested fork. A fork copies completed
history only; send the active request and complete work contract afterward.
Do not pass a queued `clientThreadId` to a tool requiring `threadId`.

Keep overlapping writers sequential or explicitly isolated. Validate accepted
changes in the destination checkout, even when worker-local checks passed.
Preserve existing Git state and the user's authority for commits and publication.

Omit model overrides by default. Retain task IDs, host IDs, wait cursors, scope,
and artifact identity. Use bounded `wait_threads` calls with cursors; use
`read_thread` when compact output lacks evidence. Only the calling coordinator
schedules work; do not start an additional nested graph in each task.

User-owned tasks remain available unless the user asks to archive them. Emit the
required created-task directive with the exact returned identifier. A requested
remote handoff must use supported handoff tools, never guessed host state.
