---
mde_type: workflow
title: The wiki check
workflow: check.workflow.json
---

# The wiki check

## TL;DR

Every now and then the wiki is checked as a whole, the way a librarian would: contradictions, superseded statements,
pages nobody links, concepts without a page, broken links. The librarian writes the report, the documentation owner
decides what gets fixed.

- The documentation owner launches it, for example after a few new sources or before a delivery.
- The librarian does not fix: it proposes. The fixes are made by the editor with a source, or by the person by hand.
- The report stays in `reviews/`, the round in the round log.

## The round

```plantuml(@workflow, ./check.workflow.json)
```

## Who does what

| Step | Who works | What they deliver | Who approves |
|---|---|---|---|
| Check the wiki | librarian agent | `reviews/check-<date>.md` | the documentation owner |
| Decide the fixes | the documentation owner | the decision, in the round log | — |
