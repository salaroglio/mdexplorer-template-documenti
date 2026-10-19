---
title: Imparare con il MarkAgent
---

# Imparare con il MarkAgent

## TL;DR

Il MarkAgent è l'assistente di MdExplorer con cui parli: conosce il progetto e legge questa teoria. Puoi chiedergli di
spiegarti un capitolo, di proporti una struttura, di fare con te il primo ingest o un controllo di salute.
- Prima di cambiare un file te lo chiede.
- Impara meglio facendo: comincia da una fonte vera del tuo progetto.
- La teoria di altri metodi si scarica anche dopo, dalle impostazioni o chiedendola a lui.

## Che cosa sa

Il MarkAgent legge i documenti del progetto come li leggi tu, compresa questa cartella. Non ricorda le conversazioni
passate: quello che deve restare va scritto nel wiki. È proprio l'idea del [capitolo 1](01-perche-un-wiki-per-llm.md).

## Farsi spiegare

Qualche domanda per cominciare:

- «Spiegami in parole semplici che cos'è un wiki per LLM.»
- «Spiegami il capitolo 2 della teoria e fammi un esempio sul nostro progetto.»
- «Che differenza c'è fra una pagina di concetto e una pagina di sintesi?»
- «Fammi tre domande per vedere se ho capito il capitolo 3.»

L'ultima è la più utile: rispondere a una domanda fissa le cose più che leggerle.

## Farsi proporre una struttura

Quando il progetto è nuovo, chiedi:

- «Guarda i documenti che ho già e proponimi gli argomenti dell'indice.»
- «Proponimi le prime cinque pagine di concetto, con una riga ciascuna.»
- «Scrivi nel file d'istruzioni le regole del nostro wiki: cartelle, argomenti, che cosa non ci entra.»

Il MarkAgent propone; tu correggi e confermi. Le regole scritte nel file d'istruzioni varranno poi per tutti gli agenti.

## Il primo ingest insieme

Il modo migliore di imparare l'ingest è farlo una volta con calma:

1. Metti una fonte vera in `fonti/`, per esempio l'ultimo verbale.
2. Chiedi: «Facciamo l'ingest di questo verbale passo per passo: dimmi che cosa faresti prima di farlo.»
3. Leggi la proposta: sintesi, pagine da toccare, righe dell'indice, voce del registro.
4. Correggi quello che non ti torna, poi dai il via.
5. Rileggi il risultato con il [capitolo 4](04-scrittura-sistematica.md) accanto.

Dal secondo ingest in poi puoi affidarlo al redattore, e usare il MarkAgent per le domande.

## Il controllo di salute

- «Fai un lint del wiki e dimmi le tre cose più urgenti.»
- «Ci sono pagine che si contraddicono sulla scadenza della gara?»
- «Quali pagine non sono nell'indice?»

Il MarkAgent risponde con un elenco. Le correzioni le fai tu, o le chiedi a lui una per una.

## Prima di cambiare, chiede

Il MarkAgent può leggere tutto, ma prima di modificare o creare un file ti dice che cosa vuole fare e aspetta il tuo sì.
Se non sei sicuro, chiedigli di mostrarti prima il testo che scriverebbe.

## La teoria degli altri metodi

Se il tuo progetto ha anche altri metodi (per esempio le ontologie o la ISO 9001), anche loro hanno una teoria. Se non
l'hai presa alla creazione, puoi averla dopo:

- da **Impostazioni del progetto → Metodi del progetto → «Scarica la teoria»**, sulla riga del metodo;
- oppure dal MarkAgent: quando si accorge che gli servirebbe, te la propone e, con il tuo permesso, la scarica con lo
  strumento `add_theory`.

La teoria arriva nella versione del metodo che il progetto usa, con un commit suo, e finisce in `teoria/<metodo>/`, come
questa.

## Se qualcosa non torna

Se una risposta del MarkAgent non corrisponde a quello che leggi qui, diglielo e indicagli il capitolo. La teoria
scritta vale più del suo ricordo. E se è la teoria a essere sbagliata o poco chiara per il tuo gruppo, correggila: è tua.
