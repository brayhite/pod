# Developer Documentation

Front door for project docs. Keep this map current when the layout changes.

## Living files

| File | Purpose | Created by |
|------|---------|------------|
| **This README** | Map of the docs and where things go. | Ships with POD |
| `Reference/Session Wind-Down.md` | End-of-session handoff so the next chat (or device) can resume from the docs alone. | Ships with POD |
| `Project Status.md` | *Now*: in-flight work plus one snapshot row per agent role. No Next / Later sections. | RUNFIRST (core) |
| `Backlog.md` | Open bugs, enhancements, and features — what to pick up next. | RUNFIRST (core) |
| `Changelog.md` | *Then*: newest-first record of shipped work and meaningful changes. | RUNFIRST (core) |
| `Backlog Archive.md` | Closed Backlog rows, IDs preserved. | Optional — add the first time a Backlog row closes |

Blank forms for all of these (and the optional Reference docs, plans, and specs) live in the project-root `Templates/` folder, beside this folder. See its README for names, locations, and when to create each one.

---

## Folders

Beside this folder at the project root: `Templates/`, `Agent Instructions/`, `Agent Handoffs/`, `Archive/`, `Code/`, and the rules file (`.cursorrules` or equivalent) that points agents here.

### Reference

Stable truth — not a weekly log.

- **Core:** `Project Overview.md` (goals, audience, scope, product rules), `QA and Testing.md` (how we test today).
- **Optional:** `Architecture.md`, `Implementation Principles.md` — add each when the project has enough substance to fill it.

### In Progress

Plans and specs that constrain work **being built now**. A doc lives here **only** while its Backlog row is `in progress`. Empty or nearly empty is healthy.

- **Start building:** set the Backlog row to `in progress` → move the plan here.
- **Pause:** set the row back to `unstarted` → move the plan to Future Work.
- **Ship:** Changelog entry → move the plan to `Archive/` with a one-line banner pointing at that entry → close the Backlog row.

### Future Work

Proposals, catalogs, and plans/specs for open work that is **not being built yet**. Writing a plan does not make it In Progress. The Backlog is the structured index; long write-ups live here.

### Archive (project root)

Deprecated and historical docs only. **Agents: do not read or cite Archive contents unless the user explicitly asks.** Living sources are this folder and `Reference/`.

---

## Where does it go?

| If the doc is… | Put it in… |
|----------------|------------|
| A plan/spec for work actively being built | In Progress |
| A plan/spec/proposal for open work not started | Future Work |
| Always-true product or how-we-build | Reference |
| Done, wrong, or historical | Archive |
| "What happened on date X" | Changelog |
| "What's in flight / who last touched it" | Project Status |
| Structured next work | Backlog |
| Closed or won't-do Backlog rows | Backlog Archive |

---

## Session continuity

- **Project Status is the handoff surface.** The **Now** table says what is in flight; the **Agents** table says what each role last did and will do next.
- **Every agent role gets a row** in Project Status → Agents. Add a row when a role is created in `Agent Instructions/`; remove it when the role is retired.
- **End a session** with `Reference/Session Wind-Down.md`. Start the next one from the living docs, not the old chat.

---

## Currency block

Living docs carry a short block near the top so readers can tell how fresh they are:

```
**Last verified:** YYYY-MM-DD
**Against:** what the claims were checked against (codebase, test suite, project state, …)
**Environment:** toolchain · runtime/device — or N/A
```

Update the date whenever the doc's claims are re-checked.

**Last verified:** 2026-09-27  
**Against:** folder layout  
**Environment:** N/A
