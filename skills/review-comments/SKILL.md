---
name: review-comments
description: Remove unnecessary, stale and redundant code comments from requested files or a diff, preserving justified rationale and required notices. Use for comment cleanup or a focused comment review.
---

# Review comments

Be aggressive about comment noise. A comment must earn its place.
Use the available tools; no particular agent type or other skill is required.

## 1. Set scope

Use the requested files or diff. Otherwise inspect the current changes against the repository's configured base branch,
including staged, unstaged and relevant untracked files. Ask if the base cannot be established.
Read project rules and surrounding code. For a review-only request, report findings without editing.

## 2. Remove noise

Delete narration of obvious code, redundant headings and banners, stale explanations, commented-out code and unsupported warnings.
After inspecting the context, delete ordinary explanatory comments when their value remains uncertain.
Do not preserve a comment merely because it sounds authoritative or says `IMPORTANT`.

Preserve legal/license notices and accurate public API contracts.
Keep concise explanations of non-obvious rationale, invariants, ordering, recovery, side-effect boundaries
and external compatibility constraints when the explanation adds information the code cannot make clear.
Keep issue/RFC references that explain a relevant constraint.
Delete obsolete or redundant doc comments too; do not remove accurate contract information as noise.

## 3. Check directives and claimed constraints

Distinguish ordinary prose from tool directives such as lint/type suppressions, formatter controls and build annotations.
Inspect the affected rule and verify a directive is unnecessary before removing it; do not hide a real defect by deleting its explanation.
If removing a directive needs application-code changes, report that separately unless those changes are authorized.
Verify suspicious claims against callers, tests or relevant dependency behavior. Do not invent a justification to keep a comment.

## 4. Stay within cleanup

Report places where names or structure should make behavior clearer.
Do not change runtime behavior, redesign components or widen the task merely to eliminate comments.
If a deleted comment claimed an unenforced constraint, report that constraint and the smallest useful follow-up.
Do not add tests or abstractions solely to justify a comment deletion.

## 5. Verify and report

Inspect the diff for accidental executable-code changes. Run relevant existing checks when directives or tooling behavior are affected.
Report the cleanup, important retained comments and any unresolved directives or refactoring recommendations.
Do not present the deletion count as proof that the code improved.

Adapted from Lauren Tan's pstack [no-comments](https://github.com/cursor/plugins/blob/ce649c03ac3b75b6ae80cbd15b7e2c536caedb5a/pstack/skills/no-comments/SKILL.md)
and [comment-sicko](https://github.com/cursor/plugins/blob/ce649c03ac3b75b6ae80cbd15b7e2c536caedb5a/pstack/agents/comment-sicko.md).
Her copyright and MIT license are preserved in [LICENSE](LICENSE).
