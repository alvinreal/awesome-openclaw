# Research Loop Rules

## Purpose

Periodically discover new OpenClaw resources worth adding and open issues suggesting them.

## Frequency

Run once per week. Do not run if you already opened a research issue in the last 7 days (check `agent:suggested` label).

## Sources to Check

1. **GitHub search** — `openclaw` topic, `openclaw` in repo name, or `openclaw` in description
2. **ClawHub** — https://clawhub.com for new published skills
3. **OpenClaw Discord** — https://discord.com/invite/clawd (if accessible) for community projects
4. **GitHub** — search `openclaw skill`, `openclaw plugin`, `openclaw integration`
5. **Reddit / HN** — search for recent OpenClaw mentions

## Qualification Criteria

A resource is worth suggesting if:
- Clear OpenClaw relevance (skill, plugin, integration, guide, deployment tool, etc.)
- Has a working repo, page, or documentation
- Not already in the list (search README before suggesting)
- Reasonably active or a useful stable reference
- Fits an existing category in the README

## How to Suggest

Open a GitHub issue with:
- **Title:** `[Research] Add: <Project Name>`
- **Body:**
  - Repo/resource URL
  - One-sentence description
  - Suggested category
  - Why it belongs (OpenClaw relevance)
  - Source where you found it

Apply label `agent:suggested`.

## Limits

- At most **3 research issues per cycle**
- Check existing `agent:suggested` issues to avoid duplicates

## Edge Cases

- **Brand new project (<1 week old):** Still suggest if clearly relevant — note recency
- **Official OpenClaw org repo not yet listed:** Definitely suggest it
- **Skill on ClawHub not in the list:** Good candidate — suggest it
