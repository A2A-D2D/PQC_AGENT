# SNOVA Card

## Basic role

SNOVA is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Multivariate signature; structured UOV-like design over rings.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

SNOVA uses structured multivariate maps to reduce public-key size compared with plain UOV-style signatures while preserving short-signature advantages.

## Implementation modules

- Finite-field/ring arithmetic over F16-related structures
- Public-key expansion
- Seed-type and expanded secret-key representations
- Multivariate public-map evaluation
- Signing and verification routines

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#snova`.

## Facts requiring citation

- l=2/3/4/5 parameter variants
- fractional byte values reported in the spec table
- Seed-type vs expanded secret-key sizes
- Any benchmark or attack-complexity claim

## Teaching warning

SNOVA should be taught as a structured multivariate scheme. Do not merge its parameter trade-offs with UOV or QR-UOV without explicitly stating the different structure.
