# Cheat Sheet — What to Say to Trigger Each Skill

Copy a phrase, tweak it, watch the skill fire. `/x` = slash command; ▸ = a plain-language
prompt that auto-triggers.

## Documents
- ▸ "draft this as a **.docx** / Word memo" → `docx`
- ▸ "make a **PDF**" · "merge these PDFs" · "OCR this scanned pdf" → `pdf`
- ▸ "turn this into a **PowerPoint** / .pptx" → `pptx`
- ▸ "clean this **CSV**" · "add a column and total it as **xlsx**" → `xlsx`

## Artifacts & Design
- ▸ "**design** a landing page / poster / mockup" → `design`
- ▸ "build an interactive dashboard / tool" → Artifact (+ `artifact-design`)
- ▸ "…that **remembers** votes everyone can see" → `artifact-capabilities`

## Data Viz
- ▸ "make a **chart** / **dashboard**" · "give me a categorical **palette**" → `dataviz`

## Memory
- `/consolidate-memory` — tidy memory
- ▸ "**import** this memory export" → `import-memory`

## Automation
- `/run` — launch & screenshot the app
- `/loop 5m <task>` — repeat on a timer this session
- ▸ "**every weekday at 8am**, do X" → `schedule`
- ▸ "**use a workflow** to fan out agents" → `workflow-authoring`

## Config
- `/init` — write CLAUDE.md
- `/setup-claude` — onboarding
- ▸ "**allow** npm commands" · "**whenever** I stop, run the formatter" (hook) → `update-config`
- `/fewer-permission-prompts` — reduce prompts
- ▸ "**rebind** submit to ctrl+enter" → `keybindings-help`

## Build
- ▸ "**create a skill** that…" → `skill-creator`
- ▸ "new **Agent SDK** app in TS" → `new-sdk-app`

## Quality
- `/code-review [PR#] [low|high|max] [--fix|--comment]`
- `/simplify` — tidy without bug-hunting
- `/security-review` — vuln check on the branch

## API
- ▸ "which Claude **model** / what does it **cost**" · "add **tool use** to this Anthropic SDK script" → `claude-api`

## Org / Personal
- `/marvell` — connect internal gateways
- ▸ "**Marvell**-branded **deck**" → `marvell-pptx`
- `/morning` — morning brief
- ▸ "**explain my usage** / where did my tokens go" → `explain-usage`
