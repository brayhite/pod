# Backlog

**Template version:** v.01

## How to use this doc

Structured inventory of **open** bugs, enhancements, and features. Source of truth for what to pick up next when current work wraps.

**Closed rows** move to Backlog Archive (if used) or are removed after a Changelog entry. IDs are never reused.

**Type:** `bug` | `enhancement` | `feature`

**Status:** `unstarted` | `in progress` — only open work belongs in this table.

**Priority:** `Now` | `Next` | `Later` — what to pick up. Multiple `Now` rows are fine; keep Project Status → Now in sync with them.

**Release:** Optional target version (e.g. `1.0.0`). Blank = unscheduled. Release is which version cut; Priority is execution order.

**Seq:** Optional integer within the same Release + Priority group (lower = earlier). Leave blank when order does not matter.

**Date Added:** When the row was filed. Format: `Mon D, YYYY`.

**Dependencies:** Note in **Notes** when needed (`Blocked on 12`, `Requires 07`, `soft: 09`).

**ID:** Sequential integer, two digits under 100 (`00`, `01`, …). Assign the next unused number; do not reuse closed IDs.

**Table order:** Release ascending (blank last) → Priority (`Now` → `Next` → `Later`) → Seq ascending (blank last) → ID.

**When closing:** Changelog entry (if shipped or a meaningful decision) → move the row to Backlog Archive (if used) → remove it from this table.

**Plans / specs:** Link path should match Status — `In Progress/` only while Status is `in progress`; otherwise `Future Work/` (or `Archive/` when closed). Writing a plan does not change Status or folder.

Not this doc: shipped history (Changelog), session notes or pickup narrative (Project Status), how to implement (plans).

**Last verified:** YYYY-MM-DD  
**Against:** backlog table  
**Environment:** N/A

---

| ID | Type | Status | Priority | Release | Seq | Date Added | Summary | Notes |
|----|------|--------|----------|---------|-----|------------|---------|-------|
| 00 | feature | unstarted | Now | | | Mon D, YYYY | Short summary | Plan/spec link if any; dependencies if any. |
