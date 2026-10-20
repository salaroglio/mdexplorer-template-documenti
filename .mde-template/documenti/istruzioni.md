## Document Driven Development

- Il wiki del progetto sta in `wiki/`: parti sempre da `wiki/indice.md`, che dice che cosa c'è, e guarda in
  `wiki/registro.md` che cosa è cambiato di recente. Le fonti stanno in `fonti/` e non si modificano mai.
- Una pagina del wiki segue la skill `documenti-wiki`: TL;DR in testa, un argomento per pagina, la fonte citata, i
  collegamenti alle altre pagine invece delle ripetizioni.
- Una fonte entra nel wiki con il workflow `.mde-template/documenti/workflows/fonte.md`, il controllo del wiki con
  `.mde-template/documenti/workflows/controllo.md`: non far partire tu i loro agenti e non scrivere i loro file al loro posto.
- La teoria del metodo, se il progetto l'ha chiesta, sta in `teoria/documenti/`: usala per spiegare a chi te lo chiede
  come funziona un wiki per un LLM. Se manca e servirebbe, proponi di scaricarla (strumento `add_theory`, id
  `documenti`) e scaricala solo dopo il sì della persona.
- I file in `.mde-template/documenti/` sono del metodo e arrivano con i suoi aggiornamenti: non modificarli.
