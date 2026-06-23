# SLH-DSA Card

## Basic role

SLH-DSA is a stateless hash-based digital signature algorithm.

## Traditional-crypto analogy

Closest role: digital signature. Unlike ML-DSA/Falcon, it does not rely on lattice assumptions; it relies on hash-function security.

## Main idea

SLH-DSA builds signatures from hash-based components such as WOTS+, XMSS, and FORS in a stateless construction.

## Main implementation modules

- SHA2 or SHAKE family functions
- address manipulation
- tree traversal
- WOTS+
- XMSS
- FORS

## Authoritative source in corpus

`01_nist_standards/NIST_FIPS_205_SLH-DSA_2024.pdf`

## Facts requiring citation

- parameter rows;
- public key size;
- signature size;
- security category;
- SHA2/SHAKE instantiation rules.
