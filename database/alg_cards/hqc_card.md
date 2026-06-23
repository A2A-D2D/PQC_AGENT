# HQC Card

## Basic role

HQC is a code-based key encapsulation mechanism. In protocol role, it is closer to ECDH/ML-KEM than to AES or a digital signature scheme.

## Traditional crypto analogy

- Closest traditional role: key establishment, similar system role to ECDH or ML-KEM.
- Not equivalent to: RSA signatures, ECDSA, ML-DSA, Falcon, AES.
- Teaching analogy: instead of relying on elliptic-curve discrete logarithm or lattice/LWE problems, HQC relies on hard decoding problems from coding theory.

## Core idea

HQC uses quasi-cyclic codes and decoding-hardness assumptions. It provides algorithmic diversity relative to lattice-based ML-KEM.

## Main flow for teaching

1. KeyGen generates an encapsulation key and decapsulation key.
2. Encaps uses the public/encapsulation key to create a ciphertext and shared key.
3. Decaps uses the secret/decapsulation key to recover the shared key from the ciphertext.

## Main implementation modules

- Binary polynomial/vector operations.
- Sparse vector generation.
- Error-correcting code operations.
- Hash/XOF operations.
- Constant-time decapsulation and failure handling.

## Facts requiring citation

- HQC-1 / HQC-3 / HQC-5 parameters.
- Key/ciphertext sizes.
- DFR values.
- Software benchmark cycles.
- NIST standardization status.

## Do not claim without source

- Final FIPS byte sizes.
- Hardware area or FPGA resources.
- Superiority over ML-KEM without a stated metric and source.

## Teaching notes

Use HQC to teach why PQC standardization wants algorithmic diversity. ML-KEM is lattice-based; HQC is code-based, so it hedges against overconcentration on one mathematical family.
