---
name: prepare-project
description: Set up project documents, working files and agent workflow instructions for a new or existing project the user controls, then produce a grounded implementation plan. Use when establishing or revising a project's development foundation.
---

# Prepare project

Leave the project ready for implementation, with usable records and verified prerequisites.
Reuse existing equivalents; do not create competing documents or replace useful conventions.
Preparation does not authorize product implementation, publication or deployment.

## 1. Confirm the project and control

Identify the target repository and whether the user wants new-project setup or an existing-project update.
Confirm that they control its architecture, documentation and development workflow through ownership or delegated authority.
Use prior confirmation when available; ask only if unclear. Repository access alone does not establish control.
If they lack that authority, stop this setup workflow and explain why.

## 2. Inspect the existing setup

Read existing agent instructions, README, development commands, documentation and installed skills.
For an existing project, inspect enough code and tests to understand its structure.
Present a short Keep / Update / Create list. Preserve unrelated edits.
For a new project, report what exists without inventing implemented behavior.

## 3. Settle missing choices

Confirm missing decisions about purpose, scope, success criteria, technology, agent tools and where plans/tasks live.
Reuse settled choices. Research technical unknowns and record unresolved questions.
Save purpose, scope and success criteria in the project brief; technology decisions in the architecture guide;
agent tools, selected skills and Stash/Linear associations in the agent instructions; exploratory questions in Stash and task blockers in Linear.
Reuse existing equivalents. Record significant trade-offs in decision records.

## 4. Write the project documents

Update existing equivalents first. Use these default locations when none exist:

| File | Write |
| --- | --- |
| `docs/project-brief.md` | Problem, users, scope, exclusions and acceptance criteria |
| `ARCHITECTURE.md` | Components, responsibilities, user/system flows, state ownership and data lifecycle |
| `GLOSSARY.md` | Confirmed domain vocabulary; omit when no useful terms are established |
| `docs/development.md` | Prerequisites, install/start/test/inspection commands and required services |
| `docs/adr/` | Significant decisions with alternatives and consequences; no invented starter ADR |
| `README.md` | Project purpose, short getting-started path and links |
| Agent instruction file | Working rules, skill usage and links to canonical records |

Cover relevant permissions, credentials, sensitive data, errors, retries, cancellation and recovery.
Label proposed architecture and unverified commands. Save research and working drafts in Stash, implementation plans/tasks in Linear.
Do not create repository research dumps or duplicate Markdown plans. Add operational runbooks only when needed.
Add a feature map only for implemented behavior. Use the instruction files the selected agents actually load.
Require affected records to be updated alongside code. Treat boundaries and contracts as revisable;
notify the user when research or implementation evidence warrants meaningful changes.

Add a `Project notes and work tracking` section to `AGENTS.md` or the selected agents' equivalent.
Include the verified Stash project link/ID and Linear team/project links, then this rule:

> Use `project-notes` during research and design. Save ideas, research and working drafts in this project's Stash workspace.
> Use `to-spec` for substantial work needing a shared specification, and `to-tickets` for its implementation breakdown in Linear.
> Keep only settled, maintained documentation in the repository. Small changes can go directly to `to-tickets`.
> Saved research is reference material, not implementation approval. Update affected project documentation alongside code.

Record that `e-mode` routes the work and `long-running-work` owns substantial implementation, Linear progress and checkpoints.
Use available project verification skills for real user paths. Require a separate audit log only when explicitly needed.

Update an existing equivalent section rather than duplicating it. Resolve missing project associations or report them as blockers; do not leave invented links.

## 5. Set up working files

Establish the agreed location for plans/tasks. Reuse the existing tracker when selected; do not duplicate it in local docs.
Add necessary configuration examples with fake values, and ignore secrets, local state and generated scratch files.
Check existing ignore rules before editing. Keep reproducible configuration and intentional evidence trackable.
Do not introduce a tracker, approval workflow or external configuration without an agreed choice.

## 6. Configure skill usage

Ensure every skill in the estack collection is installed for each selected agent by default, including this skill.
Discover the full collection from the verified estack source; do not rely on a fixed subset or assume the current agent's available skills prove another agent is configured.
Reuse existing installations and install missing skills with their required resources and license files, using each agent's supported method and the user's existing installation scope.
If the source or installation scope is unclear, ask. Do not require a project-local skills directory or overwrite customized installations without agreement.
Verify the complete collection is discoverable by each selected agent. Record task-specific usage rules in project instructions; installing all skills does not require invoking all of them on every task.
Report any missing or unverifiable skill and mark skill setup incomplete until resolved.

## 7. Verify the setup

Check document links, instruction loading and skill discovery.
Verify Stash/Linear lookup and that the agent instructions contain the ongoing notes rule; do not create test notes or tickets just to check access.
Run available install/build/test/start commands appropriate to the project, using a clean checkout or isolated state where practical.
Verify one real user path when a runnable product exists. Clean up processes and scratch state created for verification.
For an empty project, report which checks cannot run yet. Record missing credentials, services and other blockers.
Do not repair unrelated product defects merely to pass setup verification.

## 8. Finish the implementation plan and report

Prepare the Linear implementation breakdown with outcomes, starting points, dependencies and work checkboxes.
Use `to-spec` first when substantial work needs a shared specification; skip it for a straightforward task.
Use `to-tickets` for review and publication; do not create a parallel Markdown plan in the repository.
Keep acceptance checkboxes separate and include how each outcome will be verified.
Include relevant integration, documentation, migration and recovery work. Detail the next slice; expose later assumptions.
Follow established review and approval rules without adding gates. Do not force one module per diagram node.
Check that the documents agree and the next slice is actionable.

Show the actual setup file tree, marking relevant files as created, updated or reused.
Include project documents and working configuration; omit unrelated files.
Show any remaining required files separately as pending, never as completed setup.
Report skill usage rules recorded, checks run and remaining blockers.
Link the plan and state whether preparation is complete or partial. Empty templates do not count as completed setup.
Stop before product implementation unless the user has also authorized it.
