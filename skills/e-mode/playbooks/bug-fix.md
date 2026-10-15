# Bug fix

Use when the user asks to correct a reported defect. If they ask only to diagnose it, use Investigation.

1. Capture the reported behavior, expected behavior, affected version or environment, and a reproduction path. Use the project's verification skill when one exists. If the real surface is unreachable, record the blocker and use the closest valid test seam; do not call that an end-to-end reproduction.
2. Gather evidence before editing. Form plausible causes and rule them out with source inspection, traces, logs, tests, or a controlled run. State the mechanism that explains the symptom. If the mechanism remains uncertain, say so and narrow the next check.
3. Record the fix approach on the relevant Linear issue. For substantial or multi-session implementation, use `long-running-work` rather than a second execution plan. Check affected callers and side effects. Add a focused regression test when useful; do not write a brittle proxy test just to satisfy a sequence.
4. Fix the cause in the existing path. Remove a superseded path when safe. Do not stack speculative guards or broaden the change to nearby features without explaining why the bug requires it.
5. Rerun the original reproduction and relevant automated checks. Check the main failure path and likely regression paths. Save inspectable evidence of the before and after when available. A passing unit test alone does not prove a UI or integration failure is gone.
6. Review the diff and report the cause, change, evidence, and remaining gaps. Open a PR through [Opening a PR](opening-a-pr.md) only when the authorized project workflow calls for one.

Record reproduction and verification evidence in Linear; keep exploratory findings in Stash. Use `show-me-your-work` only when requested or required. Never claim the original failure was reproduced or fixed if either observation was inconclusive.
