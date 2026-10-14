# Session Wind-Down

## Goal

Leave a short, durable record of this chat so that the next session has context to keep the work going — even in a new chat or on a different device.

The record lives in existing living docs (mainly `Project Status.md`). Do not create a separate session log.

---

## How to invoke

**End of session:** ask the agent to wind down using this doc, e.g.

> Wind down this session per `Developer Documentation/Reference/Session Wind-Down.md`.

**Start of next session:**

> Continue from living docs only (ignore prior chat). Read `Developer Documentation/Project Status.md` (Now + Agents), then any linked plan/spec and Backlog rows. Recommend what to do next.

---

## What to record

Capture only what the next agent needs to pick up cleanly. Prefer a few concrete lines over a transcript.

**Always useful**

- What was in flight (Backlog ID(s) if any)
- Where things stand (done / mid-flight / paused)
- The single best next action
- Links to the plan, spec, or key files if not obvious from Project Status

**Add when it matters**

- Open decisions or blockers the next session will hit
- Intentional pauses ("stopped here because…")
- Anything that would be wrong if the next agent only read an outdated Project Status row

Skip narrative, debate history, and "we also discussed…" unless it changes what to do next.

---

## Where to write it

1. **Project Status** — primary handoff surface  
   - Refresh **Now** for work this session touched. In **Notes**, when useful, include a brief "Last worked:" line (state, decision, or stop point).  
   - Update **this** agent's **Agents** row: IDs, building / blocked / idle, next step in a sentence or two. If this session's role has no row yet, add one.  
   - Do **not** add Next or Later sections to Project Status.  
   - Set **Last verified** to today.

2. **Backlog** — update only if Status, Priority, or Notes no longer match reality.

3. **Active plan or spec** — only if phases, status, or "next" notes need to match what Project Status says.

4. **Agent Handoffs** — only when another *role* must act (use the handoff doc for that pair). Not a dump of this chat.

Ship / pause / archive workflows stay with those docs (see the Developer Documentation README); wind-down just makes Project Status and related docs true enough to resume.

---

## Shared files

Other sessions may edit the same docs. Re-read before writing. Change your Agents row and the Now / Backlog rows you own; leave other agents' snapshots alone.

---

## After wind-down

Briefly confirm what you updated and the next step you left for the following session. That confirmation is for the human — the durable truth is in the docs.
