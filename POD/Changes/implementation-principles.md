# Implementation Principles

**Template version:** v.02

## How to use this doc

Default rules for day-to-day work and for new implementation plans. A plan may record an exception under **Exceptions to principles**; it should not re-argue these. Give each rule a one-line *Why:* so it isn't reopened.

Not this doc: product rules (Project Overview); how the system is laid out today (Architecture); shipped history (Changelog).

**Last verified:** YYYY-MM-DD  
**Against:** codebase + principles  
**Environment:** [toolchain] or N/A

---

## Invariants

Product rules that code must enforce. Summarize and point at Project Overview — don't restate in every plan.

- 

## Data

Storage defaults, safe decoding, and shared-access rules. Leave layer boundaries to Architecture.

- 

## Conventions

- Naming (types, files, modules):
- File organization:
- Unsafe shortcuts (e.g. force unwraps, `any`, ignored errors) — policy:

## Error handling

- When to fail softly / keep the last good state:
- When to throw or handle explicitly:
- How unexpected failures surface to users:

## UI and interaction

Interaction defaults: motion, timing, accessibility, feedback.

- 

## Plans and code

Framework and concurrency preferences, file size, state ownership (one line — details in Architecture), and how to write plans.

- 

## Testing

What to test automatically and manually by default. Point to QA and Testing for inventory.

- 
