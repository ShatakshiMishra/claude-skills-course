# Module 3 — Artifacts & Design

An **Artifact** is a live web page Claude publishes to claude.ai — a dashboard, a tool, a
mockup, a report you can actually click. These skills make artifacts good.

## Skills covered

| Skill | Role |
|-------|------|
| `artifact-design` | Design fundamentals — load *before writing any artifact* to calibrate effort and quality |
| `artifact-diagramming` | How to draw a diagram inside an artifact that shows the real mechanism, legible in light and dark |
| `artifact-capabilities` | Runtime powers a published page can have — saving state, reading live data, remembering what viewers do, storing files |
| `design` | A multi-artboard visual **design canvas** — UI mockups, landing pages, posters, flyers you can refine by hand |

## The difference between `design` and a plain Artifact

- **Artifact** = a working web page (a calculator, a dashboard, an interactive report).
  The `artifact-*` skills are the *craft guidance* Claude reads before building one.
- **`design`** = a visual *canvas* of artboards (screens, pages, print pieces) meant to
  be tweaked visually — closer to Figma than to code. Reach for it when you want a
  mockup/wireframe/poster you'll nudge by hand, not a functioning app.

## When they trigger

- Asking for **"a mockup / wireframe / landing page / poster / flyer / one-pager"** →
  `design` (the canvas).
- Asking for **"an interactive page / dashboard / tool / game"** → an Artifact, and Claude
  loads `artifact-design` (and `artifact-diagramming` / `artifact-capabilities` as needed)
  behind the scenes.

You rarely invoke the `artifact-*` skills by name — they're support skills Claude pulls in
automatically. `design` you can ask for directly ("design me a…").

## What `artifact-capabilities` unlocks

Normal HTML is static. This skill is what lets a published artifact:

- **Remember** what people do — a poll, a sign-up sheet, a checklist that survives reload
- **Share state** across everyone viewing it
- **Read live or connected data**
- **Store files** viewers upload, or hand viewers a file to download
- **Know who's viewing**, or **ask Claude a question** from inside the page

If you want a page that does any of that, say so — e.g. "a team poll that saves votes
everyone can see" — and Claude will load this skill to wire it up.

## Worked examples

**A design canvas:**
> **You:** design a landing page for a note-taking app — hero, three features, pricing, footer

Claude uses `design`, lays out artboards on a canvas you can refine and export.

**A stateful artifact:**
> **You:** build me a shared retro board where the team can add sticky notes that everyone sees

Claude builds an Artifact and loads `artifact-capabilities` to persist the notes.

**A diagram-heavy artifact:**
> **You:** make a page explaining our request flow with a clear architecture diagram

Claude loads `artifact-diagramming` so the diagram shows the real mechanism and reads in
both light and dark themes.

## Try it

1. Ask for a **poster** ("design a poster for a Friday game night") → notice you get a
   canvas.
2. Ask for a **tool** ("build a tip calculator I can use on my phone") → notice you get an
   interactive artifact.
3. Ask for a **stateful** version ("…that remembers my last bill amount") → notice the
   capabilities kick in.

Next: [Module 4 — Data Visualization](04-data-visualization.md)
