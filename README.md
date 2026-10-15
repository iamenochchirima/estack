# Estack

[![skills.sh](https://skills.sh/b/iamenochchirima/estack)](https://skills.sh/iamenochchirima/estack)

Reusable agent skills for Codex, Claude Code, and other compatible agents.

## Skills

| Skill | Purpose |
| --- | --- |
| [e-mode](skills/e-mode/SKILL.md) | Cross-project playbooks for investigation, implementation, pull requests, merge follow-up, and handoffs. |
| [show-me-your-work](skills/show-me-your-work/SKILL.md) | An evidence-backed decision log for reviewable long-running work. |
| [create-verification-skill](skills/create-verification-skill/SKILL.md) | Build a project-local way to run the app and verify real user paths. |
| [maintain-verification-skill](skills/maintain-verification-skill/SKILL.md) | Keep that verification skill and its feature map aligned with the product. |
| [long-running-work](skills/long-running-work/SKILL.md) | Execute Linear tickets with focused verification, Git checkpoints and recoverable progress. |
| [prepare-project](skills/prepare-project/SKILL.md) | Set up documents, working files and agent workflow instructions for a project the user controls. |
| [clean-interface](skills/clean-interface/SKILL.md) | Design clean product interfaces with concise copy and little visual noise. |
| [to-tickets](skills/to-tickets/SKILL.md) | Turn agreed work into Linear issues with dependencies, acceptance checks and Stash references. |
| [project-notes](skills/project-notes/SKILL.md) | Maintain research and working drafts in Stash, linking agreed work to Linear and keeping repository docs focused. |
| [to-spec](skills/to-spec/SKILL.md) | Synthesize agreed requirements and Stash research into a concise specification in Linear. |
| [review-comments](skills/review-comments/SKILL.md) | Remove comment noise while preserving justified rationale, contracts and required notices. |

## Install with `npx skills`

List the skills available from the repository:

```bash
npx skills@latest add iamenochchirima/estack --list
```

Install a selected skill for the current project, for example:

```bash
npx skills@latest add iamenochchirima/estack \
  --skill e-mode \
  --agent codex \
  --copy
```

Replace `e-mode` with any skill name in the table. Add `--global` if you
want the skill available across projects. Refresh installed skills later with:

```bash
npx skills@latest update
```

## Install as a Claude Code plugin

This repository also contains a Claude Code marketplace that points to the same
`skills/` directory. From inside Claude Code:

```text
/plugin marketplace add iamenochchirima/estack
/plugin install enoch-skills@enoch-skills
```

The skills are then available under the `enoch-skills` namespace, for example
`/enoch-skills:e-mode`. After publishing a release with both manifest
versions bumped, Claude users can run:

```text
/plugin marketplace update enoch-skills
/plugin update enoch-skills@enoch-skills
```

The Claude plugin declares its version in both `.claude-plugin/plugin.json` and
`.claude-plugin/marketplace.json`. Bump both values for each plugin release so
Claude Code detects the update. The `npx skills` installer continues to use the
repository commit as its update signal.

## License

Released under the [MIT License](LICENSE). Upstream credits and adaptation details
are recorded in [ATTRIBUTIONS.md](ATTRIBUTIONS.md).
