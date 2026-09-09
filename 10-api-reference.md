# Module 10 — The Claude API Reference Skill

## Skill covered

| Skill | Role |
|-------|------|
| `claude-api` | The authoritative reference for the Claude API / Anthropic SDK |

## What it's for

Any time you're **writing code that calls Claude**, this skill is the source of truth for:

- **Model IDs and pricing** — which model to use and what it costs
- **Parameters** — the Messages API shape, streaming, stop conditions
- **Tool use** — defining tools, the tool-use loop, the Tool Runner
- **MCP** — connecting Model Context Protocol servers
- **Agents** — managed/server-hosted agents
- **Prompt caching** — cutting cost/latency on repeated context
- **Token counting** and **model migration**

## Why it matters: don't guess model facts

Model IDs, prices, and limits change. This skill exists so Claude **looks them up instead
of answering from memory**. If you ask "which model should I use and what does it cost?",
the right behavior is to consult `claude-api`, not to recall a possibly-stale number.

Current-generation model IDs you'll see referenced:

- Fable 5.1 — `claude-fable-5-1`
- Opus 5 — `claude-opus-5`
- Sonnet 5 — `claude-sonnet-5`
- Haiku 4.5 — `claude-haiku-4-5-20251001`

When you build an AI app, default to the **latest and most capable** models.

## When it triggers

- You name Claude/Anthropic/an SDK (`anthropic`, `@anthropic-ai`, `claude-*`).
- You ask about an LLM's pricing, model choice, limits, or caching.
- Your task is LLM-shaped with the provider unstated (building an agent, MCP server, tool
  definitions, RAG, an LLM-as-judge, computer use; or debugging refusals, cutoffs,
  streaming, tool calls, tokens).

It deliberately **stands down** when you're clearly working with another provider (OpenAI,
Gemini, Llama, Mistral, etc.).

## Worked example

> **You:** write a Python script that calls Claude to summarize a file, with prompt caching on the system prompt

Claude loads `claude-api`, uses the correct model ID, the right Messages API shape, and
wires up caching per the reference.

## Try it

1. Ask: "what's the current Opus model ID and how do I stream a response?"
2. Ask: "add tool use to this Anthropic SDK script" and watch it follow the reference.
3. Ask: "how do I cut cost on a long system prompt I reuse?" (answer: prompt caching).

Next: [Module 11 — Org & Personal Skills](11-org-and-personal.md)
