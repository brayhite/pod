# How to POD

The original state of the POD folder is:

POD - root folder 

1. How to POD file (you are probably here)
2. Start Here folder
  . RUNFIRST file
  . Developer Documentation folder
  1. README file (map of the docs)
  2. In Progress folder
  3. Future Work folder
  4. Reference folder
    . Session Wind-Down file
    Templates folder
  5. README file
  6. Agent Instructions Template file
  7. Agent Handoff Template file
  8. Core templates: project status, backlog, changelog, project overview, QA and testing
  9. Optional templates: backlog archive, implementation principles, architecture, implementation plan, design spec
    Agent Instructions folder (empty until agent files are created)
    Agent Handoffs folder (empty until handoff files are created)
    Archive folder
    Code folder



## Getting Started

The basic instructions for using this folder are:

1. Create a copy of the "Start Here" folder
2. Rename it to a project name - if you aren't sure, call it "Unknown"
3. Open the folder in Cursor
4. In the Agent window, say:
  Please run the RUNFIRST instructions. The project name is {what you said for the folder, including "unknown"}. Execute the {basic or advanced} instructions. Here is my {basic/advanced} context: {whatever context helps set up the files}. I confirm {this is/this is not} basic."



## Ending and Resuming Sessions

Chats end, and you may switch devices. The docs carry the context forward, not the chat.

1. Before ending a chat, say: "Wind down this session per `Developer Documentation/Reference/Session Wind-Down.md`." The agent updates Project Status (what's in flight, and each agent's last state and next step).
2. In the next chat, say: "Continue from living docs only (ignore prior chat). Read `Developer Documentation/Project Status.md` (Now + Agents), then any linked plan/spec and Backlog rows. Recommend what to do next."



## Best Practices for Humans

1. Context is valuable no matter which preference you specify
2. Add files and folders to the created Start Here folder and reference them in your initial prompt's context
3. Always keep at least one version of this initial template you downloaded. This gives you a reset button in case your custom set of instructions gets unwieldy
4. In both the RUNFIRST file and this one is a "Version History" section. Maintain a version history of these files to learn from best practices and share them with others.
5. Add your own best practices and tips to the "## Using Context" section of the RUNFIRST doc as you see fit. Or wherever you want, they are your files.
6. The RUNFIRST file contains different instructions depending on whether basic or advanced is selected. The difference essentially boils down to whether or not you will be asked clarifying questions on project start, and whether optional docs are created up front.
7. Setup creates only the core docs. Ask for optional ones (Architecture, Implementation Principles, Decisions, Backlog Archive) when the project grows into them — the Templates README says when each is worth it.
8. Project Status only tracks what's in flight now. Keep "what's next" in the Backlog and "what happened" in the Changelog so none of them go stale.



## Version History

History of changes to this doc. Entries should follow this format, unless specified otherwise from prompt, ordered descending from most recent:

- {yyyy-mm-dd}: {version number} – {summary of changes made}



### Versions

- 20260927: v.04 – Aligned the Start Here outline and the wind-down path with the current folders: `Templates/` beside Developer Documentation, agent templates inside `Templates/`, and Session Wind-Down in `Reference/`.
- 20260926: v.03 – Updated folder outline for the new Developer Documentation structure (README, Session Wind-Down, In Progress / Future Work / Reference folders, Templates); added "Ending and Resuming Sessions"; added best practices for optional docs and keeping Project Status focused.
- 20260216: v.02 – Added instructions for handling an unknown project name.
- 20251226: v.01 – Created and added to POD folder.

