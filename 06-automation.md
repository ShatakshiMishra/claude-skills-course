# Module 6 — Automation & Scheduling

Getting Claude to run work repeatedly, on a timer, or as an orchestrated multi-agent job.

## Skills covered

| Skill | Role | Time horizon |
|-------|------|-------------|
| `run` | Launch and drive *this project's app* to see a change working | now, once |
| `loop` | Repeat a prompt or slash command on an interval within a session | minutes–hours, this session |
| `schedule` | Create/manage **cloud** agents that run on a cron schedule | days–forever, unattended |
| `workflow-authoring` | Reference for writing multi-agent orchestration scripts | one big job, many agents |

## `run` — see it actually work

When you want proof a change works in the real app (not just tests):

> **You:** /run
>
> **You:** start the app and take a screenshot of the new settings screen

Claude finds how the project launches (CLI, server, browser app, Electron, …) and drives
it. Use it to confirm a fix visually.

## `loop` — repeat on an interval

For polling or recurring checks *within a session*:

> **You:** /loop 5m check the deploy status and tell me when it goes green

Give it an interval (`5m`) or omit it to let Claude self-pace. Good for "keep an eye on
CI," "re-run this every few minutes." It stops when you stop it or the session ends.

## `schedule` — unattended cron agents

For work that should run when you're not there:

> **You:** every weekday at 8am, summarize my open PRs and message me

or

> **You:** run this once tomorrow at 3pm

This creates a **cloud routine** that fires on schedule. Use it for morning briefs, nightly
reports, weekly cleanups. Manage them with the same skill ("list my scheduled agents").

### `loop` vs `schedule` — which one?

- Same session, you're around, short horizon → **`loop`**
- Unattended, survives your session, cron-like → **`schedule`**

## `workflow-authoring` — orchestrate many agents

For a big job you want to fan out across many subagents deterministically (e.g. "review
every changed file across 5 dimensions, then verify each finding"). This skill is the
*reference for writing the script*. **You must explicitly opt in** to multi-agent
orchestration — it can spawn many agents and use a lot of tokens — by saying something
like "use a workflow" or "fan out agents."

> **You:** use a workflow to review all changed files for bugs, perf, and style, then verify each finding

## Try it

1. `/run` your project (or ask Claude to launch a simple script) and confirm it works.
2. `/loop 2m` a trivial check ("tell me the current time") and then stop it.
3. Ask to "schedule a one-time reminder in 10 minutes" and then "list my scheduled tasks."

Next: [Module 7 — Config & Setup](07-config-and-setup.md)
