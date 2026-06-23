# CTRU / CNTR Card

## Basic role

CTRU and CNTR appear in this corpus as NTRU-family KEM research/draft materials. Treat them as China-related research/draft schemes unless a final formal standard is added.

## Traditional crypto analogy

- Closest traditional role: public-key encryption / KEM for establishing shared keys.
- Not equivalent to: digital signatures, AES, or SHA.
- Teaching analogy: CTRU/CNTR are useful for showing that lattice PQC includes NTRU-style ring constructions, not only Module-LWE/ML-KEM.

## Core idea

The CTRU paper table describes CTRU as using NTRU and RLWE assumptions and CNTR as using NTRU and RLWR assumptions over a compact NTRU lattice ring. The Chinese draft contains named parameter sets such as CTRU-576, CTRU-768, CTRU-1024, CTRU-Light, and CTRU-Prime.

## Main flow for teaching

1. KeyGen creates ring-polynomial secret/public key material.
2. Encapsulation/encryption forms ciphertext using ring arithmetic and small/random polynomials.
3. Decapsulation/decryption recovers the shared key/message using the secret polynomial structure.

## Main implementation modules

- Polynomial multiplication in NTRU-style rings.
- Modular reduction for q/q2-like moduli.
- Small polynomial sampling.
- Packing/unpacking of polynomial coefficients.
- Hash/KDF steps for KEM transform.

## Facts requiring citation

- Parameter names and ring definitions.
- n, q, q2, distribution names, key/ciphertext sizes.
- Classical/quantum security estimates.
- DFR values.
- Any benchmark values.

## Do not claim without source

- That CTRU or CNTR is final standardized.
- That the research-paper table and Chinese draft table are identical.
- Any FPGA/ASIC performance.

## Teaching notes

For beginners coming from RSA/ECC, CTRU/CNTR can be introduced after ML-KEM as “another lattice KEM family using NTRU-style polynomial rings.” Emphasize that ring choice and coefficient packing strongly affect implementation.
