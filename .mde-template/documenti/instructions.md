## Systematic writing of documents

- The project's wiki is in `wiki/`: always start from `wiki/index.md`, which says what is there, and look in
  `wiki/log.md` for what changed recently. The sources are in `sources/` and are never modified.
- A wiki page follows the `documenti-wiki` skill: TL;DR at the top, one topic per page, the source cited, links to the
  other pages instead of repetitions.
- A source enters the wiki with the workflow `.mde-template/documenti/workflows/source.md`, the wiki check with
  `.mde-template/documenti/workflows/check.md`: do not start their agents yourself and do not write their files in
  their place.
- The method's theory, if the project asked for it, is in `theory/documenti/`: use it to explain to whoever asks how a
  wiki for an LLM works. If it is missing and would help, propose to download it (tool `add_theory`, id `documenti`)
  and download it only after the person says yes.
- The files in `.mde-template/documenti/` belong to the method and arrive with its updates: do not modify them.
