<div align="center">

# Composer-era Cursor Rules

**Build and continue apps — with intent, evidence, and an honest handoff.**

Continue-by-default · confusion-weight asks · vertical slices · proof labels · no fake "done"

<br />

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Stack](https://img.shields.io/badge/Stack-agnostic-6366f1?style=for-the-badge)]()
[![Cursor](https://img.shields.io/badge/Cursor-Rules_&_Skills-0ea5e9?style=for-the-badge)](https://cursor.com)
[![Composer 2.5](https://img.shields.io/badge/Tuned_for-Composer_2.5-f97316?style=for-the-badge)]()
[![Grok 4.5](https://img.shields.io/badge/Also_for-Cursor_Grok_4.5-000000?style=for-the-badge)]()

<br />

[Quick start](#-quick-start) · [What's new](#-whats-new-build--continue-reorient) · [Rules](#-what-the-pack-teaches) · [Design](#-design-principles) · [Extend](#-extending)

</div>

---

## At a glance

| | Principle | What you get |
| --- | --- | --- |
| Continue | **Continue-by-default** | Follow-ups refine open work; prefer existing seams; leave a handoff (done / next / assumptions) |
| Intent | **Infer-and-act** | Read the outcome, not just the words; state assumptions inline and keep building |
| Ask | **Confusion-weight gate** | Ask only when high (irreversible, contract-changing, contradictory, no repo signal) |
| Slice | **Vertical slice** | One path end-to-end before widening |
| Proof | **Evidence + labels** | `verified` / `implemented but unverified` / `blocked` — no fake "done" |
| Safety | **Git remote safety** | Never `git push` unprompted — commits ≠ remote updates |

Stack-agnostic. Tuned for **Composer 2.5** and **Cursor Grok 4.5** — same builder spine either way. **Two always-on rules** form that spine; everything else loads on demand. Research and senior-practices stay available as **edge tools**, not co-equal pillars. The principles are durable even as Cursor's lineup changes.

```text
┌─────────────────────────────────────────────────────────────┐
│  ALWAYS ON          │  REQUESTABLE ON TASK                  │
│  composer-core      │  clarify · reasoning · delivery       │
│  composer-verify    │  orchestration · coding · debugging   │
│                     │  tools · (edge) research · practices  │
├─────────────────────┼───────────────────────────────────────┤
│  AGENTS             │  SKILLS                               │
│  verifier · debugger│  deep-research · senior-practices     │
└─────────────────────────────────────────────────────────────┘
```

---

## Quick start

Repository: **`madebyaris/cursor-composer-rules`**

```bash
git clone https://github.com/madebyaris/cursor-composer-rules.git

# Replace the destination with your actual app directory
cp -r cursor-composer-rules/.cursor path/to/your-app/.cursor
```

> **Merge carefully** if you already have `.cursor/rules` or `.cursor/agents`:
>
> - Duplicate **always-on** rules hurt quality — keep one core + one verification spine.
> - If you already have a `verifier` subagent, merge prompts or rename to avoid conflicting delegation.
> - Custom subagents in this pack are examples; adapt descriptions to your team.

---

## What's new (build + continue reorient)

| Change | Purpose |
| --- | --- |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | **Builder spine** — intent modes, confusion-weight ask gate, continue-the-app + handoff, vertical slice; shorter always-on |
| [`clarify-first.mdc`](.cursor/rules/clarify-first.mdc) | **Infer-and-act** ask policy — ask only on high confusion weight |
| [`composer-reasoning.mdc`](.cursor/rules/composer-reasoning.mdc) | **Judgment only** — tradeoffs, one-way doors, pushback (basic intent moved to core) |
| [`composer-fullstack-delivery.mdc`](.cursor/rules/composer-fullstack-delivery.mdc) | **Build/continue playbook** — seams → slice → failure modes → explicit handoff |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Unchanged proof contract — still the second always-on |

Optional: extend with [Cursor Marketplace](https://cursor.com/marketplace) plugins — not required for the core behavior contract.

---

## What the pack teaches

### Always-on (the builder spine)

| File | Purpose |
| --- | --- |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Continue-by-default, intent + modes, confusion weight, evidence, slice, handoff |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Proof contract: `verified` / `implemented but unverified` / `blocked` |

### Requestable (loaded by description match)

| File | Use for |
| --- | --- |
| [`clarify-first.mdc`](.cursor/rules/clarify-first.mdc) | When and how to ask — high confusion weight only |
| [`composer-reasoning.mdc`](.cursor/rules/composer-reasoning.mdc) | Architectural / multi-option work: tradeoffs, one-way doors, honest pushback |
| [`composer-fullstack-delivery.mdc`](.cursor/rules/composer-fullstack-delivery.mdc) | Multi-layer feature build or continue: seams, slice, handoff |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | Subagents, plan mode, parallel workstreams, long-running tasks |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | Writing code: surgical edits, convention matching, no fabricated APIs |
| [`composer-debugging.mdc`](.cursor/rules/composer-debugging.mdc) | Broken behavior: reproduce, trace, root cause |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Tools: parallel reads, MCP schemas, subagents, no fabricated output |
| [`composer-senior-practices.mdc`](.cursor/rules/composer-senior-practices.mdc) | **Edge:** version-pinned guidance when the stack is unfamiliar |
| [`composer-deep-research.mdc`](.cursor/rules/composer-deep-research.mdc) | **Edge:** audits, comparisons, benchmarks — not the default build path |

### Example subagents

| File | Use for |
| --- | --- |
| [`verifier.md`](.cursor/agents/verifier.md) | After "done" claims — run checks, report verified vs gaps (`readonly`) |
| [`debugger.md`](.cursor/agents/debugger.md) | Isolated debug when repro is known — root cause + minimal fix |

Built-in Explore, Bash, and Browser subagents need no config; orchestration rule explains when Cursor uses them.

Invoke explicitly: `/verifier confirm tests pass`, or ask naturally: *"use the debugger subagent on this failure."*

### Skills (long-form workflows)

| Path | Purpose |
| --- | --- |
| [`.cursor/skills/deep-research/SKILL.md`](.cursor/skills/deep-research/SKILL.md) | Multi-pass research with claim ledger and contradiction log |
| [`.cursor/skills/deep-research/reference.md`](.cursor/skills/deep-research/reference.md) | Compact checklist version |
| [`.cursor/skills/senior-practices/SKILL.md`](.cursor/skills/senior-practices/SKILL.md) | Version-pinned best practices: inventory → T1 anchor → reconcile with repo |
| [`.cursor/skills/senior-practices/reference.md`](.cursor/skills/senior-practices/reference.md) | Compact checklist version |

---

## Design principles

| | Principle |
| --- | --- |
| Product | **Build and continue.** Agents ship slices and leave handoffs — not greenfield every turn. |
| Intent | **Infer-and-act with a confusion-weight ask gate.** Low/medium → assume and proceed; high → one decisive question. |
| Proof | **Evidence before write.** Intent is not a license to invent APIs. Same verification labels as before. |
| Context | **Tiny always-on core.** Orchestration, judgment, delivery, and research stay requestable. |
| Focus | **One concern per rule.** Activate what the task needs. |
| Honesty | **Never fabricate output;** never mark **verified** from a subagent summary alone. |
| Git | **Never push unprompted.** For hard enforcement, add your own [`beforeShellExecution` hook](https://cursor.com/docs/agent/hooks) — not shipped in this pack. |
| Roles | **Agents execute, rules govern.** Verifier runs checks; verification rule defines labels. |

---

## Extending

Add stack-specific rules as new `.mdc` files with `globs`:

```text
.cursor/rules/typescript.mdc        # globs: **/*.{ts,tsx}
.cursor/rules/python.mdc            # globs: **/*.py
.cursor/rules/rust.mdc              # globs: **/*.rs
```

Add focused subagents under `.cursor/agents/` with specific `description` fields — avoid dozens of vague helpers ([Cursor subagent docs](https://cursor.com/docs/agent/subagents)).

Keep extensions short. Don't duplicate core or verification — link to them.

---

## Layout

```text
.cursor/
  agents/
    verifier.md                      # example subagent
    debugger.md                      # example subagent
  rules/
    composer-core.mdc                # always on — builder spine
    composer-verification.mdc        # always on — proof contract
    clarify-first.mdc                # requestable — ask policy
    composer-reasoning.mdc           # requestable — judgment
    composer-fullstack-delivery.mdc  # requestable — build/continue
    composer-orchestration.mdc       # requestable
    composer-coding-excellence.mdc   # requestable
    composer-senior-practices.mdc    # requestable (edge)
    composer-debugging.mdc           # requestable
    composer-deep-research.mdc       # requestable (edge)
    cursor-tools-discipline.mdc      # requestable
  skills/
    deep-research/
      SKILL.md
      reference.md
    senior-practices/
      SKILL.md
      reference.md
README.md
LICENSE
.gitignore
```

---

<div align="center">

## License

MIT — see [LICENSE](LICENSE)

<br />

**Made for teams who want agents that ship the next slice — and know when to ask.**

</div>
