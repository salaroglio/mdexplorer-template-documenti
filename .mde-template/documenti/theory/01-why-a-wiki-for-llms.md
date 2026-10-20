---
title: Why a wiki for an LLM
---

# Why a wiki for an LLM

## TL;DR

An LLM that reads all the sources again every time learns nothing from one question to the next. The idea of the LLM
wiki, proposed by Andrej Karpathy, is to have the LLM write a wiki that grows and corrects itself, so knowledge piles up.
MdExplorer adopts it and adds people who approve, git, and agents with precise roles.
- Three layers: the sources (untouched), the wiki (curated), the rules (written).
- Knowledge piles up in the pages, not in the memory of the chat.
- In MdExplorer the people still decide: the agents prepare.

## The starting problem

When you ask an assistant something about a set of documents, this is what usually happens: the assistant looks for the
pieces that seem relevant, reads them, answers. It is the approach called RAG, *retrieval augmented generation*.

It works, but it has a limit. Every question starts from scratch. If yesterday the assistant understood that two sets
of minutes contradict each other, today it no longer knows. If a summary was good, it is not kept anywhere. The work of
understanding is lost at the end of every conversation.

## Karpathy's idea

In April 2026 Andrej Karpathy described a different approach, in a gist called «LLM Wiki»:
<https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f>.

The idea, in short: instead of reading the sources again for every question, the LLM **writes and maintains a wiki**.
When a new source arrives, it reads it once, summarises it, updates the pages of the concepts it touches, and notes what
it did. The following questions start from the wiki, which is already in order. The wiki gets better with use:
knowledge piles up.

Karpathy distinguishes three layers:

1. **The sources**: the original documents. The LLM reads them but never modifies them.
2. **The wiki**: the pages written by the LLM, with an index and a log of the changes.
3. **The schema**: the rules on how the wiki is made and kept, written in an instructions file the LLM always reads.

And three operations: adding a source (*ingest*), querying the wiki (*query*), checking its health (*lint*). You find
them in [chapter 3](03-the-three-operations.md).

For the details go to the original gist: here we report its sense, not its words.

## What MdExplorer adds

Karpathy's idea has in mind one person with their LLM. A working group needs a few things more. The ones below are
MdExplorer's choices, not part of the gist:

- **People approve.** An agent prepares a page or a fix; whoever answers for that work reads it and accepts it. The wiki
  does not change behind the group's back.
- **Git keeps the history.** Every change is a commit: you see who changed what, and you can go back.
- **Three roles instead of an all-purpose LLM.** An editor writes, a reviewer checks, a librarian checks the wiki as a
  whole, index and log included. [Chapter 5](05-editor-reviewer-librarian.md) is about them.
- **Shared writing conventions.** Every document starts with a TL;DR, talks about one thing, links instead of repeating.
  They are in [chapter 4](04-systematic-writing.md).
- **The schema is the project's instructions file**: `CLAUDE.md`, `AGENTS.md` or `copilot-instructions.md`, depending on
  the engine you use. MdExplorer writes the method's block there; the rest belongs to the group.

## Why it pays

- Answers start from pages already checked, not from fragments.
- A contradiction found once stays written down.
- Whoever joins the group reads the wiki and understands, without having to ask everything.
- The LLM works better: it reads less, and reads things in order.

## When you do not need it

If the documents are few and rarely change, a good README is enough. The wiki pays off when the sources are many, arrive
over time, and several people work on them.
