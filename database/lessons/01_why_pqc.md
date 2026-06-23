# Lesson 01 - Why PQC?

## One-sentence answer

PQC is mainly about replacing public-key mechanisms such as RSA, finite-field Diffie-Hellman, and ECC with algorithms believed to resist large-scale quantum attacks.

## Teaching bridge

If the audience already knows RSA/ECC, start from the fact that Shor-type quantum attacks threaten integer factorization and discrete logarithm assumptions. Then explain that symmetric cryptography such as AES and hash functions is affected differently and is not replaced wholesale by PQC.

## Safe claims

- PQC primarily targets key establishment and digital signatures.
- Bulk encryption remains symmetric in most protocols.
- Migration is a system problem, not just an algorithm swap.

## Facts requiring source

- exact standardization status;
- approved algorithm lists;
- security category mapping;
- migration deadlines or regulatory claims.
