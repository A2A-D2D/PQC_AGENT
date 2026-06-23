# PQC Database v3

This package extends `pqc_database_v2` by extracting the nine NIST Additional Digital Signatures Round 3 candidate tables.

## What changed in v3

New metadata file:

- `database/metadata/additional_signatures_round3_tables.md`

Updated files:

- `database/metadata/parameter_tables_extended.md`
- `database/metadata/standard_status.md`
- `database/extraction_notes/source_pages.md`
- `database/alg_cards/additional_signatures_round3_overview.md`
- `database/alg_cards/README.md`

New algorithm cards:

- `database/alg_cards/faest_card.md`
- `database/alg_cards/hawk_card.md`
- `database/alg_cards/mayo_card.md`
- `database/alg_cards/mqom_card.md`
- `database/alg_cards/qr_uov_card.md`
- `database/alg_cards/sdith_card.md`
- `database/alg_cards/snova_card.md`
- `database/alg_cards/sqisign_card.md`
- `database/alg_cards/uov_card.md`

## Candidate coverage

The v3 extraction covers:

| Candidate | Family / teaching bucket | Extracted content |
|---|---|---|
| FAEST | Symmetric-key / AES-Rijndael OWF + VOLE-in-the-head | main parameters, pk size, derived sk size, signature size |
| HAWK | Lattice / NTRU-style hash-and-sign | parameter sets, key/signature sizes, degree and distribution parameters |
| MAYO | Multivariate / Oil-and-Vinegar variant | MAYO1/2/3/5 key/signature sizes and main parameters |
| MQOM | Multivariate MQ + MPC/TCitH-style proof | GF(2)/GF(256), short/fast, 3r/5r sizes |
| QR-UOV | Multivariate / quotient-ring UOV | main and additional parameter sets, key/signature sizes |
| SDitH | Code-based / syndrome decoding in the head | GF(2), GF(256), and TCitH variant size tables |
| SNOVA | Multivariate / structured UOV over rings | key/signature-size table for l=2/3/4/5 sets |
| SQIsign | Isogeny-based | key/signature sizes for NIST-I/III/V |
| UOV | Multivariate / unbalanced oil-and-vinegar | compact/expanded key sizes and signatures |

## Status caveat

The nine schemes are Round 3 candidates, not final standards. The exact sizes in v3 are candidate-specification values from the PDFs in the corpus. If NIST publishes updated Round 3 packages or final standards later, update this database and mark the old rows superseded.

## Agent rule

The database still follows the core rule:

> Concepts may be explained freely; numerical claims must be sourced.

For the nine Round 3 candidates, cite:

1. `database/metadata/additional_signatures_round3_tables.md`, and
2. the original candidate PDF/table listed in `database/extraction_notes/source_pages.md`.
