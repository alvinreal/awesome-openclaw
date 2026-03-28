# Issue Triage Rules

## When to Run

On every agent loop cycle, scan all open issues.

## Skip Conditions

- Issue already has `agent:reviewed` label → skip entirely
- Issue was opened by an agent → skip
- GitHub-generated issue (dependabot, etc.) → skip

## Triage Steps

### 1. Classify the issue type

- **Addition request** — someone wants a new resource added
- **Removal request** — entry is stale, broken, or no longer relevant
- **Correction** — fixing a description, link, or category
- **Question / discussion** — not a concrete change request
- **Spam / off-topic** — unrelated to OpenClaw

### 2. Evaluate based on type

**Addition requests — quality bar:**
- Does it have clear OpenClaw relevance? (Is it a skill, plugin, tool, guide, or resource for OpenClaw users?)
- Does it have a working repo or page?
- Is it actively maintained or at minimum a useful stable reference?
- Is it not already in the list? (Search README before commenting)
- Does it fit an existing category?

Note: Unlike general OSS lists, this list does NOT require:
- OSI-approved license (many tools are proprietary-friendly or not code)
- Specific star count (small but useful OpenClaw tools are welcome)

The primary bar is: **genuinely useful to OpenClaw users**.

**Removal requests:**
- Is the reason valid? (broken link, project dead, no longer OpenClaw-related)
- Verify the claim independently.

**Corrections:**
- Is the correction accurate?
- Does it follow CONTRIBUTING.md format?

**Questions/discussions:**
- Answer if you can from the README/CONTRIBUTING.md context
- Label `needs-human` if it requires maintainer judgment

**Spam/off-topic:**
- Label `needs-human`, leave a polite comment explaining the repo's scope

### 3. Comment

Leave a clear, helpful comment with your verdict and specific feedback. Be friendly — contributors put effort in.

### 4. Apply labels

- Always apply `agent:reviewed` after handling
- Apply `agent:commented` if you left a comment
- Apply `duplicate`, `not-openclaw-related`, `needs-info`, or `broken-link` as appropriate
- Apply `needs-human` if you cannot resolve confidently

## Edge Cases

- **Unclear if OpenClaw-relevant:** Label `needs-info`, ask submitter to clarify the connection
- **Project is useful but not specifically OpenClaw:** Label `not-openclaw-related`, explain the scope
- **Issue is very old (>90 days, no activity):** Follow staleness rules in `staleness.md`
