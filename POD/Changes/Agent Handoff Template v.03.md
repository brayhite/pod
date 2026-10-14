# Agent Handoff Document Template

**Template version:** v.03

Use this document only when one agent needs another to act. Each agent's own status lives in `Developer Documentation/Project Status.md` → Agents, not here. Don't paste chat transcripts; link supporting docs instead.

## New handoff template steps
After creating a copy of the template file, follow these steps when creating a new handoff doc. When you are done, the "New handoff template steps" section should be removed from the file.

### Steps
1. As relevant, replace mentions of AGT_ names with the corresponding agents this document is for
2. Unless otherwise specified in the project rules file (`.cursorrules` or equivalent), do not add new sections. 
3. If artifacts need to be generated, create new files and store in "Agent Handoffs" folder, and reference their names in this doc accordingly.
4. Update each section below using the guidance provided within each
5. When finished, every section below should either contain content, or instructions for what to add to it when ready
6. The "New handoff template steps" section is removed

## Header Info
Update this information as pertinent to tracking document history and picking up for future reference.
- Last Updated: [date of last update]
- Current Status: [brief status]

## Reference Materials
- [Links to relevant docs, names of relevant files and project documentation, tips and best practices for agents working together, etc; create sections as needed]

Cite only the docs the receiving agent actually needs. Copy paths from `Developer Documentation/README.md` or the project rules file rather than from older handoffs — older handoffs may point at files that have since moved or been archived. Link `Archive/` only to say something is superseded, never as current truth.

## Open Threads
### AGT_1 → AGT_2
#### Last message
[date of message] - [body of message from AGT_1 to AGT_2]

#### Requested Action Items
These actions items were requested by AGT_1. They are marked completed by AGT_2. They will be removed by AGT_1 as instructed. If there are no outstanding action items, "None" will be listed.
- [ ] Action item 1
- [ ] Action items 2

Action items blockers:
- [List any dependencies on todos for other agents, blockers, etc.]

### AGT_2 → AGT_1
#### Last message
[date of message] - [body of message from AGT_2 to AGT_1]

#### Requested Action Items
These actions items were requested by AGT_2. They are marked completed by AGT_1. They will be removed by AGT_2 as instructed. If there are no outstanding action items, "None" will be listed.
- [ ] Action item 1
- [ ] Action items 2

Action items blockers:
- [List any dependencies on todos for other agents, blockers, etc.]

## Communication Log
These entires are added on demand. Follow the format below when adding new entires. Sort by date in descending order, with the most recent at the top and oldest at the bottom.

**Example entry:** 2025-12-21 – AGT_1 requested AGT_2 to address bugs found in the last round of test results. Bugs found included {list or summary of bugs}. AGT_2 addressed them by {summary of code changes}. Some bugs could not be adequately addressed, including {list of bugs that weren't fixed}.

### Entries
- {date of documentation creation} - Handoff document created.