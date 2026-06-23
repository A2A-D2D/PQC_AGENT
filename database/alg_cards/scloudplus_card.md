# Scloud+ Card

## Basic role

Scloud+ is a China-related LWE-family PKE/KEM research scheme in this corpus. For teaching, it is useful as an example of a non-ML-KEM KEM with lattice coding, message encoding/decoding, and BDD-style decoding.

## Traditional crypto analogy

- Closest traditional role: key establishment / public-key encryption building block.
- Not equivalent to: AES, SHA, digital signature.
- Teaching analogy: where RSA/ECC engineers expect big-integer or curve arithmetic, Scloud+ forces them to think about matrix/vector arithmetic, coding lattices, shaping lattices, and decoding.

## Core idea

Scloud+ relies on LWE-style constructions and uses lattice coding techniques for message encoding and decoding. Its parameters include matrix dimensions, moduli, noise parameters, and MsgEnc/MsgDec coding-lattice settings.

## Main flow for teaching

1. Public-key material is generated from LWE-style matrix/vector relations.
2. Encapsulation/encryption uses randomness and noise to produce ciphertext.
3. Decapsulation/decryption removes the secret contribution and decodes the message/shared secret using MsgDec/BDD-style logic.

## Main implementation modules

- Matrix/vector arithmetic.
- Modular additions/subtractions and reductions.
- Sampling/noise generation.
- Message encoding and decoding.
- BW32 coding lattice / BDD flow for the Scloud+ parameterization in the source paper.
- Packing and unpacking of keys/ciphertexts.

## Facts requiring citation

- q, q1, q2, m, n, mbar, nbar.
- Public key/ciphertext/shared secret sizes.
- Security and DFR numbers.
- MsgEnc/MsgDec parameters such as mu, tau, BW32, and shaping lattice.
- Software-cycle benchmark values.

## Do not claim without source

- That Scloud+ is standardized by NIST.
- That local RTL/demo parameters are the same as paper parameters.
- Any hardware area, LUT/FF/DSP count, or cycle count unless sourced from a specific report.

## Teaching notes

Scloud+ is particularly useful for a hardware-oriented tutor because it exposes blocks that do not look like the usual Kyber/ML-KEM NTT-centric datapath. Keep paper-level algorithm facts separate from any local RTL architecture decisions.
