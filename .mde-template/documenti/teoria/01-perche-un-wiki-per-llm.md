---
title: Perché un wiki per un LLM
---

# Perché un wiki per un LLM

## TL;DR

Un LLM che rilegge ogni volta tutte le fonti non impara niente da una domanda all'altra. L'idea del wiki per LLM,
proposta da Andrej Karpathy, è far scrivere all'LLM un wiki che cresce e si corregge, così la conoscenza si accumula.
MdExplorer la adotta e ci aggiunge persone che approvano, git e agenti con ruoli precisi.
- Tre strati: le fonti (intatte), il wiki (curato), le regole (scritte).
- La conoscenza si accumula nelle pagine, non nella memoria della chat.
- In MdExplorer chi decide restano le persone: gli agenti preparano.

## Il problema di partenza

Quando chiedi qualcosa a un assistente su un insieme di documenti, di solito succede questo: l'assistente cerca i pezzi
che sembrano pertinenti, li legge, risponde. È il modo detto RAG, *retrieval augmented generation*.

Funziona, ma ha un limite. Ogni domanda riparte da zero. Se ieri l'assistente ha capito che due verbali si
contraddicono, oggi non lo sa più. Se una sintesi era buona, non resta da nessuna parte. Il lavoro di comprensione si
perde alla fine di ogni conversazione.

## L'idea di Karpathy

Nell'aprile 2026 Andrej Karpathy ha descritto un modo diverso, in un gist intitolato «LLM Wiki»:
<https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f>.

L'idea, in breve: invece di rileggere le fonti a ogni domanda, l'LLM **scrive e mantiene un wiki**. Quando arriva una
fonte nuova, la legge una volta, ne fa una sintesi, aggiorna le pagine dei concetti che tocca, e annota che cosa ha fatto.
Le domande successive partono dal wiki, che è già ordinato. Il wiki migliora con l'uso: la conoscenza si accumula.

Karpathy distingue tre strati:

1. **Le fonti**: i documenti originali. L'LLM li legge ma non li modifica mai.
2. **Il wiki**: le pagine scritte dall'LLM, con un indice e un registro delle modifiche.
3. **Lo schema**: le regole su come è fatto il wiki e come lo si tiene, scritte in un file d'istruzioni che l'LLM legge
   sempre.

E tre operazioni: aggiungere una fonte (*ingest*), interrogare il wiki (*query*), controllarne la salute (*lint*). Le
trovi nel [capitolo 3](03-le-tre-operazioni.md).

Per i dettagli vai al gist originale: qui ne riportiamo il senso, non le parole.

## Che cosa ci aggiunge MdExplorer

L'idea di Karpathy pensa a una persona sola con il suo LLM. In un gruppo di lavoro servono alcune cose in più. Quelle che
seguono sono scelte di MdExplorer, non parte del gist:

- **Le persone approvano.** Un agente prepara una pagina o una correzione; chi risponde di quel lavoro la legge e la
  accetta. Il wiki non cambia alle spalle del gruppo.
- **Git tiene la storia.** Ogni modifica è un commit: si vede chi ha cambiato che cosa, e si può tornare indietro.
- **Tre ruoli invece di un LLM tuttofare.** Un redattore scrive, un revisore controlla, un bibliotecario tiene in ordine
  indice e registro. Ne parla il [capitolo 5](05-redattore-revisore-bibliotecario.md).
- **Convenzioni di scrittura comuni.** Ogni documento comincia con un TL;DR, parla di una cosa sola, rimanda invece di
  ripetere. Sono nel [capitolo 4](04-scrittura-sistematica.md).
- **Lo schema sono i file d'istruzioni del progetto**: `CLAUDE.md`, `AGENTS.md` o `copilot-instructions.md`, secondo il
  motore che usi. MdExplorer ci scrive il blocco del metodo; il resto è del gruppo.

## Perché conviene

- Le risposte partono da pagine già verificate, non da frammenti.
- Una contraddizione trovata una volta resta scritta.
- Chi arriva nel gruppo legge il wiki e capisce, senza dover chiedere tutto.
- L'LLM lavora meglio: legge meno, e legge cose ordinate.

## Quando non serve

Se i documenti sono pochi e cambiano di rado, un buon README basta. Il wiki rende quando le fonti sono tante, arrivano
nel tempo, e più persone ci lavorano.
