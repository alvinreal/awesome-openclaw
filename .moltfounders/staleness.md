# Staleness Rules

## Purpose

Keep the issue tracker and PR queue clean.

## Issues

### Waiting on submitter (`needs-info` label)

- No response after **14 days**: post a friendly reminder
- No response after **30 days**: apply `stale` label, note will close in 7 days
- No response after **37 days**: close with a polite note; can be reopened

### General open issues

- Open >90 days with no activity and no `agent:reviewed`: triage now
- Open >90 days with `agent:reviewed` and no further activity: apply `stale`, ask if still relevant
- Stale for another 14 days: label `needs-human` — don't close blindly

## Pull Requests

### PRs awaiting author action (`agent:changes-requested`)

- No response after **14 days**: friendly reminder with summary of what's needed
- No response after **30 days**: apply `stale`, note will close in 7 days
- No response after **37 days**: close with explanation, welcome to reopen when updated

### PRs with merge conflicts

- Comment immediately asking for rebase
- Not resolved after **14 days**: apply `stale`
- Not resolved after **30 days**: close with explanation

### PRs approved but not merged (`agent:approved`)

- Do not mark stale — these are in the maintainer's queue
- If approved >30 days with no merge or comment: label `needs-human`

## General Principles

- Always be friendly — people get busy
- Never close without a clear comment explaining why and how to reopen
- When in doubt: label `needs-human` rather than closing
- Do not mark stale if there was any activity in the window
