---
title: Systematic writing of documents
---

# Systematic writing of documents

## TL;DR

The common layer of every composed project in MdExplorer: a project wiki written and kept in order with the agents, as
the idea of LLM wikis suggests. The sources stay untouched, the pages grow with every new source, the index and the log
say what is there and what changed.

- It is always taken when a composed project is created; the methods (Ontologies, ISO 9001) are added on top.
- Three agents prepare (editor, reviewer, librarian); the documentation owner approves and decides.
- The theory, if you ask for it, lands in `theory/documenti/`: to read alone or with the MarkAgent.

## What it brings

| What | Where |
|---|---|
| The two workflows: a source into the wiki, the wiki check | `workflows/` |
| The cards of the three agents | `agents/` |
| The role: Documentation owner | the project's responsibilities document, as an open role |
| The instructions for the project's agents | a block in `CLAUDE.md`, `AGENTS.md`, `copilot-instructions.md` |
| The group's starting files | `sources/`, `wiki/index.md`, `wiki/log.md`, `reviews/` |
| The skill of the wiki conventions | `.claude/skills/documenti-wiki/` |
| The theory of LLM wikis | `theory/`, copied into `theory/documenti/` if you ask for it |

## How to start

1. Whoever answers for the documentation takes the role in the responsibilities document (or says «It's mine» in the agent city).
2. Put a document to start from in `sources/`: minutes, a specification, an exported email.
3. Launch the editor («A source into the wiki»): it reads the source, writes or updates the pages, the index and the log.
4. Every now and then launch the librarian («The wiki check»): it finds contradictions, orphan pages, broken links.
