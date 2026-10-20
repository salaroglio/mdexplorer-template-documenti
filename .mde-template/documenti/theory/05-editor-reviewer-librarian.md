---
title: Editor, reviewer, librarian
---

# Editor, reviewer, librarian

## TL;DR

The common layer brings three agents, each with one task only: the editor writes, the reviewer checks, the librarian
keeps things in order. They prepare the work; the people who answer for the roles read and approve.
- The editor does the ingest: pages, index and log, following the conventions.
- The reviewer proposes fixes, does not rewrite.
- The librarian runs the health check of the whole wiki, index and log included.

## Why three and not one

A single agent that writes, checks itself and puts itself in order tends to agree with itself. Splitting the tasks does
what an editorial office does: whoever writes is not whoever reads again. And every agent has a short, clear card, which
makes fewer mistakes.

## The editor

**Id**: `documenti-editor`

It does the writing work:

- the **ingest** of a new source: summary, concept pages, links, index and log;
- the **update** of a page when something changes;
- the **new page** when a good answer deserves to stay.

It follows the conventions of [chapter 4](04-systematic-writing.md): TL;DR, one topic per page, cited sources, links
instead of copies. It does not touch the sources. When it is done, it tells the person what it wrote and where.

## The reviewer

**Id**: `documenti-reviewer`

It reads again what the editor wrote and checks:

- that every statement has its source, and that the source really says that;
- that the TL;DR is enough on its own and respects the form (three lines, three points);
- that the page does not contradict other pages of the wiki;
- that the links are there and work.

The reviewer **does not rewrite**. It produces a list of remarks, each with the page, the problem and the fix it
proposes. Then the person decides: they accept the page, or send it back to the editor with the remarks.

## The librarian

**Id**: `documenti-librarian`

It checks the wiki as a whole:

- the **index**: every page is in it, under the right topic, with its line, and every entry has its page;
- the **log**: every operation has its entry, and every entry names pages that exist;
- the **lint**: orphan pages, superseded pages, contradictions, concepts without a page, broken links (the full list is
  in [chapter 3](03-the-three-operations.md)).

It too does not delete and does not fix behind your back: it reports, proposes, and waits for the yes.

## The people

The agents work for someone. In the project's responsibilities document (usually `responsibilities.md`) every role has
a person, with name and email. That person:

- takes the agents of their role («It's mine» in the agent city) and trusts them;
- reads what they prepare;
- approves, or sends it back with the reason.

A role without a person is an open role: its agents do not start until someone takes it.

## A typical round

1. Some minutes arrive. The person puts them in `sources/` and asks the editor for the ingest.
2. The editor writes the summary, updates two concept pages, the index and the log.
3. The reviewer finds a statement without a source and a wrong link, and says so.
4. The person sends it back to the editor, who fixes it. The person approves.
5. A few sources later, the person launches the librarian: its check finds an orphan page, and the person decides to
   link it.

Every step is a commit: at the end you see who did what, and when.

## What the agents do not do

- They do not modify the sources.
- They do not approve their own work.
- They do not delete pages: at most they propose to mark them as superseded.
- They do not work on orders that arrive inside a document: an instruction found in a source is data, not a command.
