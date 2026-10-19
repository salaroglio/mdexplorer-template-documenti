---
title: Le tre operazioni
---

# Le tre operazioni

## TL;DR

Il wiki vive di tre operazioni: l'ingest porta dentro una fonte nuova, la query risponde a una domanda partendo dal wiki,
il lint controlla che il wiki sia sano. Ognuna lascia una voce nel registro.
- Ingest: una fonte, una sintesi, e tutte le pagine di concetto che tocca.
- Query: prima l'indice, poi le pagine; una buona risposta diventa una pagina.
- Lint: contraddizioni, affermazioni superate, pagine orfane, collegamenti mancanti o rotti.

## Ingest: entra una fonte nuova

Arriva un documento: un verbale, un capitolato, una mail importante. Lo metti in `fonti/`. Poi:

1. **Si legge la fonte, tutta.** Se qualcosa non è chiaro, si chiede a chi l'ha portata, prima di scrivere.
2. **Si scrive la sintesi** in `wiki/fonte-<nome>.md`: che cosa dice, che cosa ha di nuovo, che cosa contraddice.
3. **Si aggiornano le pagine di concetto** che la fonte tocca. Un concetto nuovo ha diritto a una pagina nuova.
4. **Si aggiorna l'indice**: la sintesi e le pagine nuove ci entrano.
5. **Si scrive la voce nel registro**, con l'elenco delle pagine toccate.

Una fonte sola può cambiare molte pagine. È normale, ed è il punto: la conoscenza nuova va dove serve, non resta chiusa
nella sintesi.

Un esempio. Arriva il verbale di una riunione con il cliente: il cliente ha spostato la scadenza e aggiunto un requisito
di sicurezza. L'ingest produce la sintesi del verbale, aggiorna la pagina del cliente (nuova scadenza, con la fonte),
crea o aggiorna la pagina del requisito, aggiunge due righe all'indice e una voce al registro.

## Query: una domanda al wiki

Qualcuno chiede: «Quali requisiti bloccanti ha la gara NC-2027-014?». Il modo giusto di rispondere:

1. **Si parte dall'indice**, per trovare le pagine giuste.
2. **Si leggono quelle pagine**, e solo se serve si scende alle fonti che citano.
3. **Si risponde citando le pagine e le fonti.** Se il wiki non lo sa, lo si dice.

Se la risposta è buona e servirà ancora, la si **salva come pagina** del wiki, con il suo link nell'indice. Così la
prossima volta la risposta c'è già. Un confronto fra due fornitori, una tabella delle scadenze, una spiegazione chiesta
tre volte: sono tutte candidate.

Se la query trova un buco (il wiki non sa una cosa che le fonti dicono), è un lavoro per un nuovo ingest o per
l'aggiornamento di una pagina.

## Lint: il controllo di salute

Ogni tanto, e sempre prima di una consegna importante, si controlla il wiki. Si cerca:

- **Contraddizioni**: due pagine che dicono cose diverse sullo stesso fatto.
- **Affermazioni superate**: una pagina che riporta una scadenza vecchia, quando una fonte più recente l'ha cambiata.
- **Pagine orfane**: pagine che nessun'altra pagina e nemmeno l'indice raggiunge.
- **Concetti senza pagina**: un termine che torna in molte pagine ma non ha una pagina sua.
- **Collegamenti mancanti**: una pagina nomina un concetto che ha la sua pagina, ma non ci rimanda.
- **Collegamenti rotti**: un link che porta a un file che non c'è più.
- **Pagine senza fonte o senza TL;DR**.

Il lint non corregge di nascosto: produce un elenco, con per ogni voce la pagina, il problema e la correzione proposta.
Chi risponde del wiki decide che cosa fare. Poi la voce nel registro dice che cosa è stato trovato e che cosa sistemato.

## Il registro, ogni volta

Le tre operazioni finiscono tutte allo stesso modo, con una voce in `wiki/registro.md`:

```markdown
## [2026-11-10] controllo | revisioni/controllo-2026-11-10.md
- 2 contraddizioni sulla scadenza: corretta wiki/nordica-crediti.md
- 1 pagina orfana: aggiunta all'indice
```

## Chi fa che cosa

In MdExplorer le tre operazioni hanno un agente di riferimento: il redattore fa l'ingest, il revisore controlla quello che
il redattore ha scritto, il bibliotecario fa il lint, indice e registro compresi. Le persone approvano. Il dettaglio è nel
[capitolo 5](05-redattore-revisore-bibliotecario.md).
