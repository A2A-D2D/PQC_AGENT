# Facts Requiring Citation

Use this checklist before giving an answer.

## Can be explained without citation in teaching mode

- What a KEM is at a conceptual level.
- Why PQC is needed at a high level.
- Why RSA/ECC are threatened by large-scale quantum computers at a high level.
- Why AES/SHA are not replaced wholesale by PQC.
- Why NTT is useful for polynomial multiplication.
- Why sampling, packing, and hashing matter in lattice-based PQC.

## Must be cited or extracted from metadata

- Exact ML-KEM, ML-DSA, SLH-DSA parameter values.
- Key/ciphertext/signature sizes.
- Security categories.
- Standardization status.
- Candidate selection status.
- Any hardware performance/resource number.
- Any claim comparing algorithms or implementations.
- Any domestic standardization claim.

## Preferred source files for common questions

| Question type | Preferred source |
|---|---|
| ML-KEM parameter/size/algorithm | `NIST_FIPS_203_ML-KEM_2024.pdf` |
| ML-DSA parameter/size/algorithm | `NIST_FIPS_204_ML-DSA_2024.pdf` |
| SLH-DSA parameter/size/algorithm | `NIST_FIPS_205_SLH-DSA_2024.pdf` |
| KEM deployment guidance | `NIST_SP_800-227_KEM_Recommendations_2025.pdf` |
| NIST third/fourth round status | corresponding NIST IR files |
| Additional signature candidates | candidate spec + NIST IR 8610 |
| China/domestic algorithm landscape | China-related primary PDF, not a generic survey alone |
