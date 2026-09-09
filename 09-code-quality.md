# Module 9 — Code Quality & Security

Skills that review and improve code. These are the ones you'll reach for most as a
developer.

## Skills covered

| Skill | Looks for | Applies fixes? |
|-------|-----------|----------------|
| `code-review` | Correctness bugs **and** cleanup (reuse, simplification, efficiency) | optional (`--fix`) |
| `simplify` | Cleanup only — reuse, simplification, efficiency, altitude | yes |
| `security-review` | Security vulnerabilities in pending changes | reports findings |

## `code-review` — the workhorse

Review your current diff, a PR, a branch, or a path:

```
/code-review
/code-review 1234          # a PR number
/code-review high          # effort level
/code-review --fix         # apply the findings to your working tree
/code-review --comment     # post findings as inline PR comments
```

**Effort levels** trade off breadth vs. noise:

- `low` / `medium` — fewer, high-confidence findings
- `high` → `max` — broader coverage, may include uncertain findings

With no level, it reuses the last one you used. Findings are verified before being
reported, so you get signal over noise.

> **You:** /code-review high --comment

reviews thoroughly and leaves inline comments on the PR.

## `simplify` — cleanup without bug-hunting

When the code *works* but feels messy:

> **You:** /simplify

It hunts for duplication, over-complication, inefficiency, and wrong "altitude" (code
doing too much or at the wrong layer), then **applies** the cleanups. It does **not** look
for bugs — use `code-review` for that.

### `code-review` vs `simplify`

- Want to catch **bugs**? → `code-review`
- Just want it **tidier**? → `simplify`
- Want both? → `code-review` (it covers cleanup too), or run both.

## `security-review` — before you ship

> **You:** /security-review

Reviews the pending changes on your branch specifically for security issues — injection,
auth mistakes, unsafe data handling, secrets. Run it before opening a PR on anything
sensitive.

## A good pre-PR ritual

1. `/simplify` — tidy the diff.
2. `/code-review high` — catch bugs.
3. `/security-review` — check for vulnerabilities.
4. Open the PR.

## Try it

1. Make a small, slightly-messy change in a repo.
2. Run `/code-review` and read the findings.
3. Run `/simplify` and diff what it changed.
4. Run `/security-review` on a change that touches input handling.

Next: [Module 10 — The Claude API Reference Skill](10-api-reference.md)
