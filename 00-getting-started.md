# Module 0 — Getting Started

## What you need

- **Claude Code** — the CLI, desktop app, web app (claude.ai/code), or an IDE extension.
  Any of them can use skills.
- Nothing to install for the built-in skills. Some skills come from **plugins** or your
  **organization**, so your exact list may differ from a teammate's.

## The one thing to understand first

You do not "run" a skill like a program. A skill is **instructions Claude reads** when a
task calls for it. There are two ways one gets used:

1. **Auto-trigger** — you describe a task, and Claude recognizes it matches a skill's
   description, then loads and follows it. Example: "turn these notes into a Word doc"
   auto-triggers the `docx` skill.
2. **Explicit invoke** — you type a slash command: `/code-review`, `/init`,
   `/security-review`. This is a direct request to run that skill.

Both end the same way: the skill's instructions guide Claude's next steps.

## Your first move

Ask Claude what skills you actually have. In this course we assume a broad default set,
but yours is the source of truth:

```
what skills do I have available?
```

or list them explicitly (Module 1 covers this). Then pick a module that matches
something real you want to do.

## How to read the examples

Prompt examples in this course look like this:

> **You:** make a one-page PDF summary of `report.md`

That's what you type. What Claude does next — which skill it picks, what files it
produces — is described right after. Try changing the prompt and watching what triggers.

Next: [Module 1 — What Skills Are & How They Trigger](01-what-are-skills.md)
