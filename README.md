<div align="center">

# Composer-era Cursor Rules

**Change code and continue apps — with intent, evidence, and an honest handoff.**

Continue-by-default · fast code path · high effort on hard code · proof labels · no fake "done"

<br />

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Stack](https://img.shields.io/badge/Stack-agnostic-6366f1?style=for-the-badge)]()
[![Cursor](https://img.shields.io/badge/Cursor-Rules_&_Skills-0ea5e9?style=for-the-badge)](https://cursor.com)
[![Grok 4.6](https://img.shields.io/badge/Tuned_for-Cursor_Grok_4.6-000000?style=for-the-badge)]()
[![Grok 4.7](https://img.shields.io/badge/Also_for-Grok_4.7-111827?style=for-the-badge)]()
[![Grok 4.5](https://img.shields.io/badge/Also_for-Grok_4.5-1f2937?style=for-the-badge)]()
[![Composer 2.5](https://img.shields.io/badge/Also_for-Composer_2.5-f97316?style=for-the-badge)]()

<br />

[Quick start](#-quick-start) · [What's new](#-whats-new) · [Tuned for Grok](#tuned-for-grok-46-and-47) · [Rules](#-what-the-pack-teaches) · [Design](#-design-principles) · [Extend](#-extending)

</div>

---

## At a glance

| | Principle | What you get |
| --- | --- | --- |
| Continue | **Continue-by-default** | Follow-ups refine open work; a local code change stays on the fast path |
| Intent | **Infer-and-act** | Read the outcome, not just the words; state assumptions inline and keep building |
| Ask | **Confusion-weight gate** | Ask only when high (irreversible, contract-changing, contradictory, no repo signal) |
| Speed | **Two speeds** | Fast path for a symbol, known bug, or one module; high effort for cross-layer, unclear bugs, and contracts |
| Slice | **Demoable vertical slice** | Product surfaces (UI, API, CLI) still ship one path the user can exercise |
| Proof | **Narrowest check** | Scoped test by default; `verified` / `implemented but unverified` / `blocked` |
| Closeout | **Standalone final message** | User never saw the tool calls — lead with outcome + proof label |
| Safety | **Git remote safety** | Never `git push` unprompted — commits ≠ remote updates |

Stack-agnostic. **Primary tune: Cursor Grok 4.6**, same contract on **Grok 4.7**, Grok 4.5, and Composer 2.5 ([Grok 4.6 announcement](https://cursor.com/blog/grok-4-6)). The common turn is a code change in the language already in the repo. **Two always-on rules** form the spine; everything else loads on demand. Research and senior-practices stay **edge tools**, not co-equal pillars. Rule bodies stay model-agnostic so you can copy the pack into any Cursor agent repo.

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

## What's new

| Change | Purpose |
| --- | --- |
| Programming-first | The common turn is a **code change**. Product slices still use the demoable loop |
| Two speeds | **Fast** for a symbol, known bug, or one module. **High effort** for cross-layer work, unclear bugs, contracts, and missing idioms |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Fast closeout is outcome + command + label. Product closeout keeps Run / Wired (`Run: npm test` is still BAD on a screen) |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Default proof is the **narrowest** project test (`go test -run`, `pytest` node, `cargo test`, vitest/jest path) |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | **Language of the file** — match that dialect; one primary lookup when the idiom is absent |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | Short code plan (summary, files, approach, checks, assumptions). Long plan stays for architecture |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Full harness: in (message, latest result), one action, out (diff, check, closeout). Same error twice stops |
| Branding | **Grok 4.6** primary; **Grok 4.7**, Grok 4.5, and Composer 2.5 share the contract. Model names stay in this README |

Optional: extend with [Cursor Marketplace](https://cursor.com/marketplace) plugins — not required for the core behavior contract.

---

## Tuned for Grok 4.6 and 4.7

[Grok 4.6](https://cursor.com/blog/grok-4-6) is a long-running coding model, and high effort is its default. **Grok 4.7** uses this same spine. Grok 4.5 and Composer 2.5 stay on the contract. The pack points that effort at the code: find the symbol, match the file, run the narrowest check. A longer reply is not higher effort.

What this pack **leans on**:

- Two speeds (fast code path, high effort when the change is hard)
- Structured procedures (modes, weight table, proof labels)
- A tool harness: latest result in, one action, diff and check out, stop on a repeated error
- Explicit uncertainty (`verified` / hypothesis / unknown)
- The language already in the file
- A **demoable** path when the user is shipping a screen, endpoint, or CLI

What it **restrains**:

- High effort spent on narration, drive-by refactors, or research for "add this function"
- Confident tone without a matching check → proof labels
- Asking when a repo default already exists → confusion-weight gate
- Tool work invisible to the user → standalone closeout
- Spawning subagents for a single-file edit
- Agreeing to a weak design to preserve rapport → reasoning pushback
- A full product-slice essay on a function or known bug

Always-on rules never say “You are Grok” — identity lives here in the README so the pack stays portable.

---

## What the pack teaches

### Always-on (the builder spine)

| File | Purpose |
| --- | --- |
| [`composer-core.mdc`](.cursor/rules/composer-core.mdc) | Two speeds: fast code path by default; product slice, slice-1 floor, and Run/Wired when the surface is user-visible |
| [`composer-verification.mdc`](.cursor/rules/composer-verification.mdc) | Proof contract: scoped test by default; surface proof when user-visible; `verified` / `implemented but unverified` / `blocked` |

### Requestable (loaded by description match)

| File | Use for |
| --- | --- |
| [`clarify-first.mdc`](.cursor/rules/clarify-first.mdc) | When and how to ask — high confusion weight only |
| [`composer-reasoning.mdc`](.cursor/rules/composer-reasoning.mdc) | Architectural / multi-option work: tradeoffs, one-way doors, honest pushback |
| [`composer-fullstack-delivery.mdc`](.cursor/rules/composer-fullstack-delivery.mdc) | New screen, feature, endpoint, or multi-layer slice: seams, demoable path, failure modes |
| [`composer-orchestration.mdc`](.cursor/rules/composer-orchestration.mdc) | Subagents, plan mode (short code plan vs architecture plan), parallel workstreams |
| [`composer-coding-excellence.mdc`](.cursor/rules/composer-coding-excellence.mdc) | Any language: surgical edits, language of the file, no fabricated APIs |
| [`composer-debugging.mdc`](.cursor/rules/composer-debugging.mdc) | Known repro stays on the fast path; unclear or flaky failures get the full trace |
| [`cursor-tools-discipline.mdc`](.cursor/rules/cursor-tools-discipline.mdc) | Tool harness: what may enter a turn, which Cursor tool runs, what may leave, and the stop when the same error returns twice |
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
| Product | **Code first, then continue.** A local change is the common turn. A screen, endpoint, or CLI still ships a demoable slice and a Run/Wired handoff. |
| Intent | **Infer-and-act with a confusion-weight ask gate.** Low/medium → assume and proceed; high → one decisive question. |
| Proof | **Evidence before write.** Intent is not a license to invent APIs. Same verification labels as before. |
| Closeout | **Standalone final message.** Fast path: outcome, command, label. Product slice: add Run/Wired so the next turn can resume. |
| Context | **Tiny always-on core.** The common turn is a code change. The tool harness, orchestration, judgment, and research stay requestable. |
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
    composer-core.mdc                # always on — two speeds (fast code path + product slice)
    composer-verification.mdc        # always on — proof contract
    clarify-first.mdc                # requestable — ask policy
    composer-reasoning.mdc           # requestable — judgment
    composer-fullstack-delivery.mdc  # requestable — build/continue
    composer-orchestration.mdc       # requestable
    composer-coding-excellence.mdc   # requestable
    composer-senior-practices.mdc    # requestable (edge)
    composer-debugging.mdc           # requestable
    composer-deep-research.mdc       # requestable (edge)
    cursor-tools-discipline.mdc      # requestable — tool harness (in / act / out / stop)
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

**Made for teams who want agents that change the code — and know when to ask.**

</div>
