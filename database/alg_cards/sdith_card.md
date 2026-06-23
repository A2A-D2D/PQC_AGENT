# SDitH Card

## Basic role

SDitH is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Code-based signature; syndrome decoding in the head.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

SDitH builds signatures from the hardness of syndrome decoding and an in-the-head proof system. It is useful for teaching code-based signatures separately from code-based KEMs such as HQC.

## Implementation modules

- Syndrome decoding instance generation
- Hashing and seed expansion
- VOLEitH or TCitH proof-system machinery
- Commitments, openings, and transcript handling

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#sdith`.

## Facts requiring citation

- GF(2) and GF(256) parameter sets
- short vs fast trade-offs
- TCitH variant sizes
- Public/secret key sizes
- Signature sizes
- Any performance claim

## Teaching warning

Do not confuse SDitH with HQC. Both are code-based in a broad sense, but HQC is a KEM while SDitH is a signature construction with in-the-head proof overhead.
