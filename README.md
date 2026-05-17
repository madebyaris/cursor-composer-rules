# Composer Cursor Rules

A Cursor rule pack that encodes how a senior engineer thinks: **evidence over assumption, surgical edits, honest uncertainty, root-cause debugging, and structured research.**

Stack-agnostic. Two always-on rules form the operating spine; the rest are loaded on demand by description match. No vendor lock-in, no model identity claims — Cursor's model lineup changes, the principles don't.

## Quick start

Repository: **`madebyaris/cursor-composer-rules`** — clone URL:

```bash
git clone https://github.com/madebyaris/cursor-composer-rules.git

# Replace the destination with your actual app directory
cp -r cursor-composer-rules/.cursor path/to/your-app/.cursor
```

If your project already has `.cursor/rules`, merge thoughtfully — duplicate or contradictory always-on prompts hurt quality.

## What the pack teaches

### Always-on (the operating spine)

| File | Purpose |
| --- | --- |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Operating principles: evidence-first, read before edit, smallest diff, honest uncertainty, no scope creep |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Proof contract: `verified` / `implemented but unverified` / `blocked`, proportional evidence per change type |

### Requestable (loaded by description match)

| File | Use for |
| --- | --- |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | Writing or modifying code: surgical edits, convention matching, no slop comments, no fabricated APIs, refactor caution |
| [`composer-debugging.mdc`](.cursor/rules/composer-debugging.mdc) | Anything broken or unexpected: reproduce, read full error, trace data flow, test cheapest hypothesis, fix root cause |
| [`composer-fullstack-delivery.mdc`](.cursor/rules/composer-fullstack-delivery.mdc) | Multi-layer changes: freeze seams, ship one vertical slice, treat failure modes as first-class |
| [`composer-deep-research.mdc`](.cursor/rules/composer-deep-research.mdc) | Investigation, comparison, audit, benchmarking: primaries first, claim ledger, contradiction log, confidence labels |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Tool use: parallel reads, schema-first MCP, right-tool-for-the-job, never fabricate output |
| [`clarify-first.mdc`](.cursor/rules/clarify-first.mdc) | When to ask: only after inspecting, only when the answer changes the design, never as a stalling tactic |

### Skills (long-form workflows)

| Path | Purpose |
| --- | --- |
| [`.cursor/skills/deep-research/SKILL.md`](.cursor/skills/deep-research/SKILL.md) | Multi-pass research workflow with claim ledger and contradiction log |
| [`.cursor/skills/deep-research/reference.md`](.cursor/skills/deep-research/reference.md) | Compact checklist version of the same |

## Design principles

- **Behavior contracts, not model identity.** Rules don't assert "Composer = X model". Cursor's model lineup changes; the principles are durable.
- **Tiny always-on core.** Always-on prompts cost context forever. Anything not universal lives behind a description match or a skill.
- **One concern per rule.** Coding-craft is separate from debugging is separate from research. Activate what the task needs.
- **Concrete over abstract.** Rules show the difference between good and bad with examples, not just adjectives.
- **Honest tooling.** Never fabricate tool output, never claim verification you didn't perform, never loop on a failed call hoping for a different result.

## Extending

Add stack-specific rules as new `.mdc` files with `globs`:

```text
.cursor/rules/typescript.mdc        # globs: **/*.{ts,tsx}
.cursor/rules/python.mdc            # globs: **/*.py
.cursor/rules/rust.mdc              # globs: **/*.rs
```

Keep them short. Don't duplicate the core or verification policies — link to them.

## Layout

```text
.cursor/
  rules/
    composer-core.mdc                  # always on
    composer-verification.mdc          # always on
    composer-coding-excellence.mdc     # requestable
    composer-debugging.mdc             # requestable
    composer-deep-research.mdc         # requestable
    composer-fullstack-delivery.mdc    # requestable
    cursor-tools-discipline.mdc        # requestable
    clarify-first.mdc                  # requestable
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
