# Deviations from `Anbeeld/AGENTS.md`

`AGENTS.md` here is upstream's text plus the additions below. Anything not
listed on this page should match upstream word for word: if a diff shows
something else, it is a mistake, not an edit.

## Additions, quoted from their source

- *Start every reply with `Canary,`.* - [PR #2](https://github.com/Anbeeld/AGENTS.md/pull/2).
- From [uv's AGENTS.md](https://github.com/astral-sh/uv/blob/main/AGENTS.md):
  the CONTRIBUTING.md pointer, the new-test style, existing-coverage,
  variant-scope and explicit-fixture rules, the pre-existing-failure rule, the
  comment-rationale rule, and the conversation-leak rule (also
  [PR #3](https://github.com/Anbeeld/AGENTS.md/pull/3)).

## Moved, unchanged

- *Do not silently change tested behavior.* - Testing to Boundaries.
- *Commit only when explicitly requested.*, the `--no-verify` /
  `--no-gpg-sign` rule, and *Do not force-push to main/master.* - Git & PRs to
  Boundaries.
- The commit-message and PR-size rules - Git & PRs to Change Constraints. The
  `Git & PRs` heading is gone.

## Reordered on purpose

- `Change Constraints` sits before `Workflow`. Upstream has it after `Testing`,
  which states the size and scope limits after the step that applies them
  ("Implement the smallest correct change"). The decision order is: limits,
  procedure, delegation, verification.
- The `Make it faster` example is nested under the bullet it illustrates
  instead of trailing the section.

## Corrected on purpose, do not restore the upstream wording

- The approval rule reads *before any other destructive action*. Upstream says
  *before executing a destructive action*, which lets an authorized request
  override the absolute force-push prohibition that opens the same bullet.
  `any other` closes that hole.
- *Ask before an unresolved material choice.* drops upstream's tail (*- not
  before a choice the user's request, a higher-authority instruction, or clear
  evidence has already resolved.*): the next bullet states the same rule from
  the other side.
- uv's *NEVER assume clippy warnings or test failures are pre-existing...* loses
  `clippy warnings or`, which is Rust-specific.

## Removed as duplicates or example, no rule lost

- *State uncertainty when something cannot be confirmed.* - Boundaries'
  *State gaps explicitly* covers it.
- *If not, ask or report the gap.*
- *keep unfinished, blocked, or superseded work represented accurately...* -
  Completion states it.
- *Treat a subagent's result as a claim: revalidate it against current state and
  never assume success.* - Workflow step 6 states it.
- *Answer direct questions directly when possible. Example: `npm test`, not
  `The command to run tests npm test.`* - the example only.
