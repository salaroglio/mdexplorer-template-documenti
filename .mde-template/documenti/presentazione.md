---
document_type: slides
reveal:
  theme: mde-space
---

<!-- .slide: data-background-image="/mde-space/sfondi/luna.svg" class="mde-cielo" -->
<img class="mde-icona-grande" src="/mde-space/icone/base.svg" alt="">

# Scrittura sistematica dei documenti

Lo **strato comune** di ogni progetto composto:
il wiki del progetto, scritto e tenuto in ordine con gli agenti.

---

## <img class="mde-icona" src="/mde-space/icone/telescopio.svg" alt=""> A che cosa serve

- I documenti di un progetto si accumulano, e ogni volta qualcuno, persona o LLM, li rilegge da capo
- Qui le fonti diventano un **wiki che cresce**: ogni fonte nuova arricchisce pagine che ci sono già
- L'**indice** dice che cosa c'è, il **registro** che cosa è cambiato, git chi ha fatto che cosa

---

## <img class="mde-icona" src="/mde-space/icone/satellite.svg" alt=""> Tre strati

1. **Le fonti** in `fonti/`: verbali, specifiche, mail. Non si toccano mai
2. **Il wiki** in `wiki/`: una pagina per argomento, con TL;DR, fonti citate e collegamenti
3. **Le convenzioni**: la skill `documenti-wiki` e le istruzioni del progetto

---

## <img class="mde-icona" src="/mde-space/icone/astronauta.svg" alt=""> Chi fa che cosa

- **Redattore**: porta le fonti nuove nel wiki, con indice e registro
- **Revisore**: rilegge le pagine contro le fonti e dice che cosa correggere
- **Bibliotecario**: controlla il wiki intero, contraddizioni e pagine orfane comprese
- Il **responsabile della documentazione** approva e decide

---

## <img class="mde-icona" src="/mde-space/icone/cometa.svg" alt=""> Due giri

- **Una fonte nel wiki**: redattore → revisore → la persona accetta, o rimanda indietro
- **Il controllo del wiki**: bibliotecario → la persona decide che cosa correggere

---

## <img class="mde-icona" src="/mde-space/icone/stella.svg" alt=""> La teoria

Se la chiedi, arriva in `teoria/documenti/`: perché un wiki per un LLM, com'è fatto, le tre operazioni,
le convenzioni di scrittura, i ruoli, come imparare con il MarkAgent.

Si può scaricare anche dopo, dalle impostazioni del progetto.

---

<!-- .slide: data-background-image="/mde-space/sfondi/razzo.svg" class="mde-sinistra" -->

## <img class="mde-icona" src="/mde-space/icone/bandiera.svg" alt=""> Che cosa trovi nel progetto

- `fonti/`, `wiki/indice.md`, `wiki/registro.md`, `revisioni/`
- tre agenti e il ruolo di responsabile della documentazione, ancora senza nome
- sopra, i metodi che scegli: Ontologie, ISO 9001
