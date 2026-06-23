# Aigis Card

## Basic role

Aigis appears in this corpus as China-related design documents for both an encryption/KEM-style scheme (`Aigis-enc`) and a signature scheme (`Aigis-sig`). Treat these as domestic/research/candidate materials unless a formal issued standard source is added.

## Traditional crypto analogy

- Aigis-enc: closest role is key establishment/KEM, similar system role to ML-KEM/ECDH.
- Aigis-sig: closest role is digital signature, similar system role to ML-DSA/ECDSA.
- Not equivalent to: AES, SHA, or bulk data encryption.

## Core idea

- Aigis-enc is described as an asymmetric MLWE/AMLWE-style KEM/encryption design.
- Aigis-sig is structurally close to Fiat-Shamir-with-aborts lattice signatures and should be taught by comparison with Dilithium/ML-DSA-style commit-challenge-response flows.

## Main flow for teaching

### Aigis-enc

1. KeyGen generates public and secret key material.
2. Encaps/Encrypt uses public key and randomness to produce ciphertext and shared secret/message protection.
3. Decaps/Decrypt uses secret key to recover the shared secret/message.

### Aigis-sig

1. KeyGen creates public key and secret signing material.
2. Sign samples a temporary value, forms a commitment, hashes to a challenge, computes a response, and performs range/rejection checks.
3. Verify recomputes the challenge consistency from public data.

## Main implementation modules

- Modular polynomial/vector arithmetic.
- NTT-like polynomial multiplication where applicable.
- Noise/small-coefficient sampling.
- Hash/XOF.
- Compression/packing.
- For signatures: decomposition, hints, rejection sampling, challenge generation.

## Facts requiring citation

- All parameter-set values.
- Public/secret key sizes.
- Ciphertext/signature sizes.
- CPU benchmark values.
- Any claim that a parameter set is recommended.

## Do not claim without source

- That Aigis is a NIST standard.
- That Aigis is nationally standardized unless a final standard is added.
- Hardware performance, area, or timing.
- Equivalence to ML-KEM or ML-DSA beyond structural analogy.

## Teaching notes

Aigis is useful for explaining that PQC development is not limited to NIST schemes. For a quickstart tutor, keep it in a “China-related/domestic candidate” lane and always separate Aigis-enc from Aigis-sig.
