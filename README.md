# POD

A Project On Demand, aka POD, is a starter kit of folders, templates, and setup instructions for running a software project with AI coding agents in tools like [Cursor](https://cursor.com) and [Claude Code](https://www.anthropic.com/claude-code).

POD has everything necessary to keep just the right amount of documentation and context needed so that work can seamlessly start, stop, and resume from the same device or another one, so long as you use Github or some other service to make POD folders available anywhere you work.

## What you get

- **A one-time setup script for your agent.** `RUNFIRST.md` transforms your idea for an app into a set of agent ready to help code, design, QA, and document your progress.
- **Living docs.** A small set of documents that each answer one question, so none of them go stale:


| Doc              | Answers                                                         |
| ---------------- | --------------------------------------------------------------- |
| Project Status   | What's in flight right now, and where each agent left off?      |
| Backlog          | What should we pick up next?                                    |
| Changelog        | What shipped, and when?                                         |
| Project Overview | What are we building, for whom, and what are the product rules? |
| QA and Testing   | How do we check that work is done?                              |


- **Optional docs** for when the project grows into them: Architecture, Implementation Principles, Backlog Archive, and per-feature Implementation Plans and Design Specs.
- **A session wind-down routine** so every chat ends by writing down where things stand and what to do next.



## Repository layout

```
POD/
├── How to POD.md          Human guide: setup, sessions, best practices
└── Start Here/            Copy this folder to start a new project
    ├── RUNFIRST.md        One-time setup instructions for the agent
    ├── Developer Documentation/
    │   ├── README.md      Map of the docs and where things go
    │   ├── Reference/     Stable truth (Overview, QA, Session Wind-Down, ...)
    │   ├── In Progress/   Plans for work being built now
    │   └── Future Work/   Plans for work not started yet
    ├── Templates/         Blank forms for every doc, agent, and handoff
    ├── Agent Instructions/  One file per agent role (created at setup)
    ├── Agent Handoffs/      One file per pair of agents that trade work
    ├── Archive/           Historical docs; agents ignore it unless asked
    └── Code/              Your project's code
```



## Getting started

1. Clone this repo or download it as a ZIP.
2. Copy the `POD/Start Here` folder to wherever you keep projects, and rename it to your project's name. If you don't have a name yet, call it `Unknown`.
3. Open the renamed folder in Cursor or Claude Code.
4. Open `[POD/How to POD.md](POD/How%20to%20POD.md)` for instructions on what's next; there are only 1 or 2 more steps to go before you're ready to start building

## Using Claude Code

POD was built in Cursor, and by default RUNFIRST creates a `.cursorrules` file, which Claude Code doesn't read. If you use Claude Code, add this to your setup prompt:

> Use `CLAUDE.md` as the rules file instead of `.cursorrules`.

The rest of POD is plain Markdown and works the same way.

## Tips

- **Keep a clean copy of** `Start Here`**.** It's your reset button if a project's setup gets messy.
- **Project Status only tracks what's in flight.** Put "what's next" in the Backlog and "what happened" in the Changelog.
- **Add optional docs when you need them, not up front.** `Templates/README.md` explains when each one is worth creating.
- **Make the files your own.** Agents are told to suggest improvements to their instructions and templates rather than change them silently, and each template has a version line and history so you can track what changed.

See `[POD/How to POD.md](POD/How%20to%20POD.md)` for the full human guide.