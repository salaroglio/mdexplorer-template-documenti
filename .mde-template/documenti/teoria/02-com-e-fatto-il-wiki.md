---
title: Com'è fatto il wiki
---

# Com'è fatto il wiki

## TL;DR

In un progetto di MdExplorer il wiki ha due cartelle: `fonti/`, che nessuno modifica, e `wiki/`, con l'indice, il
registro e una pagina per ogni concetto o fonte. Ogni pagina ha un titolo, un TL;DR e i collegamenti alle pagine vicine.
- `wiki/indice.md` è la porta d'ingresso: da lì si trova tutto.
- `wiki/registro.md` è il diario delle modifiche, una voce per operazione.
- Le fonti restano come sono arrivate: le pagine le citano.

## Le cartelle

```text
fonti/                     i documenti originali: verbali, capitolati, articoli
wiki/
├── indice.md              la mappa del wiki
├── registro.md            il diario delle modifiche
├── nordica-crediti.md     una pagina per ogni concetto, persona, organizzazione o processo
└── fonte-<nome>.md        una pagina di sintesi per ogni fonte letta
revisioni/                 le revisioni del revisore e i controlli del bibliotecario
```

Le pagine stanno tutte nella stessa cartella: è l'indice a dividerle per tipo (concetti, persone e organizzazioni,
processi, fonti), e il nome del file dice l'argomento.

I nomi delle cartelle sono un punto di partenza: se il tuo gruppo preferisce altro, cambiali, ma scrivi la scelta nel
file d'istruzioni del progetto, così gli agenti la seguono.

## Le fonti non si toccano

Una fonte è un documento che arriva da fuori. Si mette in `fonti/` e da lì non cambia più. Se arriva una versione nuova,
entra come file nuovo, con la data nel nome: `fonti/2026-11-03-verbale-riunione.md`.

Perché: le pagine del wiki dicono «secondo il verbale del 3 novembre». Se il verbale cambiasse, quella frase non sarebbe
più verificabile.

Una fonte in PDF o Word va bene lo stesso: la sintesi la cita con il nome del file.

## L'indice

`wiki/indice.md` elenca le pagine del wiki, raggruppate per argomento, ognuna con una riga che dice di che cosa parla.
Un esempio:

```markdown
## Clienti
- [Nordica Crediti](nordica-crediti.md) — il cliente, i contatti, le gare passate
- [Capitolato NC-2027-014](fonte-nc-2027-014.md) — sintesi del capitolato, con i requisiti bloccanti
```

Chi cerca qualcosa, persona o agente, parte da qui. Una pagina che non è nell'indice per il wiki quasi non esiste.

## Il registro

`wiki/registro.md` è un diario che si scrive solo in fondo, senza cancellare. Ogni operazione ha la sua voce:

```markdown
## [2026-11-03] fonte | verbale-2026-11-03.md
- Nuova: wiki/fonte-verbale-2026-11-03.md
- Aggiornate: wiki/nordica-crediti.md, wiki/requisiti-sicurezza.md
- indice: aggiunta la sintesi sotto «Clienti»
```

Le azioni sono `fonte` (un ingest), `pagina` (una pagina scritta o corretta a mano, anche la risposta a una query che vale la pena tenere) e `controllo` (un lint). Il registro risponde alla domanda «che cosa è cambiato
da quando ho guardato l'ultima volta?» senza dover leggere tutti i commit.

## Le pagine

Ci sono due tipi di pagina:

- **Pagina di concetto**: un'idea, una persona, un'organizzazione, un requisito. Raccoglie quello che il gruppo sa,
  da tutte le fonti. Cresce nel tempo.
- **Pagina di sintesi**: una fonte letta. Dice che cosa contiene, che cosa ha cambiato, e rimanda ai concetti toccati.
  Una volta scritta cambia poco.

Ogni pagina comincia con il front matter e il TL;DR:

```markdown
---
title: Requisiti di sicurezza
fonti: [fonti/NC-2027-014-capitolato.pdf, fonti/2026-11-03-verbale.md]
aggiornato: 2026-11-03
---

# Requisiti di sicurezza

## TL;DR
...
```

## I collegamenti

Una pagina che nomina un concetto con una sua pagina ci rimanda con un link relativo:
`[requisiti di sicurezza](requisiti-sicurezza.md)`. Così il wiki diventa una rete che si percorre, e il
bibliotecario può accorgersi delle pagine che nessuno raggiunge.

Ogni affermazione importante dice da quale fonte viene. Senza fonte è un'opinione: va bene scriverla, ma va detto.

## Dove sta lo schema

Le regole del wiki stanno nel file d'istruzioni del progetto (`CLAUDE.md`, `AGENTS.md` o `copilot-instructions.md`).
Lì il gruppo scrive le sue scelte: i nomi delle cartelle, gli argomenti dell'indice, che cosa non entra nel wiki. Gli
agenti lo leggono a ogni lavoro. Le operazioni che usano questa struttura sono nel [capitolo 3](03-le-tre-operazioni.md).
