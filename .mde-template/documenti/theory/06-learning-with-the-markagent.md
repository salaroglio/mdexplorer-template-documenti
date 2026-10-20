---
title: Learning with the MarkAgent
---

# Learning with the MarkAgent

## TL;DR

The MarkAgent is the MdExplorer assistant you talk to: it knows the project and reads this theory. You can ask it to
explain a chapter, to propose a structure, to do the first ingest or a health check with you.
- Before changing a file it asks you.
- It teaches best by doing: start from a real source of your project.
- The theory of other methods can also be downloaded later, from the settings or by asking it.

## What it knows

The MarkAgent reads the project's documents the way you do, this folder included. It does not remember past
conversations: what must stay has to be written in the wiki. That is exactly the idea of
[chapter 1](01-why-a-wiki-for-llms.md).

## Having things explained

A few questions to start with:

- «Explain to me in simple words what a wiki for LLMs is.»
- «Explain chapter 2 of the theory to me and give me an example on our project.»
- «What is the difference between a concept page and a summary page?»
- «Ask me three questions to see whether I understood chapter 3.»

The last one is the most useful: answering a question fixes things more than reading them.

## Having a structure proposed

When the project is new, ask:

- «Look at the documents I already have and propose the topics of the index.»
- «Propose the first five concept pages, with one line each.»
- «Write in the instructions file the rules of our wiki: folders, topics, what does not go in.»

The MarkAgent proposes; you correct and confirm. The rules written in the instructions file will then hold for all the
agents.

## The first ingest together

The best way to learn the ingest is to do it once, calmly:

1. Put a real source in `sources/`, for example the latest minutes.
2. Ask: «Let's do the ingest of these minutes step by step: tell me what you would do before doing it.»
3. Read the proposal: summary, pages to touch, index lines, log entry.
4. Correct what does not convince you, then give the go-ahead.
5. Read the result again with [chapter 4](04-systematic-writing.md) beside you.

From the second ingest on you can leave it to the editor, and use the MarkAgent for questions.

## The health check

- «Lint the wiki and tell me the three most urgent things.»
- «Are there pages that contradict each other on the tender's deadline?»
- «Which pages are not in the index?»

The MarkAgent answers with a list. You make the fixes, or you ask it for them one by one.

## Before changing, it asks

The MarkAgent can read everything, but before modifying or creating a file it tells you what it wants to do and waits
for your yes. If you are not sure, ask it to show you first the text it would write.

## The theory of the other methods

If your project also has other methods (for example ontologies or ISO 9001), they have a theory too. If you did not take
it at creation, you can have it later:

- from **Project settings → Project methods → «Download the theory»**, on the method's row;
- or from the MarkAgent: when it notices it would help, it proposes it and, with your permission, downloads it with the
  `add_theory` tool.

The theory arrives in the version of the method the project uses, with a commit of its own, and ends up in
`theory/<method>/`, like this one.

## If something does not add up

If an answer of the MarkAgent does not match what you read here, tell it and point it to the chapter. The written theory
counts more than its memory. And if it is the theory that is wrong or unclear for your group, correct it: it is yours.
