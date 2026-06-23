# NEV Card

## Basic role

NEV appears in this corpus as a research KEM/PKE-family construction related to NTRU-style encryption and vector decoding. Treat it as research context, not as a standard scheme.

## Traditional crypto analogy

- Closest traditional role: public-key encryption/KEM building block.
- Not equivalent to: signatures, AES, SHA, or standard ML-KEM.
- Teaching analogy: NEV is useful for discussing alternative NTRU-like research directions and the role of decoding/decryption-failure probability.

## Core idea

The paper compares NEV and NEV' parameter sets and reports key/ciphertext sizes, decryption-failure probability, and LWE-estimator security figures. NEV' is presented as an optimized variant in the paper.

## Main flow for teaching

1. Generate compact ring/vector public and secret keys.
2. Encrypt/encapsulate with noise/randomness.
3. Decode/decrypt with vector-decoding logic and analyze failure probability.

## Main implementation modules

- Ring/vector arithmetic.
- Sampling.
- Vector decoding.
- Packing/unpacking.
- Hash/KDF for KEM wrapping if applicable.

## Facts requiring citation

- Public key, secret key, and ciphertext sizes.
- DFR values.
- LWE-estimator bits.
- Any claim about NEV versus NEV'.

## Do not claim without source

- That NEV is a NIST or national standard.
- Exact parameter internals beyond the extracted comparison table.
- Hardware area/latency.

## Teaching notes

Use NEV as an “advanced/optional research branch” in the tutor. It should not distract beginners from the standard map: ML-KEM, ML-DSA, SLH-DSA, Falcon/FN-DSA, and HQC.
