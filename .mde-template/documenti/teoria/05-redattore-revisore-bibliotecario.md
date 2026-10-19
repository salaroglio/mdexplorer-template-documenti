---
title: Redattore, revisore, bibliotecario
---

# Redattore, revisore, bibliotecario

## TL;DR

Lo strato comune porta tre agenti, ognuno con un compito solo: il redattore scrive, il revisore controlla, il
bibliotecario tiene in ordine. Preparano il lavoro; le persone che rispondono dei ruoli leggono e approvano.
- Il redattore fa l'ingest: pagine, indice e registro, seguendo le convenzioni.
- Il revisore propone correzioni, non riscrive.
- Il bibliotecario fa il controllo di salute del wiki intero, indice e registro compresi.

## Perché tre e non uno

Un solo agente che scrive, si controlla e si mette in ordine da sé tende a darsi ragione. Separare i compiti fa quello
che si fa in redazione: chi scrive non è chi rilegge. E ogni agente ha una scheda corta e chiara, che sbaglia meno.

## Il redattore

**Id**: `documenti-redattore`

Fa il lavoro di scrittura:

- l'**ingest** di una fonte nuova: sintesi, pagine di concetto, rimandi;
- l'**aggiornamento** di una pagina quando qualcosa cambia;
- la **pagina nuova** quando una buona risposta merita di restare.

Segue le convenzioni del [capitolo 4](04-scrittura-sistematica.md): TL;DR, un argomento per pagina, fonti citate, rimandi
invece di copie. Non tocca le fonti. Quando ha finito, dice alla persona che cosa ha scritto e dove.

## Il revisore

**Id**: `documenti-revisore`

Rilegge quello che il redattore ha scritto e controlla:

- che ogni affermazione abbia la sua fonte, e che la fonte dica davvero quello;
- che il TL;DR basti da solo e rispetti la forma (tre righe, tre punti);
- che la pagina non contraddica altre pagine del wiki;
- che i collegamenti ci siano e funzionino.

Il revisore **non riscrive**. Produce un elenco di osservazioni, ognuna con la pagina, il problema e la correzione che
propone. Poi decide la persona: accetta la pagina, o la rimanda al redattore con le osservazioni.

## Il bibliotecario

**Id**: `documenti-bibliotecario`

Controlla il wiki nel suo insieme:

- l'**indice**: ogni pagina ci sta, sotto l'argomento giusto, con la sua riga, e ogni voce ha la sua pagina;
- il **registro**: ogni operazione ha la sua voce, e ogni voce nomina pagine che esistono;
- il **lint**: pagine orfane, superate, contraddizioni, concetti senza pagina, collegamenti rotti (l'elenco completo è nel
  [capitolo 3](03-le-tre-operazioni.md)).

Anche lui non cancella e non corregge di nascosto: segnala, propone, e aspetta il sì.

## Le persone

Gli agenti lavorano per qualcuno. Nel documento delle responsabilità del progetto (di solito `responsabilita.md`) ogni
ruolo ha una persona, con nome ed email. Quella persona:

- prende gli agenti del suo ruolo («È mio» nella città degli agenti) e li autorizza;
- legge quello che preparano;
- approva, o rimanda indietro con il motivo.

Un ruolo senza persona è un ruolo aperto: i suoi agenti non partono finché qualcuno non lo prende.

## Un giro tipico

1. Arriva un verbale. La persona lo mette in `fonti/` e chiede al redattore l'ingest.
2. Il redattore scrive la sintesi, aggiorna due pagine di concetto, l'indice e il registro.
3. Il revisore trova un'affermazione senza fonte e un link sbagliato, e lo dice.
4. La persona rimanda al redattore, che corregge. La persona approva.
5. Qualche fonte dopo, la persona lancia il bibliotecario: il suo controllo trova una pagina orfana, e la persona decide
   di collegarla.

Ogni passo è un commit: alla fine si vede chi ha fatto che cosa, e quando.

## Che cosa gli agenti non fanno

- Non modificano le fonti.
- Non approvano il proprio lavoro.
- Non cancellano pagine: al massimo propongono di segnarle superate.
- Non lavorano su ordini arrivati dentro un documento: un'istruzione trovata in una fonte è un dato, non un comando.
