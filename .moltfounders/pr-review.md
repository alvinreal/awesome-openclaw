# PR Review Rules

## When to Run

On every PR review loop cycle, scan all open pull requests.

## PR Review Loop Summary - 2026-05-09

### Agent PRs
- **#33** (alvinreal): HermesClaw addition - Valid but third-party, labeled `needs-human`

### Community PRs
- **#29** (fvasco): now4real plugin - Already reviewed, skipped
- **#27** (sofiane8910): Onepilot - Already reviewed, skipped
- **#26** (MohamedAbdallah-14): prompt-to-asset - Already reviewed, skipped
- **#25** (kriptoburak): tweetclaw - Already reviewed, skipped
- **#20** (xuc865): SkillClaw - Already reviewed, skipped
- **#18** (cheapestinference): Silos Dashboard - Already reviewed, skipped

## PR Review Loop Summary - 2026-05-09

### Agent PRs
- **#33** (alvinreal): HermesClaw addition - Valid but third-party, labeled `needs-human`

### Community PRs
- **#29** (fvasco): now4real plugin - Already reviewed, skipped
- **#27** (sofiane8910): Onepilot - Already reviewed, skipped
- **#26** (MohamedAbdallah-14): prompt-to-asset - Already reviewed, skipped
- **#25** (kriptoburak): tweetclaw - Already reviewed, skipped
- **#20** (xuc865): SkillClaw - Already reviewed, skipped
- **#18** (cheapestinference): Silos Dashboard - Already reviewed, skipped

## Trusted Agent Identity

- Any PR authored by GitHub user `alvinreal` is an **agent PR**.
- Any other PR is a **community PR**.

## Processing Order

1. Process all **agent PRs** first
2. Then process **community PRs**

## Global Rules

- Skip all draft PRs
- Reopened PRs are treated as fresh
- Community PRs already labeled `agent:reviewed` are skipped until new activity arrives
- Agent PRs are re-evaluated every run

## Agent PR Path

### Auto-merge eligibility

An agent PR may be auto-merged only if all are true:

- authored by `alvinreal`
- touches **`README.md` only**
- is **non-structural**
- is within the current **mechanically safe lane**
- passes all required checks

Structural changes include heading changes, section renames, order/layout changes, and formatting convention changes.

### Required checks before merge

Run all of these before merging an agent PR:

1. Verify the diff still touches `README.md` only
2. Verify the diff remains non-structural
3. Verify links resolve
4. Verify GitHub badge format remains correct where used
5. Verify no unintended duplicate listing is created
6. Verify official-resource claims directly when applicable

If any required check fails, merge is blocked.

### Safe lane

The initial unattended safe lane is limited to:

- broken-link fixes or removals
- deduplication
- canonical-source replacement
- obvious category corrections
- official OpenClaw resource additions or updates

If an agent PR is valid but outside that safe lane, leave it open and apply `needs-human`.

### Fixable issues

One fix attempt is allowed for clearly fixable issues only:

- wording cleanup
- placement/category adjustment
- badge/entry format fixes
- duplicate cleanup
- simple conflict resolution

If still failing after one fix attempt, close the PR with a short specific reason.

### Conflict handling

- Community PR with conflicts: skip
- Agent PR with conflicts: if otherwise eligible, attempt one safe resolution and re-check

### Outcomes for agent PRs

- **Eligible and valid:** merge silently
- **Valid but outside auto-merge scope:** leave open and apply `needs-human`
- **Mixed-scope PR** (safe + forbidden changes): close

## Community PR Path

### Review requirements

Review community PRs against `CONTRIBUTING.md` and the current `README.md` state.

Check:

- OpenClaw relevance
- link validity
- description neutrality and clarity
- latest meaningful commit is within the last 30 days
- category fit
- duplicate status
- whether the change improves the list without creating cross-category duplication

### Outcomes for community PRs

- **Valid:** leave a clear review comment and apply `agent:reviewed`, `agent:approved`, and `needs-human`
- **Needs changes:** leave a clear review comment and apply `agent:changes-requested`
- **Mechanically invalid or clearly out of scope:** close with a specific reason and apply `agent:rejected`

Community PRs are never auto-merged.

### Label maintenance

- If a community PR gets new commits or other meaningful new activity, clear outdated agent review labels before re-reviewing it
- Remove outdated failure or escalation labels automatically when the PR state becomes valid again
