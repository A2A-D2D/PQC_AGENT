# HAWK Card

## Basic role

HAWK is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Lattice-based / NTRU-style hash-and-sign signature.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

HAWK is a compact lattice signature design. It is useful for teaching that lattice signatures are not limited to ML-DSA/Falcon, although the implementation and security arguments differ.

## Implementation modules

- Polynomial arithmetic over rings
- NTRU-style key structure
- Gaussian/distribution sampling components
- Fixed-size key/signature encodings

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#hawk`.

## Facts requiring citation

- HAWK-512 / HAWK-1024 sizes
- Whether HAWK-256 is only a challenge/cryptanalytic target
- Security level claims
- Any benchmark or side-channel claim

## Teaching warning

Do not merge HAWK with Falcon just because both are lattice signatures with compact signatures. Treat it as a separate candidate with its own specification.
