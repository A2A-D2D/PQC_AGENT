# MQOM Card

## Basic role

MQOM is a post-quantum digital-signature candidate in the NIST Additional Digital Signatures Round 3 process.

## Family / teaching bucket

Multivariate MQ plus MPC/TCitH-style proof-of-knowledge signature.

## Traditional crypto analogy

Closest role: ECDSA / EdDSA / RSA-PSS replacement candidate.

## Core intuition

MQOM signs by proving knowledge of a solution to a multivariate quadratic instance, using an in-the-head proof construction. It combines MQ hardness with proof-system engineering.

## Implementation modules

- MQ system generation/evaluation
- Finite-field arithmetic over GF(2) or GF(256)
- MPC-in-the-head / TCitH-style transcript generation
- Commitments, openings, and hash challenges

## Parameter source

Use `database/metadata/additional_signatures_round3_tables.md#mqom`.

## Facts requiring citation

- 3-round vs 5-round signature sizes
- GF(2) vs GF(256) variants
- Public/secret key sizes
- Any benchmark claim

## Teaching warning

Do not group MQOM with plain UOV only because both are multivariate. MQOM’s proof-system layer is central to the design.
