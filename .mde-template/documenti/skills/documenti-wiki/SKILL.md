---
name: documenti-wiki
description: "The conventions of the project's wiki (MdExplorer's common layer): how a page is made, the index wiki/index.md and the log wiki/log.md, and what the reviewer and the librarian check. Use it when you write, update, review or check a page in wiki/, or when you bring a source from sources/ into the wiki."
---

# The project's wiki

Three layers, as in LLM wikis: **the sources** (`sources/`, untouched: minutes, specifications, exported emails),
**the wiki** (`wiki/`, the pages written and kept in order), **the conventions** (this skill and the project's
instructions). The wiki grows: every new source enriches pages that are already there, instead of staying one more
document to read again.

## A page

- The file name says the topic, lowercase with dashes: `wiki/nordica-crediti.md`, `wiki/requirements-review.md`.
- Front matter with `title:`; then `## TL;DR` (at most three lines and three points, written last): whoever reads only
  that must come away with the essentials.
- **One topic per page**: a concept, a person or an organisation, a process, the summary of a source
  (`wiki/source-<name-of-the-source>.md`).
- Every statement says where it comes from: `(source: [minutes of 12/03](../sources/minutes-2027-03-12.md), § Decisions)`.
- It links to the nearby pages instead of repeating them: `[the review](requirements-review.md)`.
- At the bottom `## History`: one line for every change that matters, with the date and the source that brought it.

## The index `wiki/index.md`

One table per kind of page (concepts, people and organisations, processes, sources): **page** (the link), **one line
that says what is in it**. Every page of the wiki is in the index, and every index entry has its page. Whoever looks for
something starts here.

## The log `wiki/log.md`

Entries are added at the bottom, never rewritten. One entry per operation:

```
## [2027-03-14] source | minutes-2027-03-12.md
- New: wiki/source-minutes-2027-03-12.md
- Updated: wiki/nordica-crediti.md, wiki/requirements-review.md
```

The actions are `source` (a source brought into the wiki), `page` (a page written or fixed by hand), `check` (a check
by the librarian). A source in `sources/` that the log does not name is a **new** source.

## What the reviewer checks

The pages just written or updated, one by one: the source of every statement is there and really says so; the TL;DR is
enough on its own; the page is in the index and links to the nearby ones; it does not contradict another page; the name
says the topic.

## What the librarian checks

The whole wiki: pages that contradict each other; statements superseded by a newer source; orphan pages (no page links
to them); concepts named in several pages without a page of their own; broken links; index and pages that do not match;
log entries without the page they name.
