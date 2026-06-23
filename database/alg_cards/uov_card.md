# UOV Card

## Basic role

UOV is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Multivariate signature; unbalanced oil-and-vinegar.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

UOV signs by using a hidden trapdoor structure that makes it easy for the signer to find preimages, while the public key appears as a hard multivariate quadratic system. It is known for short signatures but large public keys.

## Implementation modules

- Multivariate quadratic polynomial maps
- Finite-field arithmetic over F16 or F256 depending on parameter set
- Compact/expanded public-key representations
- Compact/expanded secret-key representations
- Signing by solving Oil-and-Vinegar systems
- Verification by public-map evaluation

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#uov`.

## Facts requiring citation

- uov-Ip/uov-Is/uov-III/uov-V key and signature sizes
- Compact vs expanded key sizes
- Security level claims
- Any benchmark claim

## Teaching warning

UOV is a useful baseline for explaining multivariate signatures, but do not present it as having small keys; the compact public keys are still large compared with many lattice/hash-based signatures.
