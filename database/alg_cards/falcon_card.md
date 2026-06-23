# Falcon / FN-DSA-track Card

## Basic role

Falcon is a lattice-based digital signature scheme. In protocol role, it is a candidate successor/complement to RSA-PSS or ECDSA, not a KEM and not a symmetric cipher.

## Traditional crypto analogy

- Closest traditional role: ECDSA / EdDSA / RSA-PSS digital signature.
- Not equivalent to: ECDH, AES, SHA, or ML-KEM.
- Teaching analogy: if ECDSA is “sign by elliptic-curve scalar arithmetic,” Falcon is “sign by sampling a short lattice vector tied to the message hash.”

## Core idea

Falcon is based on NTRU lattices and follows a hash-and-sign/GPV-style signature approach. The signature is compact, but the implementation requires careful floating-point or fixed-point FFT-style arithmetic and Gaussian sampling.

## Main flow for teaching

1. KeyGen builds an NTRU-style secret basis and public key.
2. Sign hashes the message to a target and samples a short lattice vector near that target.
3. Verify checks that the signature corresponds to the public key and has small enough norm.

## Main implementation modules

- NTRU polynomial arithmetic.
- FFT/Falcon tree operations.
- Discrete Gaussian sampling.
- Hash-to-point.
- Norm check.
- Constant-time control and numerical-precision management.

## Facts requiring citation

- Falcon-512 / Falcon-1024 byte sizes.
- q, n, sigma, norm bound, or any exact parameter.
- Any final FIPS 206 / FN-DSA status claim.
- Any performance or hardware-resource result.

## Do not claim without source

- “Falcon is easier to implement than ML-DSA.”
- “Falcon is final FIPS 206.”
- “Falcon hardware is smaller/faster than ML-DSA.”
- Exact private-key/signature/public-key sizes unless taken from the parameter table.

## Teaching notes

Falcon is useful for explaining the trade-off between compact signatures and implementation difficulty. A good quickstart explanation should contrast it with ML-DSA: ML-DSA is more straightforward integer/modular arithmetic, while Falcon has shorter signatures but more difficult sampling and numerical behavior.
