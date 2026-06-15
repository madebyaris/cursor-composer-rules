<div align="center">

# 🎼 Composer-era Cursor Rules

**How a senior engineer thinks — encoded for Cursor agents.**

Evidence over assumption · surgical edits · honest uncertainty · root-cause debugging · structured research · sane orchestration

<br />

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Stack](https://img.shields.io/badge/Stack-agnostic-6366f1?style=for-the-badge)]()
[![Cursor](https://img.shields.io/badge/Cursor-Rules_&_Skills-0ea5e9?style=for-the-badge)](https://cursor.com)
[![Composer 2.5](https://img.shields.io/badge/Tuned_for-Composer_2.5-f97316?style=for-the-badge)]()

<br />

[Quick start](#-quick-start) · [What's new](#-whats-new-25-refresh) · [Rules](#-what-the-pack-teaches) · [Design](#-design-principles) · [Extend](#-extending)

</div>

---

## ✨ At a glance

| | Principle | What you get |
| --- | --- | --- |
| 🔍 | **Evidence first** | Read code, run commands, cite paths — never guess |
| 🤔 | **Reason, then re-check** | Infer the real ask; challenge the plan before acting; push back honestly |
| ✂️ | **Surgical edits** | Match project style; smallest diff that proves the next step |
| 📋 | **Rich plans** | Structured plan template with options, inventory, verification matrix |
| 🛡️ | **Git safety** | Never `git push` unprompted — commits ≠ remote updates |
| 🧠 | **Senior practices** | Version-pinned guidance from official docs, not stale training data |
| ✅ | **Proof contract** | `verified` / `implemented but unverified` / `blocked` — no fake "done" |

Stack-agnostic. **Two always-on rules** form the operating spine; everything else loads on demand by description match. No model identity claims — Cursor's lineup changes; the principles don't.

```text
┌─────────────────────────────────────────────────────────────┐
│  ALWAYS ON          │  REQUESTABLE ON TASK                  │
│  composer-core      │  reasoning · orchestration · coding   │
│  composer-verify    │  debugging · research · delivery      │
│                     │  tools · clarify                      │
├─────────────────────┼───────────────────────────────────────┤
│  AGENTS             │  SKILLS                               │
│  verifier · debugger│  deep-research · senior-practices     │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick start

Repository: **`madebyaris/cursor-composer-rules`**

```bash
git clone https://github.com/madebyaris/cursor-composer-rules.git

# Replace the destination with your actual app directory
cp -r cursor-composer-rules/.cursor path/to/your-app/.cursor
```

> **⚠️ Merge carefully** if you already have `.cursor/rules` or `.cursor/agents`:
>
> - Duplicate **always-on** rules hurt quality — keep one core + one verification spine.
> - If you already have a `verifier` subagent, merge prompts or rename to avoid conflicting delegation.
> - Custom subagents in this pack are examples; adapt descriptions to your team.

---

## 🆕 What's new (2.5 refresh)

| Addition | Purpose |
| --- | --- |
| [`composer-reasoning.mdc`](.cursor/rules/composer-reasoning.mdc) | **Senior reasoning + metacognition** — infer the real ask, reason then re-evaluate, principal judgment (tradeoffs, reversibility), honest pushback |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | **Intent + re-evaluate** principles; effort calibration tier; sharper plan vs act; **git remote safety** (never push unprompted) |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | When to delegate vs inline; **structured plan template**; foreground/background subagents; long-running checkpoints |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | **Style governance** — match vs improve decision tree; no drive-by refactors |
| [`composer-senior-practices.mdc`](.cursor/rules/composer-senior-practices.mdc) | Version-pinned best practices from primary docs + corroborated guidance |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Explore/Bash/Browser subagents, background work, sandbox **blocked** handling; **git command allow/deny** |
| [`.cursor/skills/senior-practices/`](.cursor/skills/senior-practices/SKILL.md) | Workflow to anchor framework guidance to repo versions and credible sources |
| [`.cursor/agents/verifier.md`](.cursor/agents/verifier.md) | Skeptical post-work check before **verified** |
| [`.cursor/agents/debugger.md`](.cursor/agents/debugger.md) | Isolated root-cause pass (repro first in parent) |

Optional: extend the pack with [Cursor Marketplace](https://cursor.com/marketplace) plugins (skills, MCP, hooks) — not required for the core behavior contract.

---

## 📚 What the pack teaches

### 🔒 Always-on (the operating spine)

| File | Purpose |
| --- | --- |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Principles: evidence-first, read before edit, smallest diff, effort calibration, plan vs act |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Proof contract: `verified` / `implemented but unverified` / `blocked`; independent verification |

### 📎 Requestable (loaded by description match)

| File | Use for |
| --- | --- |
| [`composer-reasoning.mdc`](.cursor/rules/composer-reasoning.mdc) | Ambiguous, high-stakes, or architectural work: infer real intent, reason then re-evaluate, weigh tradeoffs, push back honestly |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | Subagents, plan mode, parallel workstreams, long-running tasks |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | Writing or modifying code: surgical edits, convention matching, style governance, no fabricated APIs |
| [`composer-senior-practices.mdc`](.cursor/rules/composer-senior-practices.mdc) | Version-pinned framework/coding guidance from primary docs and corroborated sources |
| [`composer-debugging.mdc`](.cursor/rules/composer-debugging.mdc) | Broken or unexpected behavior: reproduce, trace, root cause |
| [`composer-fullstack-delivery.mdc`](.cursor/rules/composer-fullstack-delivery.mdc) | Multi-layer changes: seams, vertical slice, failure modes |
| [`composer-deep-research.mdc`](.cursor/rules/composer-deep-research.mdc) | Audits, comparisons, benchmarks: primaries, claim ledger, contradictions |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Tools: parallel reads, MCP schemas, subagents, no fabricated output |
| [`clarify-first.mdc`](.cursor/rules/clarify-first.mdc) | When to ask (after inspect); plan-mode exception |

### 🤖 Example subagents

| File | Use for |
| --- | --- |
| [`verifier.md`](.cursor/agents/verifier.md) | After "done" claims — run checks, report verified vs gaps (`readonly`) |
| [`debugger.md`](.cursor/agents/debugger.md) | Isolated debug when repro is known — root cause + minimal fix |

Built-in Explore, Bash, and Browser subagents need no config; orchestration rule explains when Cursor uses them.

Invoke explicitly: `/verifier confirm tests pass`, or ask naturally: *"use the debugger subagent on this failure."*

### 🛠 Skills (long-form workflows)

| Path | Purpose |
| --- | --- |
| [`.cursor/skills/deep-research/SKILL.md`](.cursor/skills/deep-research/SKILL.md) | Multi-pass research with claim ledger and contradiction log |
| [`.cursor/skills/deep-research/reference.md`](.cursor/skills/deep-research/reference.md) | Compact checklist version |
| [`.cursor/skills/senior-practices/SKILL.md`](.cursor/skills/senior-practices/SKILL.md) | Version-pinned best practices: inventory → T1 anchor → reconcile with repo |
| [`.cursor/skills/senior-practices/reference.md`](.cursor/skills/senior-practices/reference.md) | Compact checklist version |

---

## 🧭 Design principles

| | Principle |
| --- | --- |
| 🎯 | **Behavior contracts, not model identity.** Rules don't assert "Composer = X model". Cursor's model lineup changes; the principles are durable. |
| 🤔 | **Intent + metacognition.** Read for the real outcome, not the literal words; form an approach, then re-evaluate it before acting. Depth scales with blast radius. |
| 🪶 | **Tiny always-on core.** Always-on prompts cost context forever. Orchestration, tools, and specialists stay requestable or in `.cursor/agents/`. |
| 🧩 | **One concern per rule.** Orchestration is separate from debugging is separate from research. Activate what the task needs. |
| 🔧 | **Concrete over abstract.** Rules show good vs bad with examples, not adjectives. |
| 🪞 | **Honest tooling.** Never fabricate output; never mark **verified** from a subagent summary alone. |
| 🚫 | **Git remote safety.** Agents must not `git push` unless the user explicitly asks in the current turn. For hard enforcement, add your own [`beforeShellExecution` hook](https://cursor.com/docs/agent/hooks) — not shipped in this pack. |
| ⚖️ | **Agents execute, rules govern.** Verifier runs checks; verification rule defines when and how to label results. |

---

## 🔧 Extending

Add stack-specific rules as new `.mdc` files with `globs`:

```text
.cursor/rules/typescript.mdc        # globs: **/*.{ts,tsx}
.cursor/rules/python.mdc            # globs: **/*.py
.cursor/rules/rust.mdc              # globs: **/*.rs
```

Add focused subagents under `.cursor/agents/` with specific `description` fields — avoid dozens of vague helpers ([Cursor subagent docs](https://cursor.com/docs/agent/subagents)).

Keep extensions short. Don't duplicate core or verification — link to them.

---

## 📁 Layout

```text
.cursor/
  agents/
    verifier.md                      # example subagent
    debugger.md                      # example subagent
  rules/
    composer-core.mdc                # always on
    composer-verification.mdc        # always on
    composer-reasoning.mdc           # requestable
    composer-orchestration.mdc       # requestable
    composer-coding-excellence.mdc   # requestable
    composer-senior-practices.mdc    # requestable
    composer-debugging.mdc           # requestable
    composer-deep-research.mdc       # requestable
    composer-fullstack-delivery.mdc  # requestable
    cursor-tools-discipline.mdc      # requestable
    clarify-first.mdc                # requestable
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

## 📄 License

MIT — see [LICENSE](LICENSE)

<br />

**Made for teams who want agents that ship evidence, not vibes.**

</div>
