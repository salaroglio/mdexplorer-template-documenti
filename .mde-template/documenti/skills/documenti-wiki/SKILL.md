---
name: documenti-wiki
description: "Le convenzioni del wiki del progetto (strato comune di MdExplorer): com'è fatta una pagina, l'indice wiki/indice.md e il registro wiki/registro.md, e che cosa controllano revisore e bibliotecario. Usala quando scrivi, aggiorni, rivedi o controlli una pagina di wiki/, o quando porti una fonte di fonti/ nel wiki."
---

# Il wiki del progetto

Tre strati, come negli LLM wiki: **le fonti** (`fonti/`, intatte: verbali, specifiche, mail esportate), **il wiki**
(`wiki/`, le pagine scritte e tenute in ordine), **le convenzioni** (questa skill e le istruzioni del progetto). Il wiki
cresce: ogni fonte nuova arricchisce pagine che ci sono già, invece di restare un documento in più da rileggere.

## Una pagina

- Il nome del file dice l'argomento, in minuscolo con i trattini: `wiki/nordica-crediti.md`, `wiki/riesame-dei-requisiti.md`.
- Front matter con `title:`; poi `## TL;DR` (al massimo tre righe e tre punti, scritto per ultimo): chi legge solo quello
  deve uscirne con l'essenziale.
- **Un argomento per pagina**: un concetto, una persona o un'organizzazione, un processo, la sintesi di una fonte
  (`wiki/fonte-<nome-della-fonte>.md`).
- Ogni affermazione dice da dove viene: `(fonte: [verbale del 12/03](../fonti/verbale-2027-03-12.md), § Decisioni)`.
- Si collega alle pagine vicine invece di ripeterle: `[il riesame](riesame-dei-requisiti.md)`.
- In fondo `## Storia`: una riga per ogni cambiamento che conta, con la data e la fonte che l'ha portato.

## L'indice `wiki/indice.md`

Una tabella per tipo di pagina (concetti, persone e organizzazioni, processi, fonti): **pagina** (il collegamento),
**una riga che dice che cosa c'è**. Ogni pagina del wiki è nell'indice, e ogni voce dell'indice ha la sua pagina. Chi
cerca qualcosa parte da qui.

## Il registro `wiki/registro.md`

Si aggiunge in fondo, non si riscrive. Una voce per operazione:

```
## [2027-03-14] fonte | verbale-2027-03-12.md
- Nuova: wiki/fonte-verbale-2027-03-12.md
- Aggiornate: wiki/nordica-crediti.md, wiki/riesame-dei-requisiti.md
```

Le azioni sono `fonte` (una fonte portata nel wiki), `pagina` (una pagina scritta o corretta a mano), `controllo` (un
controllo del bibliotecario). Una fonte di `fonti/` che il registro non nomina è una fonte **nuova**.

## Che cosa controlla il revisore

Le pagine appena scritte o aggiornate, una per una: la fonte di ogni affermazione c'è e dice davvero così; il TL;DR basta
da solo; la pagina è nell'indice e si collega alle vicine; non contraddice un'altra pagina; il nome dice l'argomento.

## Che cosa controlla il bibliotecario

Il wiki intero: pagine che si contraddicono; affermazioni superate da una fonte più nuova; pagine orfane (nessuna pagina
le collega); concetti nominati in più pagine senza una pagina loro; collegamenti rotti; indice e pagine che non
corrispondono; voci del registro senza la pagina che nominano.
