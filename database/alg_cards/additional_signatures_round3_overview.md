# NIST Additional-Signatures Round 3 Overview Card

## Basic role

The additional-signatures candidates are digital-signature schemes considered after the main NIST PQC signature standardization path. In this corpus, the Round 3 candidate set is represented by specification PDFs for FAEST, HAWK, MAYO, MQOM, QR-UOV, SDitH, SNOVA, SQIsign, and UOV.

## Status

- Status in this database: NIST Additional Digital Signatures Round 3 candidates.
- Date/status source: NIST announcement and NIST IR 8610, both dated May 14, 2026.
- Important caveat: none of these candidates should be described as a final FIPS standard unless a later final standard is added to the database.

## Candidate list and teaching buckets

| Candidate | Broad family / teaching bucket | Good teaching angle | Detailed table |
|---|---|---|---|
| FAEST | Symmetric-key / AES-Rijndael OWF + VOLE-in-the-head | proving knowledge of a block-cipher key | `database/metadata/additional_signatures_round3_tables.md#faest` |
| HAWK | Lattice / NTRU-style hash-and-sign | compact lattice signatures beyond ML-DSA/Falcon | `database/metadata/additional_signatures_round3_tables.md#hawk` |
| MAYO | Multivariate / Oil-and-Vinegar variant | public-key-size reduction in multivariate signatures | `database/metadata/additional_signatures_round3_tables.md#mayo` |
| MQOM | Multivariate MQ + in-the-head proof | proof of knowledge of MQ solution | `database/metadata/additional_signatures_round3_tables.md#mqom` |
| QR-UOV | Multivariate / quotient-ring UOV | structured UOV to reduce public-key size | `database/metadata/additional_signatures_round3_tables.md#qr-uov` |
| SDitH | Code-based / syndrome decoding in the head | code-based signatures and proof overhead | `database/metadata/additional_signatures_round3_tables.md#sdith` |
| SNOVA | Multivariate / structured UOV over rings | structured multivariate scheme with small public-key variants | `database/metadata/additional_signatures_round3_tables.md#snova` |
| SQIsign | Isogeny-based signature | very compact keys/signatures with specialized mathematics | `database/metadata/additional_signatures_round3_tables.md#sqisign` |
| UOV | Multivariate / unbalanced oil-and-vinegar | baseline UOV: short signatures, large public keys | `database/metadata/additional_signatures_round3_tables.md#uov` |

## Traditional crypto analogy

- Closest traditional role: ECDSA / EdDSA / RSA-PSS replacement or complement.
- Not equivalent to: KEM, ECDH, AES, or SHA.

## Why they matter for teaching

ML-DSA and SLH-DSA are already standardized, while Falcon/FN-DSA is on a future-standard track. The additional-signatures process shows that NIST is still exploring signature diversity, including different mathematical assumptions and trade-offs.

A useful lecture structure is:

1. Start from ML-DSA / SLH-DSA / Falcon as the “main NIST signature portfolio.”
2. Explain why additional signatures are still useful: diversity, smaller signatures, different assumptions, and implementation trade-offs.
3. Group the nine candidates by family, not alphabetically.
4. Use the key/signature-size table only after explaining the mathematical family and implementation costs.

## Facts requiring citation

- Candidate status and round membership.
- Parameter sets.
- Public key, secret key, and signature sizes.
- Claimed security levels.
- Software/hardware performance.

## Do not claim without source

- That any candidate has won or become a final standard.
- That one candidate is best overall.
- That smaller signatures imply better deployment fit without considering key size, signing/verification time, memory, side-channel resistance, implementation complexity, and licensing.

## Agent answer rule

When asked about “the nine NIST additional signature candidates,” answer in this order:

1. State that they are Round 3 candidates, not final standards.
2. List all nine candidates.
3. Group them by family.
4. If exact sizes are needed, use `additional_signatures_round3_tables.md` and mention the original PDF/table.
5. If performance is requested, do not infer from size tables; require benchmark tables or source PDFs.
