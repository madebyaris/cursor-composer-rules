# Composer-era Cursor Rules

A Cursor rule pack that encodes how a senior engineer thinks: **evidence over assumption, surgical edits, honest uncertainty, root-cause debugging, structured research, and sane orchestration** (subagents, plan mode, effort calibration).

Stack-agnostic. Two always-on rules form the operating spine; the rest load on demand by description match. No model identity claims — Cursor's lineup changes; the principles don't.

Tuned for **Composer 2.5-era** agents: async subagents, plan mode, background work, and independent verification — without duplicating Cursor's built-in tool docs.

## Quick start

Repository: **`madebyaris/cursor-composer-rules`** — clone URL:

```bash
git clone https://github.com/madebyaris/cursor-composer-rules.git

# Replace the destination with your actual app directory
cp -r cursor-composer-rules/.cursor path/to/your-app/.cursor
```

**Merge carefully** if you already have `.cursor/rules` or `.cursor/agents`:

- Duplicate **always-on** rules hurt quality — keep one core + one verification spine.
- If you already have a `verifier` subagent, merge prompts or rename to avoid conflicting delegation.
- Custom subagents in this pack are examples; adapt descriptions to your team.

## What's new (2.5 refresh)

| Addition | Purpose |
| --- | --- |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | When to delegate vs inline; plan mode; foreground/background subagents; long-running checkpoints |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Effort calibration tier; sharper plan vs act |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Explore/Bash/Browser subagents, background work, sandbox **blocked** handling |
| [`.cursor/agents/verifier.md`](.cursor/agents/verifier.md) | Skeptical post-work check before **verified** |
| [`.cursor/agents/debugger.md`](.cursor/agents/debugger.md) | Isolated root-cause pass (repro first in parent) |

Optional: extend the pack with [Cursor Marketplace](https://cursor.com/marketplace) plugins (skills, MCP, hooks) — not required for the core behavior contract.

## What the pack teaches

### Always-on (the operating spine)

| File | Purpose |
| --- | --- |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Principles: evidence-first, read before edit, smallest diff, effort calibration, plan vs act |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Proof contract: `verified` / `implemented but unverified` / `blocked`; independent verification |

### Requestable (loaded by description match)

| File | Use for |
| --- | --- |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | Subagents, plan mode, parallel workstreams, long-running tasks |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | Writing or modifying code: surgical edits, convention matching, no fabricated APIs |
| [`composer-debugging.mdc`](.cursor/rules/composer-debugging.mdc) | Broken or unexpected behavior: reproduce, trace, root cause |
| [`composer-fullstack-delivery.mdc`](.cursor/rules/composer-fullstack-delivery.mdc) | Multi-layer changes: seams, vertical slice, failure modes |
| [`composer-deep-research.mdc`](.cursor/rules/composer-deep-research.mdc) | Audits, comparisons, benchmarks: primaries, claim ledger, contradictions |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Tools: parallel reads, MCP schemas, subagents, no fabricated output |
| [`clarify-first.mdc`](.cursor/rules/clarify-first.mdc) | When to ask (after inspect); plan-mode exception |

### Example subagents

| File | Use for |
| --- | --- |
| [`verifier.md`](.cursor/agents/verifier.md) | After "done" claims — run checks, report verified vs gaps (`readonly`) |
| [`debugger.md`](.cursor/agents/debugger.md) | Isolated debug when repro is known — root cause + minimal fix |

Built-in Explore, Bash, and Browser subagents need no config; orchestration rule explains when Cursor uses them.

Invoke explicitly: `/verifier confirm tests pass`, or ask naturally: "use the debugger subagent on this failure."

### Skills (long-form workflows)

| Path | Purpose |
| --- | --- |
| [`.cursor/skills/deep-research/SKILL.md`](.cursor/skills/deep-research/SKILL.md) | Multi-pass research with claim ledger and contradiction log |
| [`.cursor/skills/deep-research/reference.md`](.cursor/skills/deep-research/reference.md) | Compact checklist version |

## Design principles

- **Behavior contracts, not model identity.** Rules don't assert "Composer = X model". Cursor's model lineup changes; the principles are durable.
- **Tiny always-on core.** Always-on prompts cost context forever. Orchestration, tools, and specialists stay requestable or in `.cursor/agents/`.
- **One concern per rule.** Orchestration is separate from debugging is separate from research. Activate what the task needs.
- **Concrete over abstract.** Rules show good vs bad with examples, not adjectives.
- **Honest tooling.** Never fabricate output; never mark **verified** from a subagent summary alone.
- **Agents execute, rules govern.** Verifier runs checks; verification rule defines when and how to label results.

## Extending

Add stack-specific rules as new `.mdc` files with `globs`:

```text
.cursor/rules/typescript.mdc        # globs: **/*.{ts,tsx}
.cursor/rules/python.mdc            # globs: **/*.py
.cursor/rules/rust.mdc              # globs: **/*.rs
```

Add focused subagents under `.cursor/agents/` with specific `description` fields — avoid dozens of vague helpers ([Cursor subagent docs](https://cursor.com/docs/agent/subagents)).

Keep extensions short. Don't duplicate core or verification — link to them.

## Layout

```text
.cursor/
  agents/
    verifier.md                      # example subagent
    debugger.md                      # example subagent
  rules/
    composer-core.mdc                # always on
    composer-verification.mdc        # always on
    composer-orchestration.mdc       # requestable
    composer-coding-excellence.mdc   # requestable
    composer-debugging.mdc           # requestable
    composer-deep-research.mdc       # requestable
    composer-fullstack-delivery.mdc  # requestable
    cursor-tools-discipline.mdc      # requestable
    clarify-first.mdc                # requestable
  skills/
    deep-research/
      SKILL.md
      reference.md
README.md
LICENSE
.gitignore
```

## License

MIT — see [LICENSE](LICENSE).
