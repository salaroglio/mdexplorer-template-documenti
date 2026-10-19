---
mde_type: workflow
title: Una fonte nel wiki
workflow: fonte.workflow.json
---

# Una fonte nel wiki

## TL;DR

Una fonte nuova in `fonti/` entra nel wiki: il redattore scrive o aggiorna le pagine che tocca, l'indice e il registro;
il revisore le rilegge contro le fonti e le convenzioni; il responsabile della documentazione decide.

- Il responsabile della documentazione lancia il redattore quando in `fonti/` c'è qualcosa di nuovo.
- La revisione parte da sola; le pagine da correggere si rifanno quando la persona preme «Fai ripartire».
- Ogni giro resta nel registro dei giri e in git: chi ha scritto, chi ha riletto, chi ha accettato.

## Il giro

```plantuml(@workflow, ./fonte.workflow.json)
```

## Chi fa che cosa

| Passo | Chi lavora | Che cosa consegna | Chi approva |
|---|---|---|---|
| Porta le fonti nel wiki | agente redattore | le pagine di `wiki/`, l'indice, il registro | il responsabile della documentazione |
| Revisione | agente revisore | `revisioni/revisione-<data>.md` | il responsabile della documentazione |
| Accetta le pagine | il responsabile della documentazione | la decisione, nel registro dei giri | — |
