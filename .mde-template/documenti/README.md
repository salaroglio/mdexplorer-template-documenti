---
title: Document Driven Development
---

# Document Driven Development

## TL;DR

Lo strato comune di ogni progetto composto in MdExplorer: un wiki del progetto scritto e tenuto in ordine con gli agenti,
come suggerisce l'idea degli LLM wiki. Le fonti restano intatte, le pagine crescono a ogni fonte nuova, l'indice e il
registro dicono che cosa c'è e che cosa è cambiato.

- Si prende sempre, alla creazione di un progetto composto; i metodi (Ontologie, ISO 9001) si aggiungono sopra.
- Tre agenti preparano (redattore, revisore, bibliotecario); il responsabile della documentazione approva e decide.
- La teoria, se la chiedi, arriva in `teoria/documenti/`: si legge da soli o con il MarkAgent.

## Che cosa porta

| Che cosa | Dove |
|---|---|
| I due workflow: una fonte nel wiki, il controllo del wiki | `workflows/` |
| Le schede dei tre agenti | `agents/` |
| Il ruolo: Responsabile della documentazione | il documento delle responsabilità del progetto, come ruolo aperto |
| Le istruzioni per gli agenti del progetto | un blocco in `CLAUDE.md`, `AGENTS.md`, `copilot-instructions.md` |
| I file iniziali del gruppo | `fonti/`, `wiki/indice.md`, `wiki/registro.md`, `revisioni/` |
| La skill delle convenzioni del wiki | `.claude/skills/documenti-wiki/` |
| La teoria degli LLM wiki | `teoria/`, copiata in `teoria/documenti/` se la chiedi |

## Come si comincia

1. Chi risponde della documentazione prende il ruolo nel documento delle responsabilità (o dice «È mio» nella città degli agenti).
2. Metti in `fonti/` un documento da cui partire: un verbale, una specifica, una mail esportata.
3. Lancia il redattore («Una fonte nel wiki»): legge la fonte, scrive o aggiorna le pagine, l'indice e il registro.
4. Ogni tanto lancia il bibliotecario («Il controllo del wiki»): trova contraddizioni, pagine orfane, collegamenti rotti.
