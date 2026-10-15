# Feature

Use for new or changed behavior. The issue or approved spec defines the outcome when the project has one; a feature map describes what exists now, not what to build.

1. Read the target repository's instructions, the relevant issue or spec, the current implementation, and the user-facing path. If the project uses an owner-approved Ready state for agent-picked work, confirm that state before claiming a ticket. A direct user request is its own authorization within its stated scope.
2. Name the behavior and state changes. For substantial or multi-session implementation, hand execution to `long-running-work` and use Linear tickets rather than a separate plan. Use `to-spec` or `to-tickets` only when that preparation is missing. For a focused change, keep the work and verification concise.
3. Implement the smallest coherent slice in the existing architecture. Delegate independent workstreams when that helps and the environment supports it; keep shared decisions and integration with one owner. Do not require a subagent, a particular model, or a cloud workspace.
4. Verify each slice with the relevant tests and real user path. Reuse a project verification skill where available. Update the canonical feature map and technical documentation when shipped behavior changes. Keep evidence the reviewer can inspect.
5. Check the diff against the issue or spec, test adjacent paths, and report what is complete, what is uncertain, and what changed in the plan. Prepare a PR through [Opening a PR](opening-a-pr.md) when that is part of the authorized workflow.

Record progress and verification on the relevant Linear issue. Save exploratory findings through `project-notes`. A detailed `show-me-your-work` trail is optional unless requested or required by project rules.
