# Parameter Tables

Rule: numeric parameters in this file must be copied from primary sources. If a field is unknown or not yet checked, use `TODO` or `not_in_current_table`; do not guess.

## ML-KEM - FIPS 203

Source: `01_nist_standards/NIST_FIPS_203_ML-KEM_2024.pdf`, Table 2 and Table 3.

| Parameter set | Type | Security category | n | q | k | eta1 | eta2 | du | dv | Required RBG strength (bits) | Encapsulation key bytes | Decapsulation key bytes | Ciphertext bytes | Shared secret bytes |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| ML-KEM-512 | KEM | 1 | 256 | 3329 | 2 | 3 | 2 | 10 | 4 | 128 | 800 | 1632 | 768 | 32 |
| ML-KEM-768 | KEM | 3 | 256 | 3329 | 3 | 2 | 2 | 10 | 4 | 192 | 1184 | 2400 | 1088 | 32 |
| ML-KEM-1024 | KEM | 5 | 256 | 3329 | 4 | 2 | 2 | 11 | 5 | 256 | 1568 | 3168 | 1568 | 32 |

Agent note: in teaching mode, describe ML-KEM as playing a protocol role closer to ECDH/key establishment than to AES/bulk encryption.

## ML-DSA - FIPS 204

Source: `01_nist_standards/NIST_FIPS_204_ML-DSA_2024.pdf`, Table 1 and Table 2.

| Parameter set | Type | Security category | q | zeta | d | tau | lambda | gamma1 | gamma2 | (k, l) | eta | beta | omega | Private key bytes | Public key bytes | Signature bytes |
|---|---|---:|---:|---:|---:|---:|---:|---|---|---|---:|---:|---:|---:|---:|---:|
| ML-DSA-44 | Signature | 2 | 8380417 | 1753 | 13 | 39 | 128 | 2^17 | (q-1)/88 | (4,4) | 2 | 78 | 80 | 2560 | 1312 | 2420 |
| ML-DSA-65 | Signature | 3 | 8380417 | 1753 | 13 | 49 | 192 | 2^19 | (q-1)/32 | (6,5) | 4 | 196 | 55 | 4032 | 1952 | 3309 |
| ML-DSA-87 | Signature | 5 | 8380417 | 1753 | 13 | 60 | 256 | 2^19 | (q-1)/32 | (8,7) | 2 | 120 | 75 | 4896 | 2592 | 4627 |

Agent note: ML-DSA-44 is category 2, not category 1. Avoid simplifying it into a 128/192/256-bit table without stating the NIST category mapping.

## SLH-DSA - FIPS 205

Source: `01_nist_standards/NIST_FIPS_205_SLH-DSA_2024.pdf`, Table 2.

The SHA2 and SHAKE versions with the same security level and `s`/`f` suffix share the same numeric parameter row.

| Parameter sets | Type | Security category | n | h | d | h' | a | k | lgw | m | Public key bytes | Signature bytes |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| SLH-DSA-SHA2-128s / SLH-DSA-SHAKE-128s | Hash-based signature | 1 | 16 | 63 | 7 | 9 | 12 | 14 | 4 | 30 | 32 | 7856 |
| SLH-DSA-SHA2-128f / SLH-DSA-SHAKE-128f | Hash-based signature | 1 | 16 | 66 | 22 | 3 | 6 | 33 | 4 | 34 | 32 | 17088 |
| SLH-DSA-SHA2-192s / SLH-DSA-SHAKE-192s | Hash-based signature | 3 | 24 | 63 | 7 | 9 | 14 | 17 | 4 | 39 | 48 | 16224 |
| SLH-DSA-SHA2-192f / SLH-DSA-SHAKE-192f | Hash-based signature | 3 | 24 | 66 | 22 | 3 | 8 | 33 | 4 | 42 | 48 | 35664 |
| SLH-DSA-SHA2-256s / SLH-DSA-SHAKE-256s | Hash-based signature | 5 | 32 | 64 | 8 | 8 | 14 | 22 | 4 | 47 | 64 | 29792 |
| SLH-DSA-SHA2-256f / SLH-DSA-SHAKE-256f | Hash-based signature | 5 | 32 | 68 | 17 | 4 | 9 | 35 | 4 | 49 | 64 | 49856 |

## Falcon / FN-DSA

| Parameter set | Type | Status in corpus | Public key bytes | Secret key bytes | Signature bytes | Source | Notes |
|---|---|---|---:|---:|---:|---|---|
| Falcon-512 / FN-DSA equivalent | Signature | selected future standard track; final FIPS 206 not in corpus | TODO | TODO | TODO | `03_selected_future_standards/Falcon_specification_falcon-sign_2020.pdf` | Fill only after checking the spec table and FIPS 206 final status. |
| Falcon-1024 / FN-DSA equivalent | Signature | selected future standard track; final FIPS 206 not in corpus | TODO | TODO | TODO | `03_selected_future_standards/Falcon_specification_falcon-sign_2020.pdf` | Fill only after checking the spec table and FIPS 206 final status. |

## HQC

| Parameter set | Type | Status in corpus | Public key bytes | Secret key bytes | Ciphertext bytes | Shared secret bytes | Source | Notes |
|---|---|---|---:|---:|---:|---:|---|---|
| TODO | KEM | selected future standard track; final FIPS not in corpus | TODO | TODO | TODO | TODO | `03_selected_future_standards/HQC_specification_2025-08-22.pdf` | Fill only after checking the HQC specification table. |

## China-related algorithms

| Algorithm | Type | Status in corpus | Parameter sets | Key / ciphertext / signature sizes | Source | Notes |
|---|---|---|---|---|---|---|
| Aigis-enc | KEM / encryption-family material | domestic candidate/research material | TODO | TODO | `05_china_related/Aigis-enc算法设计文档.pdf` | Do not treat as NIST standard. |
| Aigis-sig | Signature-family material | domestic candidate/research material | TODO | TODO | `05_china_related/Aigis-sig算法设计文档.pdf` | Do not treat as NIST standard. |
| Scloud+ | KEM / PKE-family material | domestic candidate/research material | TODO | TODO | `05_china_related/Scloud+.pdf` | Fill only from primary source tables. |
| CTRU | KEM / PKE-family material | domestic candidate/research material | TODO | TODO | `05_china_related/CTRU.pdf` | Fill only from primary source tables. |
| NEV | KEM / PKE-family material | domestic candidate/research material | TODO | TODO | `05_china_related/NEV.pdf` | Fill only from primary source tables. |
| LAC | KEM / PKE-family material | NIST round-1 comment material present | TODO | TODO | `05_china_related/LAC_NIST_round1_official_comment_2018.pdf` | Prefer original LAC spec if later added. |
