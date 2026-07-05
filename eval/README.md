# Evaluation sets

## eval_set_v1.csv — the open benchmark (252 coins)
A stratified sample across **53 mints** — museum-attributed specimens (BM · BnF · ANS · Berlin · Fitzwilliam · Harvard) plus a slice of OCSI-verified identifications, with coins whose photographs appear in the OCSI training gallery **excluded**. Composition is deliberately varied by mint and region rather than alphabetical.

Columns: `museum, accession, record_url`. Fetch images from the museum record; predict the type (`HN Italy N` / `RRC n/m` / `RPC n`).

**Honesty note:** v1 labels are *derivable* from public sources (museum catalogues, OCSI specimen lists). Treat v1 as an **open benchmark** for development and honest self-evaluation — scores are self-reported. Report them via issue/PR for LEADERBOARD.md, stating your method and whether OCSI data was used in training.

## v2 — the blind set (in preparation)
A genuinely held-back split is being reserved from *future* verification rounds: verified labels withheld from the public register for an embargo period and used for adjudicated scoring. Announced here when frozen.
