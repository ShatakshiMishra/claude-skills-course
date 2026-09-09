# Module 7 — Config & Setup

Skills that change how Claude Code itself behaves in your project or account.

## Skills covered

| Skill | Role |
|-------|------|
| `init` | Create a `CLAUDE.md` that documents your codebase for Claude |
| `setup-claude` | Guided onboarding — install role-matched plugins, connect tools, try a skill |
| `update-config` | Edit `settings.json` — permissions, env vars, and **hooks** (automated behaviors) |
| `fewer-permission-prompts` | Scan your history and allowlist common safe commands to reduce prompts |
| `keybindings-help` | Customize keyboard shortcuts in `~/.claude/keybindings.json` |

## `init` — teach Claude your repo

Run this once per project:

> **You:** /init

Claude explores the codebase and writes a `CLAUDE.md` — conventions, structure, how to
build/test. Every future session reads it, so answers get more accurate. Re-run it when
the project changes a lot.

## `setup-claude` — first-run onboarding

New to Claude Code, or setting up for a role?

> **You:** /setup-claude

Walks you through installing plugins that match what you do, connecting external tools, and
trying a skill hands-on.

## `update-config` — settings, permissions, and hooks

This is the important one. Use it for anything in `settings.json`:

- **Permissions:** "allow all `npm` commands", "add a `bq` permission", "move this
  permission to user settings."
- **Env vars:** "set `DEBUG=true`."
- **Hooks — the key capability:** any rule of the form *"from now on, whenever X, do Y"*
  needs a **hook**, because the harness (not Claude's memory) enforces it.

> **You:** whenever I stop Claude, run my formatter on changed files

That's a hook, and `update-config` is how it gets wired. Memory/preferences alone can't do
"automatically every time" — only hooks can.

> **Note:** In this desktop session, terminal-only dialogs like `/permissions` and
> `/hooks` aren't available — `update-config` edits the settings files directly instead.

## `fewer-permission-prompts` — stop the nagging

Tired of approving the same safe read-only commands?

> **You:** /fewer-permission-prompts

Claude scans your transcripts for frequent, safe commands and proposes an allowlist for
your project's `.claude/settings.json`. You review before it applies.

## `keybindings-help` — remap keys

> **You:** rebind submit to ctrl+enter
>
> **You:** add a chord shortcut for clearing the screen

Edits `~/.claude/keybindings.json`.

## Try it

1. `/init` in a real project and read the `CLAUDE.md` it produces.
2. Ask `update-config` to "allow `git status` and `git diff` without prompting."
3. Set up one hook: "after every edit, run the linter." Watch it fire.

Next: [Module 8 — Building Your Own Skills](08-building-skills.md)
