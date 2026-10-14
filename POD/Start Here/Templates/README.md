# Templates

Blank forms for the project's living docs, plans, and specs. **Copy** a template to create a doc; do not edit these files except through **Changing a template** below.

## When copying

1. Save the copy at the **location** and **name** in the table below.
2. Replace placeholders (`[brackets]`, `YYYY-MM-DD`), keep the **How to use this doc** section, and set **Last verified** to today.
3. Delete example rows once real rows exist. Use `None` or `TBD` rather than inventing content.
4. Keep the **Template version** line. It shows which version the doc was copied from.

## Templates

| Template | Creates | Location | When |
|----------|---------|----------|------|
| `project-status.md` | `Project Status.md` | `Developer Documentation/` | **Core** — RUNFIRST |
| `backlog.md` | `Backlog.md` | `Developer Documentation/` | **Core** — RUNFIRST |
| `changelog.md` | `Changelog.md` | `Developer Documentation/` | **Core** — RUNFIRST |
| `project-overview.md` | `Project Overview.md` | `Developer Documentation/Reference/` | **Core** — RUNFIRST |
| `qa-testing.md` | `QA and Testing.md` | `Developer Documentation/Reference/` | **Core** — RUNFIRST |
| `backlog-archive.md` | `Backlog Archive.md` | `Developer Documentation/` | Optional — the first time a Backlog row closes |
| `implementation-principles.md` | `Implementation Principles.md` | `Developer Documentation/Reference/` | Optional — once coding conventions settle |
| `architecture.md` | `Architecture.md` | `Developer Documentation/Reference/` | Optional — once the system has more than one layer worth describing |
| `implementation-plan.md` | `Implementation Plan - [name].md` | `Future Work/` → `In Progress/` while building | Per piece of work |
| `design-spec.md` | `Design Spec - [name].md` | `Future Work/` → `In Progress/` while building | Per piece of work, when product/UX decisions need locking first |

`Reference/Session Wind-Down.md` and the Developer Documentation `README.md` ship ready to use — they are not templates.

## Currency block

Every template carries this block; keep it in the copy:

```
**Last verified:** YYYY-MM-DD
**Against:** what the claims were checked against
**Environment:** toolchain · runtime/device — or N/A
```

## Changing a template

1. **Propose.** Tell the product owner which template, what changes, and why. Nothing is saved until the product owner approves it.
2. **Edit.** Make the approved change and raise the version line at the top of the template (`v.03` → `v.04`). The version lives only in that line, never in the file name, so file names do not change and links keep working.
3. **Record.** Add a row to **Version History** below.
4. **Leave copies alone.** Docs already copied from an older version are not updated to match, unless the product owner asks.

## Version History

Newest first. One row per approved change.

| Date | Template | Version | Change | Approved by |
|------|----------|---------|--------|-------------|
| 2026-10-12 | Agent Instructions, Agent Handoff | v.06; v.03 | Files renamed to `agent-instructions.md` and `agent-handoff.md` to match the other templates. The version is kept only in the **Template version** line. **Changing a template** now says versions never go in file names. | Product owner |
| 2026-10-12 | This README | — | **Changing a template**: the two agent templates are renamed when their version goes up, and links to them are updated. Other file names stay the same. | Product owner |
| 2026-10-12 | Agent Instructions | v.06 | File renamed from `Agent Instructions Template v.03.md` to `Agent Instructions Template v.06.md` to match its version. | Product owner |
| 2026-10-11 | `decisions.md` | Removed | Decisions retired. Its rows moved to Project Overview, Architecture, and Implementation Principles. | Product owner |
| 2026-10-11 | `implementation-plan.md` | v.04 | The evergreen doc list drops Decisions and adds Implementation Principles. | Product owner |
| 2026-10-11 | `architecture.md`, `implementation-principles.md` | v.02 | "Not this doc" points to the Changelog instead of Decisions. Each rule gets a one-line *Why:*. | Product owner |
| 2026-10-11 | `design-spec.md`, `project-status.md`, `changelog.md` | v.02 | References to Decisions now point to Architecture or Implementation Principles. | Product owner |
| 2026-10-11 | `implementation-plan.md` | v.03 | Every plan ends with an **Update evergreen docs** phase: outline the changes, get the product owner's approval, then merge. Added **Evergreen doc changes** to collect them during the build; the intro now points there instead of writing to the docs mid-build. | Product owner |
| 2026-10-10 | Agent Instructions | v.06 | Agents that review work check it against the Reference docs and cite the doc a change conflicts with. Added a Docs line to the QA scope example. | Product owner |
| 2026-10-10 | `implementation-plan.md` | v.02 | Lasting rules, values, and terms go in evergreen docs and are linked. Added Deviations from Spec. Each phase states its outcome, how it is validated, and whether validation must finish first. Test split into QA Code Review, Automated Testing, and Manual Testing. | Product owner |
| 2026-10-10 | All templates | v.01; Agent Handoff v.03; Agent Instructions v.05 | Added a **Template version** line under each title. The two agent templates keep their existing numbers. | Product owner |
| 2026-10-10 | Agent Instructions | v.05 | Moved this template's own Version History into this table. The template's history section now starts each new agent file's own history instead. | Product owner |
| 2026-10-10 | This README | — | Added **Changing a template** and this history. Template changes were previously to be noted in `How to POD.md`, which is not part of this project. | Product owner |
| Before 2026-10-10 | Agent Instructions | v.04 | Handoff template is in `Templates/`; session wind-down is `Developer Documentation/Reference/Session Wind-Down.md`. | — |
| Before 2026-10-10 | Agent Instructions | v.03 | Read Project Status and the doc map first; fixed rules-file and handoff-template names; added Documentation discipline example and Session Continuity section. | — |
| Before 2026-10-10 | Agent Instructions | v1.0 | Initial template. | — |
