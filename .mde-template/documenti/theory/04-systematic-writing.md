---
title: Systematic writing
---

# Systematic writing

## TL;DR

A wiki is useful only if every document reads the same way. MdExplorer's conventions are few: a TL;DR at the top, one
topic per document, titles that say the content, links instead of repetitions, decisions with their date.
- The TL;DR comes before everything: three lines and three points, written last.
- A document is updated, not duplicated.
- Diagrams and slides have their own skills: `mde-plantuml` and `mde-slide`.

## The TL;DR at the top

Every narrative document (an analysis, a summary, a wiki page) starts with a `## TL;DR` section: **at most three lines
of text, then exactly three points**.

The TL;DR must be enough on its own: whoever reads only that must come away with the sense of the whole document. That
is why it is written **last**, when the rest is finished.

It is the rule of MdExplorer's `mde-doc` skill, which the agents follow when they write. It does not apply to READMEs,
which have their own skill, `mde-readme`, designed for the command examples MdExplorer can run.

## One document, one topic

A page on the security requirements talks about the security requirements. If you notice you are also writing about the
delivery calendar, that is another document, with a link between the two.

A document with a single topic is easy to find, update and check. One that talks about everything is read to the end by
nobody.

## Titles that say the content

- No: «Notes», «Miscellaneous», «Document 3».
- Yes: «Blocking requirements of tender NC-2027-014», «Why we chose PostgreSQL».

The same goes for file names: `security-requirements.md`, not `doc1.md`. The title and the file name are the first thing
you see in the index and in the document tree.

## Link instead of repeating

If a piece of information is already in a page, you do not copy it: you link to it with a relative link. Two copies of
the same information sooner or later diverge, and then one of the two is wrong without anybody knowing.

If you need a piece of another file inside the document, MdExplorer has commands to include it instead of copying it:
the `mde-features` skill describes them.

## Decisions have a date

A decision is written with the date, who took it and why:

```markdown
| Date | Decision | Who | Why |
|---|---|---|---|
| 2026-11-03 | We bid for the tender | Management | the blocking requirements are all covered |
```

In a year someone will ask «why did we do it this way?». The answer must be there.

## Update, do not duplicate

When something changes, you update the page that talks about it. You do not create «security-requirements-v2.md». Git
keeps the history of the versions: every commit says what changed, and you can always see the page as it was.

If a whole page no longer holds (a closed project, an abandoned procedure), you mark it as superseded at the top, with
the date and the link to the one that replaces it, and you remove it from the main index.

## Diagrams

A diagram often explains more than a page of text. In MdExplorer they are written in PlantUML, inside the document, so
they change together with the text. The `mde-plantuml` skill says how to draw them with sober colours, readable in the
dark theme too, with the conventions of each kind (flow, sequence, classes, data schema, mind map).

## Slides

When a topic has to be presented, the slides are written in markdown, in the same project, with the `mde-slide` skill. A
presentation that links to the wiki's pages stays aligned with what the group knows.

## A list to check

- [ ] There is the `## TL;DR`, with at most three lines and three points.
- [ ] The document talks about one thing, and the title says it.
- [ ] Every important statement cites its source.
- [ ] The information that is elsewhere is linked, not copied.
- [ ] Decisions have date, author and reason.
- [ ] The page is in the index.
