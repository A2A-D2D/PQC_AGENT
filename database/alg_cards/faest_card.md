# FAEST Card

## Basic role

FAEST is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Symmetric-key based signature using AES/Rijndael-style one-way functions and VOLE-in-the-head zero-knowledge proof machinery.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

Do not compare FAEST to AES as a symmetric cipher replacement. FAEST uses block-cipher structure as a hard relation inside a signature construction.

## Core intuition

A FAEST public key contains an input/output relation for a block-cipher-like one-way function. A signature proves knowledge of the secret key that maps the public input to the public output, without revealing the key.

## Implementation modules

- AES/Rijndael-style computations
- VOLE-in-the-head proof system
- Commitments and hashes
- Repetition/opening logic

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#faest`.

## Facts requiring citation

- FAEST/FAEST-EM variant sizes
- Public-key size
- Signature size
- Secret-key-size derivation
- Round 3 status
- Any performance claim

## Teaching warning

FAEST is good for explaining “PQC signatures can be built from symmetric primitives plus zero-knowledge proofs,” but it is not a general-purpose block cipher or KEM.
