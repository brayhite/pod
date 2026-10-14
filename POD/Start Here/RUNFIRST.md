# RUNFIRST

## Overview
These instructions are to be followed when a Cursor project is started. The "## Steps" section contains explicit, linear steps. If prompt context deviates off this explicit path, confirm the guardrails. If prompts continue to shift in that direction, you're on your own.

## Steps
1. Confirm the following folders and files are present:
	a. RUNFIRST file
	b. Developer Documentation folder
		1. README file
		2. In Progress and Future Work folders (empty at start)
		3. Reference folder, containing the Session Wind-Down file
	c. Templates folder, containing its README, the Agent Instructions Template, the Agent Handoff Template, and the doc templates it lists
	d. Agent Instructions folder (empty until agent files are created)
	e. Agent Handoffs folder (empty until handoff files are created)
	f. Archive folder
	g. Code folder
2. If these folders and files are not present, confirm if they should be made before proceeding.
3. If these folders and files are present, then confirm if the initial prompt and system context contains the following:
	a. Project name
	b. Preference for "basic" or "advanced", being mindful of typos for either word
	c. Context for a Cursor project
	d. Current date
	e. If "basic" preference shared, an explicit confirmation for preference 
4. If any of the above is unknown or unclear, except for "Project name", then confirm and clarify before proceeding. If "Project name" isn't clear, because it wasn't specified in the prompt, or the root folder is "Start Here", "Unknown", or something similar, then use a {project_name} placeholder in any documentation, and in the names of files and folders. Call this out explicitly in the rules file with instructions to update the placeholders once it's defined.
5. Begin following the steps provided under "## Basic" or "## Advanced" depending on which is preferred. Use the information in "## Using Context" and "## Creating the Files" as advised.

## Basic
If the prompt indicated a preference for "basic" instruction, do the following:

1. Analyze the prompt for basic project-relevant information, such as:
	1. Project goal
	2. Tech stack preferences
	3. Agent specific preferences
	4. Any other relevant information for the purposes of creating a Cursor project
2. Refer to "## Using Context" for guidance on using the analysis, then create files per "## Creating the Files":
	1. Do not create more than 3 agent instructions files unless explicitly told or confirmed otherwise
	2. Do not create more than 1 agent handoff file per combo of agents unless explicitly told or confirmed otherwise
	3. Create only the **core** Developer Documentation files. Do not create optional docs, plans, or specs unless explicitly told otherwise
	4. Do not create, modify, read from, or delete any files other than those named in this document unless explicitly told otherwise
	5. Explicitly follow guidance inside each template file
	6. Do not edit template files unless explicitly told to
3. Create or update the rules file per "## Cursor Rules"
4. Report on what you did using "## Report"

## Advanced
If the prompt indicated a preference for "advanced" instruction, do the following:

1. Analyze the prompt for basic project-relevant information, listed below. Ask up to 3 follow-up questions per section below, with proposed multiple choice answers and an "Other" option. Follow the guidance in each to ask the most helpful and appropriate questions based on the context in the prompt. Before proceeding, summarize the key information for each section below and reference clarifications. Confirm the list of files that will be created and/or edited.
	a. Project Goal
		i. Information to gather: Purpose, scope, target audience, key features, success criteria
		ii. Potential follow-up questions. These are only examples; frame unique versions of these questions and others that are most appropriate given provided context:
			1. What problem does this project solve?
			2. Who is the intended audience or user?
			3. What are the 3-5 core features you need?
			4. Is this a proof-of-concept, MVP, or production-ready application?
	b. Tech Stack Preferences
		i. Information to gather: Languages, frameworks, databases, hosting, existing constraints
		ii. Potential follow-up questions. These are only examples; frame unique versions of these questions and others that are most appropriate given provided context:
			1. Do you have preferred languages or frameworks (e.g., React, Python, Node.js)?
			2. What database are you planning to use, if any?
			3. Are there any existing systems this needs to integrate with?
			4. Do you have hosting/deployment preferences (e.g., Vercel, AWS, local)?
			5. What sort of devices will be used to run this application (e.g., OS-specific, form factor, browser needs)?
	c. Agent-Specific Preferences
		i. Information to gather: unique specialities, desired skill sets, expertise dependencies, perceived detail level
		ii. Potential follow-up questions. These are only examples; frame unique versions of these questions and others that are most appropriate given provided context:
			1. Is there any specific skill set you want an expert for?
			2. Do you prefer QA and engineering to be separate agents?
			3. Are you comfortable being the "product" person or do you want guidance?
			4. Given the likely complexity, do you want an agent responsible for maintaining documentation?
			5. Should the agent create new files freely or ask first?
	d. Other Relevant Information
		i. Information to gather: Experience level, existing code, dependencies, hard constraints, documentation depth
		ii. Potential follow-up questions. These are only examples; frame unique versions of these questions and others that are most appropriate given provided context:
			1. Do you have existing code or are we starting from scratch?
			2. What's your experience level with the chosen tech stack and domain?
			3. Are there any specific constraints related to the audience, industry, tech stack, domain, or personal preferences?
			4. How much autonomy can agents have in making code changes?
			5. How much autonomy can agents have in creating or updating documentation?
			6. Beyond the core docs, which optional docs should exist from the start (Architecture, Implementation Principles, Backlog Archive), or should they be added later as needed?
