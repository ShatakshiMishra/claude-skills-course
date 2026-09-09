# Exercises

A progression from "prove it works" to "build something real." Check them off as you go.
Each one is a prompt you can paste into Claude Code right now.

## Level 1 — Warm-up (trigger awareness)

- [ ] **See your set.** `list my available skills` — read the descriptions.
- [ ] **Format-driven triggering.** Make a `notes.md`, then ask for it "as a Word doc,"
      "as a PDF," and "as a PowerPoint." Note which skill fired each time.
- [ ] **Slash vs. natural language.** Trigger `code-review` once by describing it, once as
      `/code-review`.

## Level 2 — Real deliverables

- [ ] **Spreadsheet cleanup.** Paste messy CSV rows; ask for a clean `.xlsx` with a total.
- [ ] **A chart that isn't ugly.** Give 8–10 fake numbers; ask for "a dashboard." Then ask
      it to "validate the palette for accessibility."
- [ ] **An interactive artifact.** "Build a tip calculator I can use on my phone."
- [ ] **Make it stateful.** "…and remember my last bill." (watch `artifact-capabilities`)

## Level 3 — Developer workflow

- [ ] **Document a repo.** `/init` in a real project; read the `CLAUDE.md`.
- [ ] **Pre-PR ritual.** On a small change: `/simplify`, then `/code-review high`, then
      `/security-review`.
- [ ] **Cut the prompts.** `/fewer-permission-prompts` and review the proposed allowlist.
- [ ] **Wire a hook.** Ask `update-config`: "after every edit, run the linter."

## Level 4 — Automation

- [ ] **Loop.** `/loop 2m tell me the current time`, then stop it.
- [ ] **Schedule.** "Schedule a one-time reminder in 10 minutes," then "list my scheduled
      tasks."
- [ ] **Run it.** `/run` your app and get a screenshot proving a change works.

## Level 5 — Meta / advanced

- [ ] **Build a skill.** Ask `skill-creator` to make "a skill that turns bullets into a
      tweet thread," then tighten its description, then **eval** it.
- [ ] **Call Claude in code.** "Write a Python script using the Anthropic SDK to summarize
      a file, with prompt caching." (watch `claude-api`)
- [ ] **Orchestrate.** "Use a workflow to review all changed files for bugs and style,
      then verify each finding." (opt-in multi-agent)

## Reflection

After finishing a level, answer for yourself:

1. Which skill fired, and **why** — what in my wording matched it?
2. When it *didn't* fire, what phrasing fixed it?
3. Could I turn any repeated task of mine into my own skill?
