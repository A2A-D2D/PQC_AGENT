# MAYO Card

## Basic role

MAYO is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Multivariate signature; a modified Oil-and-Vinegar-style construction designed to reduce public-key size.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

Classic multivariate signatures often have short signatures but large public keys. MAYO modifies the Oil-and-Vinegar structure to trade public-key size, signature size, and expansion cost.

## Implementation modules

- Finite-field arithmetic over F16
- Multivariate quadratic polynomial evaluation
- Compact/expanded public key handling
- Compact/expanded secret key handling
- Hashing and salt processing

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#mayo`.

## Facts requiring citation

- MAYO1/MAYO2/MAYO3/MAYO5 sizes
- Compact vs expanded key sizes
- Security level claims
- Any performance claim

## Teaching warning

Do not describe MAYO as lattice-based. It belongs in the multivariate signature family.
