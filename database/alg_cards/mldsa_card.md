# ML-DSA Card

## Basic role

ML-DSA is a module-lattice-based digital signature algorithm.

## Traditional-crypto analogy

Closest role: ECDSA/RSA-PSS digital signature. The core computation is not elliptic-curve scalar multiplication; it uses lattice/module arithmetic, commitments, challenges, responses, rejection checks, and hint-related processing.

## Main flow

- KeyGen: generate public/private signing key pair.
- Sign: generate a signature for a message, optionally using pre-hashing.
- Verify: check signature validity against the public key and message.

## Main implementation modules

- SHAKE / Keccak
- NTT / INTT
- modular arithmetic over q = 8380417
- sampling and challenge generation
- Decompose / MakeHint / UseHint
- packing / unpacking

## Authoritative source in corpus

`01_nist_standards/NIST_FIPS_204_ML-DSA_2024.pdf`

## Facts requiring citation

- parameter sets and values;
- key and signature sizes;
- security categories;
- exact pseudocode;
- pre-hash/signing variant rules.
