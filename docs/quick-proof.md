# Quick proof

Ten-minute path that proves the suite installs and that one skill can run.

## 1. Install

```bash
npx @hxp-tools/ready-suite@latest
```

Or, from a clone:

```bash
bash install.sh
```

Claude Code plugin alternative (pick one method per host):

```text
/plugin marketplace add hannsxpeter/ready-suite
/plugin install ready-suite@ready-suite
```

## 2. Clear the first level

In a greenfield project (or an empty folder you care about), inside your agent:

| Host | Command |
|---|---|
| Claude Code | `/kickoff-ready` |
| Codex | `$kickoff-ready` |
| Other slash hosts | `/kickoff-ready` |

If you already know the stage, skip kickoff and run that skill directly, for example `/prd-ready`.

## 3. Open the reward

kickoff-ready writes `.kickoff-ready/PROGRESS.md` and routes the specialists. Specialist skills write their own `.{skill}-ready/*.md` artifacts. Downstream skills read those files; they never call each other.

## 4. Optional fuller run

Walk the quest map in order: prd-ready, architecture-ready, roadmap-ready, stack-ready, repo-ready, production-ready, then the shipping tier. Or jump to the stage that matches where the project already is.

Full map and install options: [README.md](../README.md). Boundaries: [SUITE.md](../SUITE.md).
