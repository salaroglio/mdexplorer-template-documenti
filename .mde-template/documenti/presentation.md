---
document_type: slides
reveal:
  theme: mde-space
---

<!-- .slide: data-background-image="/mde-space/sfondi/luna.svg" class="mde-cielo" -->
<img class="mde-icona-grande" src="/mde-space/icone/base.svg" alt="">

# Systematic writing of documents

The **common layer** of every composed project:
the project's wiki, written and kept in order with the agents.

---

## <img class="mde-icona" src="/mde-space/icone/telescopio.svg" alt=""> What it is for

- A project's documents pile up, and every time someone, a person or an LLM, reads them again from scratch
- Here the sources become a **wiki that grows**: every new source enriches pages that are already there
- The **index** says what is there, the **log** what changed, git who did what

---

## <img class="mde-icona" src="/mde-space/icone/satellite.svg" alt=""> Three layers

1. **The sources** in `sources/`: minutes, specifications, emails. Never touched
2. **The wiki** in `wiki/`: one page per topic, with TL;DR, cited sources and links
3. **The conventions**: the `documenti-wiki` skill and the project's instructions

---

## <img class="mde-icona" src="/mde-space/icone/astronauta.svg" alt=""> Who does what

- **Editor**: brings the new sources into the wiki, with index and log
- **Reviewer**: reads the pages again against the sources and says what to fix
- **Librarian**: checks the whole wiki, contradictions and orphan pages included
- The **documentation owner** approves and decides

---

## <img class="mde-icona" src="/mde-space/icone/cometa.svg" alt=""> Two rounds

- **A source into the wiki**: editor → reviewer → the person accepts, or sends it back
- **The wiki check**: librarian → the person decides what to fix

---

## <img class="mde-icona" src="/mde-space/icone/stella.svg" alt=""> The theory

If you ask for it, it lands in `theory/documenti/` (in an Italian project, `teoria/documenti/`): why a wiki for an LLM,
how it is made, the three operations, the writing conventions, the roles, how to learn with the MarkAgent.

It can also be downloaded later, from the project settings.

---

<!-- .slide: data-background-image="/mde-space/sfondi/razzo.svg" class="mde-sinistra" -->

## <img class="mde-icona" src="/mde-space/icone/bandiera.svg" alt=""> What you find in the project

- `sources/`, `wiki/index.md`, `wiki/log.md`, `reviews/`
- three agents and the documentation owner's role, nobody's yet
- on top, the methods you choose: Ontologies, ISO 9001
