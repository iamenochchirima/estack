---
name: long-running-work
description: Execute substantial, multi-session software work from Linear tickets, with focused verification, Git checkpoints and recoverable progress. Use for sustained implementation, not small changes or planning-only requests.
---

# Long-running work

Use Linear for execution state, Stash for exploratory findings and Git for implementation checkpoints.
Do not create a parallel Markdown plan or `.long-running-work/` directory.

## 1. Load the work

Read the user's authorized outcome, project instructions, relevant Linear issues and linked project docs or Stash research.
Check acceptance criteria, dependencies, readiness rules and the current Git state. Preserve unrelated changes.
On resumption, read the latest ticket progress and inspect relevant commits and working-tree changes before acting.
Reconcile stale tracker state with actual code and verification evidence; do not repeat completed work without a concrete reason.

## 2. Prepare missing tickets

Reuse existing tickets. If the authorized work lacks a usable breakdown, use `to-tickets` to propose and publish it.
Use `to-spec` first only when substantial work needs an agreed specification.
Follow those skills' approval steps and reuse approval already given. Publication or cleared dependencies alone do not authorize implementation.
If a required skill or tracker is unavailable, report the gap; do not silently replace Linear with repository plan files.

## 3. Execute the next actionable ticket

Choose a ticket within the authorized scope whose genuine blockers are resolved.
Mark it in progress using the project's workflow, inspect the relevant implementation and work through its checklist.
Build the smallest coherent change satisfying the acceptance criteria and important existing invariants.
Continue through authorized actionable tickets without asking again for routine decisions already settled.

Add newly discovered work only when needed for the agreed outcome, an existing invariant or a concrete regression caused by this work.
Report material changes in direction and update the affected ticket. Defer unrelated improvements; do not create new external work items without authorization.
Do not introduce speculative cleanup, abstractions or an automatic hardening phase.

## 4. Verify and checkpoint

Run focused checks against acceptance criteria and exercise the real entry point where relevant.
Add meaningful tests for changed behavior and concrete regression risks; do not chase coverage or invent test-count quotas.
Broaden validation when shared changes, failures or project requirements justify it. Stop repeating checks that passed unless new evidence warrants it.
Reproduce and investigate concrete failures until resolved or genuinely blocked. Several failed attempts alone do not establish a blocker.

Inspect the diff and resolve regressions introduced by the ticket. Commit coherent verified changes when authorized, keeping unrelated edits out.
Record the commit hash and verification evidence in Linear. Without a commit, record branch/HEAD, task-owned changed files and verification results.
A checkpoint must describe a recoverable state, not merely claim that work is complete.

## 5. Keep progress recoverable

At meaningful boundaries and before interruption, update the Linear ticket with completed work, checks/results,
last checkpoint, remaining work and the next action. Keep this concise; do not create a running diary.
Save reusable research or design findings in Stash through `project-notes` when available, linking them from the issue.
Keep maintained project documentation aligned with implemented changes.

For a genuine blocker, record the exact problem, its impact and the smallest decision or access needed.
Continue independent authorized work when possible. If Linear becomes unavailable, preserve the working tree,
report unsaved progress in the conversation and reconcile it before starting more tickets; never claim an update was saved.

## 6. Finish

Perform one bounded check against the original outcome and required tickets. Confirm acceptance evidence, integration checks,
updated documentation and any required review, merge or deployment conditions.
Do not mark an issue Done until its project-defined completion conditions are met. Do not infer permission to push, merge or deploy.
If a required gap remains, report partial completion or a blocker. Otherwise record the final checkpoint and report
completed behavior, verification and meaningful deferred work. Stop rather than reopening completed tickets for speculative improvements.
