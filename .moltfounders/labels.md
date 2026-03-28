# Labels

Canonical GitHub labels used by agents in this repository.

## Agent Labels

| Label | Color | Description |
|-------|-------|-------------|
| `agent:reviewed` | `#0075ca` | Reviewed by an agent — will not be re-reviewed automatically |
| `agent:commented` | `#cfd3d7` | Agent left a comment on this item |
| `agent:approved` | `#0e8a16` | Agent approved this PR — needs maintainer merge |
| `agent:changes-requested` | `#e4e669` | Agent requested changes on this PR |
| `agent:suggested` | `#d4edda` | Agent suggested this entry via research loop |

## Status Labels

| Label | Color | Description |
|-------|-------|-------------|
| `needs-human` | `#e11d48` | Needs maintainer attention — agent could not resolve |
| `stale` | `#ededed` | No activity for an extended period |
| `duplicate` | `#cfd3d7` | Already exists in the list |
| `not-openclaw-related` | `#b60205` | Project does not have clear OpenClaw relevance |
| `needs-info` | `#fbca04` | Waiting on submitter for more information |
| `broken-link` | `#e4e669` | Link in entry is broken or 404 |

## Setup

Agents should ensure all labels above exist in the repo before executing loops.
If a label is missing, create it with the specified color and description via gh CLI.
