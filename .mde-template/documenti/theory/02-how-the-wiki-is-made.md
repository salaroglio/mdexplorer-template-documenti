---
title: How the wiki is made
---

# How the wiki is made

## TL;DR

In an MdExplorer project the wiki has two folders: `sources/`, which nobody modifies, and `wiki/`, with the index, the
log and one page for every concept or source. Every page has a title, a TL;DR and the links to the nearby pages.
- `wiki/index.md` is the front door: from there you find everything.
- `wiki/log.md` is the diary of the changes, one entry per operation.
- The sources stay as they arrived: the pages cite them.

## The folders

```text
sources/                   the original documents: minutes, tender specifications, articles
wiki/
├── index.md               the map of the wiki
├── log.md                 the diary of the changes
├── nordica-crediti.md     one page for every concept, person, organisation or process
└── source-<name>.md       one summary page for every source read
reviews/                   the reviewer's reviews and the librarian's checks
```

The pages are all in the same folder: it is the index that divides them by kind (concepts, people and organisations,
processes, sources), and the file name says the topic.

The folder names are a starting point: if your group prefers something else, change them, but write the choice in the
project's instructions file, so the agents follow it.

## The sources are not touched

A source is a document that comes from outside. It goes into `sources/` and from there it no longer changes. If a new
version arrives, it comes in as a new file, with the date in its name: `sources/2026-11-03-meeting-minutes.md`.

Why: the wiki's pages say «according to the minutes of 3 November». If the minutes changed, that sentence could no
longer be checked.

A source in PDF or Word is fine too: the summary cites it by its file name.

## The index

`wiki/index.md` lists the wiki's pages, grouped by topic, each with one line that says what it is about. An example:

```markdown
## Clients
- [Nordica Crediti](nordica-crediti.md) — the client, the contacts, the past tenders
- [Tender NC-2027-014](source-nc-2027-014.md) — summary of the tender specification, with the blocking requirements
```

Whoever looks for something, person or agent, starts here. A page that is not in the index almost does not exist for
the wiki.

## The log

`wiki/log.md` is a diary written only at the bottom, without deleting. Every operation has its entry:

```markdown
## [2026-11-03] source | minutes-2026-11-03.md
- New: wiki/source-minutes-2026-11-03.md
- Updated: wiki/nordica-crediti.md, wiki/security-requirements.md
- index: added the summary under «Clients»
```

The actions are `source` (an ingest), `page` (a page written or fixed by hand, including the answer to a query worth
keeping) and `check` (a lint). The log answers the question «what changed since I last looked?» without having to read
all the commits.

## The pages

There are two kinds of page:

- **Concept page**: an idea, a person, an organisation, a requirement. It gathers what the group knows, from all the
  sources. It grows over time.
- **Summary page**: a source that was read. It says what it contains, what it changed, and links to the concepts it
  touched. Once written it changes little.

Every page starts with the front matter and the TL;DR:

```markdown
---
title: Security requirements
sources: [sources/NC-2027-014-specification.pdf, sources/2026-11-03-minutes.md]
updated: 2026-11-03
---

# Security requirements

## TL;DR
...
```

## The links

A page that names a concept with a page of its own links to it with a relative link:
`[security requirements](security-requirements.md)`. This way the wiki becomes a network you can walk, and the
librarian can notice the pages nobody reaches.

Every important statement says which source it comes from. Without a source it is an opinion: it is fine to write it,
but it must be said.

## Where the schema is

The wiki's rules are in the project's instructions file (`CLAUDE.md`, `AGENTS.md` or `copilot-instructions.md`). There
the group writes its choices: the folder names, the topics of the index, what does not enter the wiki. The agents read it
for every job. The operations that use this structure are in [chapter 3](03-the-three-operations.md).
