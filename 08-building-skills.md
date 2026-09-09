# Module 8 — Building Your Own Skills

The meta module: skills for making things Claude can reuse.

## Skills covered

| Skill | Role |
|-------|------|
| `skill-creator` | Create, edit, optimize, and **eval** skills of your own |
| `new-sdk-app` (`agent-sdk-dev:`) | Scaffold a new Claude **Agent SDK** application |

## `skill-creator` — make a reusable playbook

If you find yourself giving Claude the same instructions repeatedly ("always write commit
messages this way," "review PRs against our checklist"), turn it into a skill.

> **You:** create a skill that drafts release notes from merged PRs in our house style

`skill-creator` helps you:

- **Create** a skill from scratch — it sets up the folder, the description, the
  instructions, and any bundled reference files.
- **Edit / improve** an existing skill.
- **Optimize the description** so the skill triggers reliably (remember Module 1: the
  description is what Claude matches against).
- **Eval** — run tests and benchmark how well the skill triggers and performs, with
  variance analysis.

### Anatomy of a skill (what you'll be authoring)

- A **name** (kebab-case).
- A **description** — the trigger sentence. Spend real effort here.
- The **instructions** — the actual playbook.
- Optional **bundled files** — templates, reference docs, scripts the skill can use.

### The golden rule of skill descriptions

Write the description as *"use this when…"* and pack it with the words a user would
actually say. A vague description means the skill never fires; a keyword-rich one fires
right when it should.

## `new-sdk-app` — build an agent

Want to build a *program* powered by Claude (not just chat in Claude Code)? The Agent SDK
is the toolkit. Scaffold one:

> **You:** create a new Claude Agent SDK app in TypeScript

`new-sdk-app` sets up the project. There are companion verifier agents
(`agent-sdk-verifier-py`, `agent-sdk-verifier-ts`) that check your SDK app follows best
practices once it's built.

> **See also:** the `claude-api` skill (Module 10) is the reference you'll want open while
> building anything that calls Claude.

## Try it

1. Ask `skill-creator` to scaffold a tiny skill: "make a skill that turns bullet points
   into a tweet thread."
2. Read the description it wrote — tighten it so it triggers on your real phrasing.
3. Ask it to **eval** the skill and see the trigger-accuracy report.

Next: [Module 9 — Code Quality & Security](09-code-quality.md)