2. Refer to "## Using Context" for guidance on using the analysis, then create files per "## Creating the Files":
	a. Do not create more than 3 agent instructions files unless explicitly told or confirmed otherwise
	b. Do not create more than 1 agent handoff file per combo of agents unless explicitly told or confirmed otherwise
	c. Create the **core** Developer Documentation files, plus any **optional** docs confirmed in step 1. Do not create plans or specs unless explicitly told otherwise
	d. Do not create, modify, read from, or delete any files other than those named in this document unless explicitly told otherwise
	e. Explicitly follow guidance inside each template file
	f. Do not edit template files unless explicitly told to
3. Create or update the rules file per "## Cursor Rules"
4. Report on what you did using "## Report"

## Creating the Files

### Agent Instructions
- Create one copy of `Templates/agent-instructions.md` per agent, named `AGT_{SHORTNAME}.md` (e.g. `AGT_SWIFT.md`, `AGT_QA.md`), and save it in `Agent Instructions/`. Follow the template's "New agent instructions steps".

### Agent Handoffs
- Create at least one copy of `Templates/agent-handoff.md` for the pair of agents most likely to trade work (e.g. engineering and QA), named `AGT_{A}_and_AGT_{B}.md`, and save it in `Agent Handoffs/`. Follow the template's "New handoff template steps".

### Developer Documentation — core (always)
Copy each from `Templates/`, using the names and locations in the Templates README. Set **Last verified** to today on each.

| Doc | How to fill it at setup |
|-----|-------------------------|
| `Reference/Project Overview.md` | **Started on** = today. Goals, audience, scope, constraints, and success criteria from the prompt. Use `TBD` rather than inventing. |
| `Reference/QA and Testing.md` | A short technical review checklist and user acceptance checklist suited to the stack and goals. Coverage = `None yet` until tests exist. |
| `Backlog.md` | Rows only for concrete features, bugs, or first steps named in or clearly implied by the prompt; mark the first 1–3 as Priority `Now`. If there are none, remove the example row and leave the table empty. |
| `Project Status.md` | **Now**: one row per Backlog row at Priority `Now` (or empty). **Agents**: one row per agent created, e.g. "Idle — set up {date}. Next: {first recommended step}." |
| `Changelog.md` | One entry dated today: project set up with POD v.04, plus 2–4 sentences on the goal, tech stack, and agents created. |

### Developer Documentation — optional (advanced when confirmed, or later on request)
`Backlog Archive.md`, `Reference/Architecture.md`, `Reference/Implementation Principles.md`. The Templates README says when each becomes worth creating.

### Ready-to-use files (do not copy)
`Developer Documentation/README.md` and `Developer Documentation/Reference/Session Wind-Down.md` ship ready to use. Edit them only if you rename folders or files they reference.

## Cursor Rules
If a rules file already exists (`.cursorrules`, `AGENTS.md`, or files under `.cursor/rules/`) and contains instructions for Cursor, do NOT create a new one. Instead, add a new section called "POD Addition" to it, and add the content below there.

If none exists, create `.cursorrules` at the project root. Cursor does not read other spellings such as `.cursor_rules`.

Keep the rules file a short orientation map: point at docs rather than restating their contents.

Inside this section or document, add the following. The entire set of copy is contained in double curly brackets:

