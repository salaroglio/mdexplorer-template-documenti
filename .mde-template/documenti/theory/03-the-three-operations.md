---
title: The three operations
---

# The three operations

## TL;DR

The wiki lives on three operations: the ingest brings in a new source, the query answers a question starting from the
wiki, the lint checks that the wiki is healthy. Each one leaves an entry in the log.
- Ingest: one source, one summary, and all the concept pages it touches.
- Query: first the index, then the pages; a good answer becomes a page.
- Lint: contradictions, superseded statements, orphan pages, missing or broken links.

## Ingest: a new source comes in

A document arrives: minutes, a tender specification, an important email. You put it in `sources/`. Then:

1. **The source is read, all of it.** If something is unclear, you ask whoever brought it, before writing.
2. **The summary is written** in `wiki/source-<name>.md`: what it says, what it has that is new, what it contradicts.
3. **The concept pages the source touches are updated.** A new concept deserves a new page.
4. **The index is updated**: the summary and the new pages go into it.
5. **The log entry is written**, with the list of the pages touched.

A single source can change many pages. That is normal, and it is the point: the new knowledge goes where it is needed,
it does not stay closed in the summary.

An example. The minutes of a meeting with the client arrive: the client moved the deadline and added a security
requirement. The ingest produces the summary of the minutes, updates the client's page (new deadline, with the source),
creates or updates the requirement's page, adds two lines to the index and one entry to the log.

## Query: a question to the wiki

Someone asks: «Which blocking requirements does tender NC-2027-014 have?». The right way to answer:

1. **Start from the index**, to find the right pages.
2. **Read those pages**, and go down to the sources they cite only if needed.
3. **Answer citing the pages and the sources.** If the wiki does not know, say so.

If the answer is good and will be needed again, **save it as a page** of the wiki, with its link in the index. Next
time the answer is already there. A comparison between two suppliers, a table of deadlines, an explanation asked three
times: they are all candidates.

If the query finds a gap (the wiki does not know something the sources say), it is work for a new ingest or for the
update of a page.

## Lint: the health check

Every now and then, and always before an important delivery, the wiki is checked. You look for:

- **Contradictions**: two pages that say different things about the same fact.
- **Superseded statements**: a page that reports an old deadline, when a more recent source changed it.
- **Orphan pages**: pages that no other page, and not even the index, reaches.
- **Concepts without a page**: a term that comes back in many pages but has no page of its own.
- **Missing links**: a page names a concept that has its own page, but does not link to it.
- **Broken links**: a link that leads to a file that is no longer there.
- **Pages without a source or without a TL;DR**.

The lint does not fix things behind your back: it produces a list, with the page, the problem and the proposed fix for
each item. Whoever answers for the wiki decides what to do. Then the log entry says what was found and what was fixed.

## The log, every time

The three operations all end the same way, with an entry in `wiki/log.md`:

```markdown
## [2026-11-10] check | reviews/check-2026-11-10.md
- 2 contradictions on the deadline: fixed wiki/nordica-crediti.md
- 1 orphan page: added to the index
```

## Who does what

In MdExplorer the three operations have a reference agent: the editor does the ingest, the reviewer checks what the
editor wrote, the librarian does the lint, index and log included. People approve. The details are in
[chapter 5](05-editor-reviewer-librarian.md).
