---
mde_type: workflow
title: Il controllo del wiki
workflow: controllo.workflow.json
---

# Il controllo del wiki

## TL;DR

Ogni tanto il wiki si controlla tutto insieme, come fa un bibliotecario: contraddizioni, affermazioni superate, pagine
che nessuno collega, concetti senza pagina, collegamenti rotti. Il bibliotecario scrive il rapporto, il responsabile
della documentazione decide che cosa si corregge.

- Lo lancia il responsabile della documentazione, per esempio dopo qualche fonte nuova o prima di una consegna.
- Il bibliotecario non corregge: propone. Le correzioni le fa il redattore con una fonte, o la persona a mano.
- Il rapporto resta in `revisioni/`, il giro nel registro dei giri.

## Il giro

```plantuml(@workflow, ./controllo.workflow.json)
```

## Chi fa che cosa

| Passo | Chi lavora | Che cosa consegna | Chi approva |
|---|---|---|---|
| Controlla il wiki | agente bibliotecario | `revisioni/controllo-<data>.md` | il responsabile della documentazione |
| Decidi le correzioni | il responsabile della documentazione | la decisione, nel registro dei giri | — |
