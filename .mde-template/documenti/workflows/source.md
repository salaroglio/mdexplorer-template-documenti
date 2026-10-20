---
mde_type: workflow
title: A source into the wiki
workflow: source.workflow.json
---

# A source into the wiki

## TL;DR

A new source in `sources/` enters the wiki: the editor writes or updates the pages it touches, the index and the log;
the reviewer reads them again against the sources and the conventions; the documentation owner decides.

- The documentation owner launches the editor when there is something new in `sources/`.
- The review starts by itself; pages to fix are redone when the person presses «Restart».
- Every round stays in the round log and in git: who wrote, who reviewed, who accepted.

## The round

```plantuml(@workflow, ./source.workflow.json)
```

## Who does what

| Step | Who works | What they deliver | Who approves |
|---|---|---|---|
| Bring the sources into the wiki | editor agent | the pages in `wiki/`, the index, the log | the documentation owner |
| Review | reviewer agent | `reviews/review-<date>.md` | the documentation owner |
| Accept the pages | the documentation owner | the decision, in the round log | — |
