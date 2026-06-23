# SQIsign Card

## Basic role

SQIsign is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Isogeny-based digital signature.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

SQIsign relies on isogeny/quaternion-algebra machinery and is notable for very compact public keys and signatures compared with many PQC signatures.

## Implementation modules

- Isogeny computations
- Elliptic-curve and torsion-basis operations
- Quaternion/ideal representations
- Specialized key generation, signing, and verification procedures

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#sqisign`.

## Facts requiring citation

- Public-key, secret-key, and signature sizes
- Security-level mapping
- Any performance, memory, or implementation-complexity claim

## Teaching warning

SQIsign is compact but mathematically specialized. Do not imply it is automatically easier to deploy just because the key/signature sizes are small.
