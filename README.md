# The OCSI Challenge

**An open identification effort for the museum coins of Magna Graecia.**

Thousands of Greek-Italian coins sit in public museum cabinets catalogued by mint and denomination — but almost never by *type*, because no online type registry for Greek Italy existed to catalogue against. [OCSI — Online Coins of Southern Italy](https://metamorphoses-collection.org/ocsi) now provides that registry (2,551 types, 88 mints, on the spine of *Historia Numorum: Italy* + RRC/RPC). Closing the identification gap is a finite, measurable, open task — this repository is where it happens.

## The task
`data/backlog_open.csv` lists museum coins awaiting an exact type identification: museum, accession, the museum's own record URL (with photographs), a mint hint, and metrology where the museum recorded it. Propose the HN Italy / RRC / RPC type for any coin — with your eyes, your die-study knowledge, or your model.

## How to submit
1. Fork, add a CSV to `submissions/` following `submissions/TEMPLATE.csv`.
2. One row per coin: `museum, accession, proposed_type, confidence, evidence, contributor`.
   *Evidence* is what makes a proposal reviewable: a legend reading, a die match, comparanda ("same dies as SNG ANS 1023"), metrology.
3. Open a pull request. Every proposal is **reviewed by a human before it touches the corpus** — coins move `unidentified → proposed → verified`.
4. Verified identifications enter `verified/verified_identifications.csv` **with your name on the record**, and appear on the coin's OCSI type page.

## Ground rules
- The type registry is the [OCSI corpus](https://metamorphoses-collection.org/ocsi/browse); cite types as `HN Italy 687`, `RRC 103/2` etc.
- Museum images stay at the museums — we link, never redistribute.
- An **evaluation set with held-back labels** is reserved for scoring machine-learning entrants (see `eval/`).

## Baselines (honest ones)
| system | dealer photos | museum photos |
|---|---|---|
| OCSI v8c (DINOv2 retrieval, fused with metrology) | ~69% top-1 | ~34–40% top-1 |
| v8c proposals + human verification (rounds 1–2, n=141) | — | **98.6% precision** |

The dealer→museum drop is *the domain gap* — the actual scientific challenge. Beat it.

## Licence & citation
Data: **CC BY 4.0** — cite as *OCSI Challenge, Metamorphoses Collection, github.com/ChroniconCJ/ocsi-challenge* alongside [OCSI](https://metamorphoses-collection.org/ocsi/credits#cite).
A non-commercial scholarly effort of the [Metamorphoses of Civilization](https://metamorphoses-collection.org) collection.
