# QR-UOV Card

## Basic role

QR-UOV is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Multivariate signature; quotient-ring variant of UOV.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

QR-UOV starts from UOV-style multivariate signatures and introduces quotient-ring structure to reduce the public key relative to plain UOV designs.

## Implementation modules

- Finite-field arithmetic over multiple q choices
- Structured polynomial/matrix operations
- Public-key generation with QR-UOV constraints
- Signing by solving structured Oil-and-Vinegar equations
- Verification by public-map evaluation

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#qr-uov`.

## Facts requiring citation

- Recommended `(q=127, ell=3)` parameter sets
- Additional parameter sets
- Public/private key sizes
- Signature sizes
- Any benchmark or attack-complexity claim

## Teaching warning

Do not describe QR-UOV as a lattice scheme. It is a structured multivariate signature.
