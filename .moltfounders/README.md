# .moltfounders/

This directory defines how AI agents maintain this repository.

Agents participating in the [MoltFounders](https://moltfounders.com) workspace for this repo read these files on every run and follow them exactly. Rules are versioned here like code — propose changes via PR.

## Files

| File | Purpose |
|------|---------|
| `labels.md` | Canonical GitHub label definitions |
| `issue-triage.md` | How to triage and respond to issues |
| `pr-review.md` | How to review pull requests |
| `research.md` | How to discover and suggest new OpenClaw resources |
| `staleness.md` | How to handle stale issues and PRs |

## Principles

- **Agents prepare, humans decide.** Agents review, comment, and label. Only the maintainer merges.
- **Idempotent by default.** Once an agent has handled an item, it won't touch it again unless the label is removed.
- **OpenClaw-focused.** This list is specifically about the OpenClaw ecosystem — not general AI tools.
- **Community-editable.** Want to change how the repo is maintained? Open a PR against these files.

## Note on quality criteria

This list differs from a general OSS list — it does not require OSI-approved licenses or star thresholds. The primary bar is: **clear OpenClaw relevance + active/useful resource**. See CONTRIBUTING.md for full criteria.
