# PR Review Rules

## When to Run

On every agent loop cycle, scan all open PRs.

## Skip Conditions

- PR already has `agent:reviewed` label → skip entirely
- PR is a draft → skip
- PR was opened by an agent → skip
- Bot PR (dependabot, etc.) → label `needs-human`, skip

## Review Steps

### 1. Understand what the PR does

Read the PR title, description, and diff carefully.

### 2. Format checks

- Does the entry follow the format in CONTRIBUTING.md?
  ```
  - [owner/repo](url) ![GitHub stars badge] - Short factual description.
  ```
- Is the description short, neutral, and factual (no marketing language)?
- Is it placed in the correct section?
- Is the link valid? (Check URL resolves)
- Stars badge uses `?style=social` format?

### 3. Content checks

**OpenClaw relevance:**
- Does it have a clear, direct connection to OpenClaw? (skill, plugin, integration, guide, tool for OpenClaw users)
- If relevance is tenuous, ask the submitter to clarify in the PR

**Activity / usefulness:**
- Does the repo/resource exist and load?
- Is it reasonably active or at minimum a useful stable resource?
- Abandoned projects with no commits in 12+ months: request changes unless it's a reference/archival resource

**Duplicate check:**
- Search the current README for the repo URL and name
- If duplicate → comment clearly, apply `duplicate` label

**Category fit:**
- Is it in the right section?
- If it fits better elsewhere, suggest the correct section

### 4. Leave your review

Be specific and helpful:
- List each issue with clear explanation
- If approving: say exactly why it meets the bar
- If requesting changes: give actionable feedback

### 5. Apply labels and set review status

- Always apply `agent:reviewed`
- Apply `agent:approved` if the PR meets all criteria
- Apply `agent:changes-requested` if changes needed
- Apply relevant labels (`duplicate`, `not-openclaw-related`, `broken-link`) as needed
- Apply `needs-human` for borderline cases or disputes

## Important: Agent approval ≠ merge

`agent:approved` means the PR passed automated review. **Only the maintainer merges.**

## Edge Cases

- **PR removes a broken link:** Fast-track approve — these are unambiguously good
- **PR fixes formatting only:** Fast-track approve
- **PR adds something useful but format is slightly off:** Request small formatting fix, approve the concept
- **PR has been open >30 days with no author response:** Follow staleness rules in `staleness.md`
- **Submitter disputes feedback:** Stand firm on objective criteria (relevance, format), label `needs-human` for subjective disputes
- **PR adds a commercial tool with OpenClaw integration:** Fine if the integration is real and useful — commercial tools are allowed
