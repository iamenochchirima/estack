# Estack

[![skills.sh](https://skills.sh/b/iamenochchirima/estack)](https://skills.sh/iamenochchirima/estack)

Agent skills for setting up projects, researching changes, planning work,
implementing it and verifying the result. Works with Codex, Claude Code and other
agents supported by the skills installer.

Research and working drafts go in Stash. Agreed specifications, tasks and progress
go in Linear. Repositories keep code, maintained documentation and intentional
verification evidence.

## Install

Install all skills into the current project for Codex and Claude Code:

```bash
npx skills@latest add iamenochchirima/estack \
  --skill '*' \
  --agent codex claude-code \
  --copy
```

Choose the agents you use. Add `--global` to make the skills available across
projects. To install one skill, replace `'*'` with its name.

List available skills or update installed skills:

```bash
npx skills@latest add iamenochchirima/estack --list
npx skills@latest update
```

## Workflow

1. Use `prepare-project` to establish or revise a project you control.
2. Use `project-notes` to keep research and working drafts in Stash.
3. Use `to-spec` when substantial work needs a shared specification, then
   `to-tickets` to break agreed work into Linear issues.
4. Use `e-mode` to choose the workflow for the task. Use `long-running-work` for
   substantial implementation, verification and recoverable progress.
5. Use the verification skills to establish and maintain checks of real user paths.

Small tasks can skip unnecessary stages. Install the collection together, then
use the skills relevant to the work. Stash and Linear workflows require access
to those services and the correct project associations; installing skills does
not configure those connections.

## Skills

| Skill | Purpose |
| --- | --- |
| [prepare-project](skills/prepare-project/SKILL.md) | Set up project documents, working files and agent instructions. |
| [project-notes](skills/project-notes/SKILL.md) | Keep research, ideas and working drafts in Stash. |
| [to-spec](skills/to-spec/SKILL.md) | Turn agreed requirements and research into a specification in Linear. |
| [to-tickets](skills/to-tickets/SKILL.md) | Create reviewable Linear tasks with acceptance checks and dependencies. |
| [e-mode](skills/e-mode/SKILL.md) | Guide investigations, fixes, features, reviews and handoffs. |
| [long-running-work](skills/long-running-work/SKILL.md) | Execute substantial work with verification, checkpoints and recovery. |
| [clean-interface](skills/clean-interface/SKILL.md) | Design clear interfaces with concise copy and little visual noise. |
| [review-comments](skills/review-comments/SKILL.md) | Remove unnecessary comments while preserving useful rationale and required notices. |
| [create-verification-skill](skills/create-verification-skill/SKILL.md) | Create a project-specific skill that runs the app and verifies real user paths. |
| [maintain-verification-skill](skills/maintain-verification-skill/SKILL.md) | Keep verification instructions and feature maps aligned with the product. |
| [show-me-your-work](skills/show-me-your-work/SKILL.md) | Keep a detailed decision and evidence log when requested. |

## License

Released under the [MIT License](LICENSE). Upstream credits and adaptation details
are recorded in [ATTRIBUTIONS.md](ATTRIBUTIONS.md).
