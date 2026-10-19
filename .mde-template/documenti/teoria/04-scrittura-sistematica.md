---
title: La scrittura sistematica
---

# La scrittura sistematica

## TL;DR

Un wiki è utile solo se ogni documento si legge allo stesso modo. Le convenzioni di MdExplorer sono poche: un TL;DR in
cima, un argomento per documento, titoli che dicono il contenuto, rimandi invece di ripetizioni, decisioni con la data.
- Il TL;DR viene prima di tutto: tre righe e tre punti, scritto per ultimo.
- Un documento si aggiorna, non si duplica.
- Diagrammi e slide hanno le loro skill: `mde-plantuml` e `mde-slide`.

## Il TL;DR in cima

Ogni documento narrativo (un'analisi, una sintesi, una pagina del wiki) comincia con una sezione `## TL;DR`:
**al massimo tre righe di testo, poi esattamente tre punti**.

Il TL;DR deve bastare da solo: chi legge solo quello deve uscirne con il senso del documento intero. Per questo si scrive
**per ultimo**, quando il resto è finito.

È la regola della skill `mde-doc` di MdExplorer, che gli agenti seguono quando scrivono. Non vale per i README, che hanno
la loro skill, `mde-readme`, pensata per gli esempi di comandi che MdExplorer sa eseguire.

## Un documento, un argomento

Una pagina sui requisiti di sicurezza parla dei requisiti di sicurezza. Se ti accorgi che stai scrivendo anche del
calendario delle consegne, quello è un altro documento, con un rimando fra i due.

Un documento con un solo argomento si trova, si aggiorna e si controlla facilmente. Uno che parla di tutto non lo legge
nessuno fino in fondo.

## Titoli che dicono il contenuto

- No: «Note», «Varie», «Documento 3».
- Sì: «Requisiti bloccanti della gara NC-2027-014», «Perché abbiamo scelto PostgreSQL».

Lo stesso vale per i nomi dei file: `requisiti-sicurezza.md`, non `doc1.md`. Il titolo e il nome del file sono la prima
cosa che si vede nell'indice e nell'albero dei documenti.

## Rimandare invece di ripetere

Se un'informazione sta già in una pagina, non la si ricopia: ci si rimanda con un link relativo. Due copie della stessa
informazione prima o poi divergono, e allora una delle due è sbagliata senza che nessuno lo sappia.

Se ti serve un pezzo di un altro file dentro il documento, MdExplorer ha comandi per includerlo invece di copiarlo: li
descrive la skill `mde-features`.

## Le decisioni hanno una data

Una decisione si scrive con la data, chi l'ha presa e il perché:

```markdown
| Data | Decisione | Chi | Perché |
|---|---|---|---|
| 2026-11-03 | Partecipiamo alla gara | Direzione | i requisiti bloccanti sono tutti coperti |
```

Fra un anno qualcuno chiederà «perché abbiamo fatto così?». La risposta deve esserci.

## Aggiornare, non duplicare

Quando una cosa cambia, si aggiorna la pagina che ne parla. Non si crea «requisiti-sicurezza-v2.md». La storia delle
versioni la tiene git: ogni commit dice che cosa è cambiato, e si può sempre vedere la pagina com'era.

Se una pagina intera non vale più (un progetto chiuso, una procedura abbandonata), la si segna come superata in cima,
con la data e il rimando a quella che la sostituisce, e la si toglie dall'indice principale.

## I diagrammi

Un diagramma spesso spiega più di una pagina di testo. In MdExplorer si scrivono in PlantUML, dentro il documento, così
cambiano insieme al testo. La skill `mde-plantuml` dice come disegnarli con colori sobri, leggibili anche in tema scuro,
con le convenzioni di ogni tipo (flusso, sequenza, classi, schema dei dati, mappa mentale).

## Le slide

Quando un argomento va presentato, le slide si scrivono in markdown, nello stesso progetto, con la skill `mde-slide`. Una
presentazione che rimanda alle pagine del wiki resta allineata con quello che il gruppo sa.

## Una lista per controllare

- [ ] C'è il `## TL;DR`, con tre righe al massimo e tre punti.
- [ ] Il documento parla di una cosa sola, e il titolo la dice.
- [ ] Ogni affermazione importante cita la sua fonte.
- [ ] Le informazioni che stanno altrove sono rimandi, non copie.
- [ ] Le decisioni hanno data, autore e motivo.
- [ ] La pagina è nell'indice.
