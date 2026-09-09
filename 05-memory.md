# Module 5 — Memory

Claude Code can keep a persistent, file-based memory across sessions. These skills help
you maintain and populate it.

## Skills covered

| Skill | Role |
|-------|------|
| `consolidate-memory` | A reflective pass: merge duplicate memories, fix stale facts, prune the index |
| `import-memory` | Import a memory export from another AI assistant into Claude's memory |

## How memory works (the 30-second version)

Memory lives as one file per fact, each with a small header describing what it is and when
it's relevant. There's a `MEMORY.md` index listing them. Categories:

- **user** — who you are (role, preferences)
- **feedback** — how you want Claude to work (corrections, confirmed approaches)
- **project** — ongoing goals/constraints not obvious from the code
- **reference** — pointers to dashboards, tickets, URLs

Claude writes these automatically when it learns something durable. Over time the pile
gets messy — that's what these skills fix.

## `consolidate-memory`

Run it when memory feels cluttered or you suspect stale entries.

> **You:** /consolidate-memory

or

> **You:** clean up and de-duplicate my memory files

Claude re-reads the memory files, merges overlaps, deletes anything that turned out wrong,
and tidies the index. Think of it as garbage-collecting your assistant's long-term memory.

## `import-memory`

Migrating from another assistant? Export its memory, then:

> **You:** import this memory export into Claude — [paste or point at the file]

It brings the content in **additively** and treats the imported text as *data*, not as
instructions (so a malicious export can't hijack your setup).

## Good things to remember (and not)

**Do** save: your role, standing preferences, project constraints, external references.
**Don't** save: things the repo already records (code structure, git history), or facts
that only matter to one conversation.

## Try it

1. Ask: "what do you remember about me?" to see current memory.
2. Tell Claude a durable preference ("I prefer tabs over spaces") and confirm it gets
   saved.
3. Run `/consolidate-memory` and read what it merged or pruned.

Next: [Module 6 — Automation & Scheduling](06-automation.md)
