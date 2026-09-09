# Module 11 — Org & Personal Skills

Not every skill ships with Claude Code. Some are added by your **organization** or set up
for **you**. This module covers the ones present in this account — yours may differ.

## Skills covered

| Skill | Role |
|-------|------|
| `marvell` | Wire a project to use the Marvell ModelHub LLM gateway and Marvell MCP gateway via canonical credentials |
| `marvell-pptx` | Build PowerPoint decks in Marvell's official brand system (overrides the generic `pptx` colors/fonts) |
| `morning` | Render a styled morning brief, or set it up as a recurring weekday task |
| `explain-usage` | Explain where this session's tokens went, with a plain-language chart |

## `marvell` — connect to the internal gateways

When you're scaffolding a project that needs LLM access or MCP tools and want it to use
your Marvell setup:

> **You:** /marvell
>
> **You:** set this project up to use my Marvell ModelHub gateway

It wires the project to the canonical credentials in `~/.config/marvell/` — so you don't
hand-copy keys.

## `marvell-pptx` — on-brand decks

Any Marvell presentation should use this instead of the generic `pptx` skill:

> **You:** make a Marvell-branded deck on our Q3 roadmap

Trigger words: **"Marvell"** + *presentation / deck / slides / pptx / PowerPoint*, or "in
Marvell style / on-brand for Marvell." It applies Marvell's official palette, fonts, and
templates — overriding the generic PowerPoint styling.

## `morning` — your daily brief

> **You:** /morning
>
> **You:** set up my morning brief to run every weekday

Renders a styled HTML brief. Note it only fires when you *explicitly* ask for the brief or
to set it up — a casual "what's on my calendar?" is answered directly, not with the full
brief.

## `explain-usage` — where did my tokens go?

> **You:** explain my usage
>
> **You:** where did my tokens go this session?

Produces one simple chart breaking down this session's token usage in plain language.
Useful when a session felt expensive and you want to see what ate the budget.

## The lesson of this module

**Your skill set is account-specific.** The `marvell*` skills exist because this is a
Marvell account; another user won't have them but might have their own org skills. Always
check your own list (Module 1) rather than assuming.

---

That's the tour. Back to the [course index](../README.md), or work through the
[exercises](../exercises/README.md).
