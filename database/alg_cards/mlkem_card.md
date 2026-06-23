# ML-KEM Card

## Basic role

ML-KEM is a key encapsulation mechanism used to establish a shared secret.

## Traditional-crypto analogy

Closest role: ECDH/key establishment. It is not a bulk data encryption algorithm like AES-GCM.

## Main flow

- KeyGen: generate encapsulation key and decapsulation key.
- Encaps: use the encapsulation key to produce ciphertext and shared secret.
- Decaps: use the decapsulation key and ciphertext to recover the shared secret.

## Main implementation modules

- SHAKE / Keccak
- NTT / INTT
- modular arithmetic over q = 3329
- sampling
- compression / decompression
- byte encoding / decoding

## Authoritative source in corpus

`01_nist_standards/NIST_FIPS_203_ML-KEM_2024.pdf`

## Facts requiring citation

- parameter sets and values;
- key and ciphertext sizes;
- security categories;
- exact pseudocode;
- validation requirements.

## Do not answer without source

- exact cycle count;
- hardware area;
- fastest implementation;
- best architecture.
