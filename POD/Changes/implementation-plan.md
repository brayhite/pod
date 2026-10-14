# Implementation Plan - [name]

**Template version:** v.04

## How to use this doc

One piece of work being built. Follow Implementation Principles (if used) unless this plan records an exception under **Exceptions to principles**.

Lives in `Future Work/` until its Backlog row is `in progress`, then moves to `In Progress/`. On ship, move it to `Archive/` with a one-line banner pointing at the Changelog entry.

**Lasting knowledge goes in evergreen docs, not here.** Rules, values, terms, and how part of the app works belong in the doc that owns them: Game Modes, Settings Catalog, Terminology, Architecture, Implementation Principles, or a new Reference doc when none fits (see `Developer Documentation/README.md` → Reference). While building, add each one to **Evergreen doc changes** as it is settled. The last phase outlines them for the product owner and merges only what is approved. This plan is archived on ship and agents don't read `Archive/`, so anything left only here is lost.

When scope is cut, add the deferred work to the Backlog with Notes citing this plan (e.g. `Deferred from Implementation Plan - [name], Phase 3`).

Not this doc: standing product rules (Project Overview), standing architecture (Architecture), or the full backlog (Backlog).

**Last verified:** YYYY-MM-DD  
**Against:** this plan  
**Environment:** N/A (or toolchain / device when verifying phases)

---

## Status

`unstarted` | `in progress` | `closed` — matches the Backlog row.

## Related

Backlog ID(s) · Design Spec (if any) · Evergreen docs this plan reads or updates

## Goal

### Problems to solve

- 

### Outcomes

- 

## Locked decisions

| Topic | Decision |
|-------|----------|
| | |

## Deviations from Spec

Every place this plan departs from its design spec, and why. When the product owner changes a spec decision during the build, add a row here. Until the spec is updated, this table wins over the spec. `None` if there is no spec or the plan follows it exactly.

| Spec says | This plan does | Why | Date |
|-----------|----------------|-----|------|
| | | | |

## Evergreen doc changes

What this work settles that belongs in an evergreen doc. Add a row when it is settled; the last phase proposes and merges them. `None` until something is.

| Doc | Change | Settled in |
|-----|--------|------------|
| | | |

## Phases

Each phase states:

- **Outcome:** what is true when the phase is done.
- **How to validate:** which apply, if any: a QA code review, automated tests, or a manual check by the product owner. Point at the items in **Test** that cover it.
- **Requires validation?** `Yes` or `No`: whether validation must finish before the next phase starts, why, and what skipping it changes for the phases after it.

1. **[Phase name]**
   - **Outcome:** 
   - **How to validate:** 
   - **Requires validation?** 

Every plan ends with this phase. Keep it last, after every other phase is validated.

N. **Update evergreen docs**
   - **Outcome:** Every evergreen doc reflects what this work settled, and nothing lasting is left only in this plan.
   - **How to validate:** Outline every proposed change to the product owner: which doc, what changes, and the exact new wording or values, drawn from **Evergreen doc changes** and anything else the build settled. Ask for approval. Merge only the approved changes into the docs.
   - **Requires validation?** Yes. Nothing is written to an evergreen doc until the product owner approves the outline. Agents trust these docs over the code and the plan, so an unapproved change becomes the rule. The plan doesn't ship until this phase is done.

## Exceptions to principles

- None.

## Test

### QA Code Review

What to ask QA to review, and after which phase. Make each request by writing it in the handoff between the building agent and AGT_QA in `Agent Handoffs/`. QA checks the change against the evergreen docs as well as this plan.

- 

### Automated Testing

Which automated tests to write and run, and how to run them.

- [ ] 

### Manual Testing

A checklist for the product owner to test by hand, grouped by phase. These become QA and Testing checks when the work ships.

- [ ] 

If this plan changes what "green" means, update QA and Testing when the work ships.
