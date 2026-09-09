# Module 1 — What Skills Are & How They Trigger

## The mental model

Think of skills as **specialist playbooks**. Claude's base behavior is the generalist.
When your task matches a playbook, Claude opens it and follows the steps that expert
would. The playbook can bring extra tools, file templates, reference docs, and hard
rules ("always validate the palette before drawing a chart").

A skill has three parts that matter to you:

1. **A name** — e.g. `pdf`, `code-review`, `skill-creator`.
2. **A description** — a sentence listing *when* to use it. This is what Claude matches
   your request against, so the more your wording overlaps the description, the more
   reliably it triggers.
3. **The instructions** — loaded only when needed, so they don't clutter every chat.

## Two ways skills load

### Auto-trigger (most common)

You describe a task in plain language. If it matches a skill description, Claude loads it.

> **You:** clean up this messy CSV and give me a proper spreadsheet
>
> → matches the `xlsx` description → Claude uses the `xlsx` skill.

You don't need to know the skill name. This is the intended default.

### Explicit invoke (slash commands)

Type a slash command to demand a specific skill:

```
/code-review
/init
/security-review
```

Use this when you know exactly which playbook you want, or when a skill won't reliably
auto-trigger from a vague request.

## Where skills come from

- **Built-in** — ship with Claude Code (`pdf`, `docx`, `code-review`, …).
- **Plugin** — added by a plugin; named `plugin:skill` (e.g. `agent-sdk-dev:new-sdk-app`).
- **Organization / personal** — set up for your account (e.g. a `marvell` skill).

Because of this, **your list is not universal.** Always check yours.

## Seeing your skills

Just ask:

```
list my available skills
```

Claude can enumerate them (there are tools behind the scenes for this). You'll get names
and one-line descriptions — that description tells you when each one kicks in.

## Why triggering sometimes "misses"

If a skill didn't fire when you expected, it's almost always because your wording didn't
overlap its description. Fixes:

- Name the artifact explicitly ("a **.docx**", "a **PDF**", "a **PowerPoint**").
- Or just invoke it by slash command.

## Try it

1. Run `list my available skills` and skim the descriptions.
2. Pick one skill and guess three phrasings that would auto-trigger it. Test one.
3. Then invoke the same skill by its slash command and compare.

Next: [Module 2 — Documents](02-documents.md)
