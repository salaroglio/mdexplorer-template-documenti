# CHANGELOG

## 2.0.0 — 2026-10-21
- ⚠️ incompatible: the template is in format 2 and needs MdExplorer 2026.10.21.2 or newer. Agents, roles and workflows arrive only with the agent city turned on; the skills live in the template's folder and MDE copies them into .claude/skills/. What to do: update MdExplorer before updating the template; without the city, turn it on from the project settings to get the agents.
- The method is called «Document Driven Development», in Italian and in English (it was «Systematic writing of documents»).

## 1.1.0 — 2026-10-20
- The common layer speaks English too: the `en` (structure) and `example` branches, with agents, workflows, skill, starting files and theory in English, and the English slides for the «Create new project» showcase.

## 1.0.0 — 2026-10-19
- First version of the common layer (Italian): the project's wiki (untouched sources, pages, index, log), three agents (editor, reviewer, librarian), two workflows (a source into the wiki, the wiki check), the `documenti-wiki` skill and the theory of LLM wikis. Needs MdExplorer 2026.10.19.14 or newer.
