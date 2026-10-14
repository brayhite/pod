# Architecture

**Template version:** v.02

## How to use this doc

**Current technical truth only.** Update when the system changes.

Fill each section for this project. Use `None` or `Not applicable` when a section doesn't apply — don't delete sections.

Not this doc: product rules (Project Overview); coding style and conventions (Implementation Principles); shipped history (Changelog); this week's work (Project Status).

**Last verified:** YYYY-MM-DD  
**Against:** codebase  
**Environment:** [toolchain · runtime/device]

---

## Overview

3–5 sentences for engineers: what the system does, target platform/runtime, and the architectural style in one sentence.

---

## Layer map

Who talks to whom. For each layer: its one job, and what it is **not** allowed to do.

```
[Layer] → [Layer] → …
```

| Layer | Job | Not allowed |
|-------|-----|-------------|
| | | |

### Boundary rules

Rules new code must follow (e.g. who may write to storage, where business rules live). Give each rule a one-line *Why:* so it isn't reopened.

- 

---

## Folder structure

Real source layout today, not aspirational. **If this won't stay current, delete this section.**

```
[Project root]/
├── …
```

---

## Data flow

One representative end-to-end flow (e.g. user action → state → storage → UI). Name the mechanisms on critical paths.

1. 

---

## State management

What owns which state, and which tools to use when.

---

## Persistence

| Data | Storage | Notes |
|------|---------|-------|
| | | |

---

## Networking

`None` if offline-only.

---

## Dependency management

How dependencies are wired, and any explicit exceptions. `None` if not applicable.

---

## Concurrency

Threading / async expectations and any shared-access rules. `None` if trivial.

---

## Third-party dependencies

| Package | Why |
|---------|-----|
| | |

Also note what you deliberately **did not** add, if it matters for future work.

---

## Known constraints / non-goals

What this architecture explicitly does not solve yet.