{{
	# {Project name} – Cursor Rules

	## Project
	{1–2 sentence summary of what is being built and for whom.}

	This file orients agents only. Product rules, architecture, and conventions live in `Developer Documentation/`. Read the relevant doc below before changing behavior or data flow.

	## Documentation
	| Need | Read |
	|------|------|
	| Map of the docs | `Developer Documentation/README.md` |
	| What's in flight now | `Developer Documentation/Project Status.md` |
	| End session / resume later | `Developer Documentation/Reference/Session Wind-Down.md` |
	| What to pick up next | `Developer Documentation/Backlog.md` |
	| Shipped history | `Developer Documentation/Changelog.md` |
	| Product goals & rules | `Developer Documentation/Reference/Project Overview.md` |
	| Testing & QA | `Developer Documentation/Reference/QA and Testing.md` |
	| {one row per optional Reference doc created, e.g. Architecture & data flow} | {path} |
	| Active build plans | `Developer Documentation/In Progress/` — only while the Backlog row is `in progress` |
	| Not-yet-started plans & specs | `Developer Documentation/Future Work/` |
	| Blank forms for new docs | `Templates/` |

	`Archive/` is historical only. Do not read or cite it unless the user explicitly asks.

	## Agents
	| Role | Instructions |
	|------|--------------|
	| {AGT_NAME} – {short descriptive name}: excels at {core competencies} | `Agent Instructions/AGT_NAME.md` |
	| Handoffs | `Agent Handoffs/` (template: `Templates/agent-handoff.md`) |

	Workflow: {one line, e.g. "engineer implements → QA reviews before work is complete"}.

	## Keeping docs current
	- Every agent role has a row in Project Status → Agents. When a role is added, renamed, or removed, update that table and the Agents list above.
	- New agent: copy `Templates/agent-instructions.md` into `Agent Instructions/`. New handoff: copy `Templates/agent-handoff.md` into `Agent Handoffs/`. Use handoffs only when another role must act; link supporting docs instead of pasting long content.
	- New living doc, plan, or spec: copy from `Templates/` (see its README). Don't edit the templates unless asked.
	- When meaningful work ships, suggest a Changelog entry and close the Backlog row. When behavior or tests change, suggest QA and Testing updates.
	- When a session is ending, offer to run Session Wind-Down (`Developer Documentation/Reference/Session Wind-Down.md`).
	- Use pattern analysis and positive reactions as signals for improvements to agent instructions or templates; suggest them rather than silently applying them.

	**Last updated:** {today's date}
}}

## Report
Report on what you did with the following template, using prompt instructions relevant to your tone and whatnot as you see fit:

	"I have created files for {the project name}. The following agent instruction files exist:
		{outline list of created "AGT_" instruction files, with 1-2 sentence summary of each}
	I recommend creating Cursor windows or agents for each, named after their file name, e.g. {mention one of the agent names}.
	I have created the following developer documentation:
		{outline list of files created in "Developer Documentation", with 1-2 sentence summary of each}
	I have {created/updated} {the rules file name} with the following:
		{outline list of updates made to the rules file}
	I used the following information to create these files:
		{outline list of assumptions, clarifications, and other relevant information, limiting to 1-2 sentences per entry, and entries to 5 or less}
	While it's helpful to read all documentation I created, I highly recommend reading at least {the rules file name}. This helps understand how the project works, and can be a good place to make customizations. You can ask me to do it for you, or tweak it manually.
	When you're ready to proceed, start creating agents. For each agent window, instruct it to check for its corresponding AGT_ file, and follow its contents. When each agent is created and finished reading its instructions, start with {recommend which agent to talk to for getting started; use prompt context accordingly to make the best recommendation}. They will leverage Agent Handoff documentation to utilize the other agents as needed.
	Before ending any chat session, follow `Developer Documentation/Reference/Session Wind-Down.md`.
	Now that I'm finished using the RUNFIRST file, may I move it to the Archive folder?"

## Using Context
Before following any guidance below, check for files that are not included in the aforementioned outline of folders and files. Review these provided files for information that may conflict with guidance provided below. In all cases, err on the side of following guidance in the net-new provided files. Treat the outlines below as suggestions and follow as appropriate given the overall context of the project.

### Lack of clarity
Whether because the preference is for "basic" and there aren't any follow-up questions to ask, or the follow-up questions weren't helpful for getting clarity, use the following fallback guidance for each section:

**Project goal**: Make a best guess at what problem is being solved, who is impacted by the problem, and an effective way to solve it based on the context provided.
**Tech stack preferences**: Make a best guess at what form factor or OS will likely be used to interact with this application. Assume only the most popular one or two options. Work backwards from this best guess to determine the most appropriate tech stack considerations.
**Agent specific preferences**: Based on the domain knowledge necessary for solving the problem for its audience, and the tech stack preferences being presumed, make best guesses for what agents would be effective. In most cases, it's one agent per programming language, and up to two more agents to cover the domain, QA, additional programming language specialties, user experience guidance, documentation, etc. E.g., a project for Wordpress development could have a PHP agent, a JS agent, and a Wordpress admin agent. A mobile app project could have three agents: Swift development, Mobile UX specialist, and Quality Control.
**Any other relevant information for the purposes of creating a Cursor project**: For "basic" preferences, only consider either the context provided in the prompt, or what can be inferred from any net-new files and folders.

## Version History
History of changes to this doc. Entries should follow this format, unless specified otherwise from prompt, ordered descending from most recent:
- {yyyy-mm-dd}: {version number} – {summary of changes made}

### Versions
- 20260927: v.04 – Pointed setup, copy instructions, and the rules-file map at the current folders: `Templates/` at the project root, agent templates inside it, and Session Wind-Down in `Developer Documentation/Reference/`.
- 20260926: v.03 – Replaced "Project Overview and History" and "QA and Debugging" with templated core docs (Project Overview, QA and Testing, Backlog, Project Status, Changelog); added Session Wind-Down, doc map README, In Progress / Future Work / Reference folders, and optional doc templates; added "## Creating the Files" and a shared "## Report"; rules file is now `.cursorrules` (not `.cursor_rules`) written as a short pointer map; every agent gets a Project Status row.
- 20260216: v.02 – Added more explicit instructions for how to get started to the "RUNFIRST COMPLETE" message.
- 20251226: v.01 - Created RUNFIRST.md for POD.
