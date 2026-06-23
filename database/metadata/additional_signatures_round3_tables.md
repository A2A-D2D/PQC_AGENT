# NIST Additional Digital Signatures Round 3 Candidate Tables

These tables supplement `parameter_tables_extended.md` with the nine candidates that NIST advanced to Round 3 of the Additional Digital Signatures process in May 2026.

**Status rule:** these are **Round 3 candidate specification values**, not final NIST/FIPS standard values. If an updated Round 3 specification is later added, re-extract and supersede these tables.

**Extraction rule:** values below were reconstructed from the candidate PDFs in `04_nist_additional_signatures_round3/`. Use these for database-backed tutoring, but visually verify against the original PDF before using exact values in a formal report.

## Candidate landscape

| Candidate | Broad family / teaching bucket | Primary role | Candidate status | Source file |
|---|---|---|---|---|
| FAEST | Symmetric-key / AES/Rijndael OWF + VOLE-in-the-head | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/FAEST_v2_specification_2025.pdf` |
| HAWK | Lattice / NTRU-style hash-and-sign | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/HAWK_v1.1_specification.pdf` |
| MAYO | Multivariate / Oil-and-Vinegar variant | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/MAYO_round2_specification_2025.pdf` |
| MQOM | Multivariate MQ + MPC/TCitH-style proof | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/MQOM_round2_specification_2025.pdf` |
| QR-UOV | Multivariate / quotient-ring UOV | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/QR-UOV_v2.0_specification_2025.pdf` |
| SDitH | Code-based / syndrome decoding in the head | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/SDitH_round2_specification_2025.pdf` |
| SNOVA | Multivariate / structured UOV over rings | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/SNOVA_round2_specification_2025.pdf` |
| SQIsign | Isogeny-based signature | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/SQIsign_v2.0.1_specification_2025.pdf` |
| UOV | Multivariate / unbalanced oil-and-vinegar | Signature | NIST additional-signatures Round 3 candidate | `04_nist_additional_signatures_round3/UOV_round2_specification_2025.pdf` |

## FAEST

Source: `FAEST_v2_specification_2025.pdf`, Section 3 main-parameter table.

Note: the source table lists public-key and signature sizes. Secret-key bytes below are derived from the OWF key length: AES-128/Rijndael-128 -> 16 B, AES-192/Rijndael-192 -> 24 B, AES-256/Rijndael-256 -> 32 B. Keep the derived status in mind.

| Parameter set | OWF / public-key relation | Security target | ell | tau | wgrind | Topen | B | nleafcom | Public key bytes | Secret key bytes | Signature bytes | Source note |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| FAEST-128s | AES128_k(x) | NIST-I style / 128-bit | 1280 | 11 | 7 | 102 | 16 | 3 | 32 | 16 | 4506 | sk bytes derived from AES-128 key length. |
| FAEST-128f | AES128_k(x) | NIST-I style / 128-bit | 1280 | 16 | 8 | 110 | 16 | 3 | 32 | 16 | 5924 | sk bytes derived from AES-128 key length. |
| FAEST-192s | AES192_k(x) || AES192_k(x xor 1) | NIST-III style / 192-bit | 2496 | 16 | 12 | 162 | 16 | 3 | 48 | 24 | 11260 | sk bytes derived from AES-192 key length. |
| FAEST-192f | AES192_k(x) || AES192_k(x xor 1) | NIST-III style / 192-bit | 2496 | 24 | 8 | 163 | 16 | 3 | 48 | 24 | 14948 | sk bytes derived from AES-192 key length. |
| FAEST-256s | AES256_k(x) || AES256_k(x xor 1) | NIST-V style / 256-bit | 3104 | 22 | 6 | 245 | 16 | 3 | 48 | 32 | 20696 | sk bytes derived from AES-256 key length. |
| FAEST-256f | AES256_k(x) || AES256_k(x xor 1) | NIST-V style / 256-bit | 3104 | 32 | 8 | 246 | 16 | 3 | 48 | 32 | 26548 | sk bytes derived from AES-256 key length. |
| FAEST-EM-128s | AES128_x(k) xor k | NIST-I style / 128-bit | 960 | 11 | 7 | 103 | 16 | 2 | 32 | 16 | 3906 | sk bytes derived from AES-128 key length. |
| FAEST-EM-128f | AES128_x(k) xor k | NIST-I style / 128-bit | 960 | 16 | 8 | 112 | 16 | 2 | 32 | 16 | 5060 | sk bytes derived from AES-128 key length. |
| FAEST-EM-192s | Rijndael192_x(k) xor k | NIST-III style / 192-bit | 1728 | 16 | 8 | 162 | 16 | 2 | 48 | 24 | 9340 | sk bytes derived from Rijndael-192 key length. |
| FAEST-EM-192f | Rijndael192_x(k) xor k | NIST-III style / 192-bit | 1728 | 24 | 8 | 176 | 16 | 2 | 48 | 24 | 12380 | sk bytes derived from Rijndael-192 key length. |
| FAEST-EM-256s | Rijndael256_x(k) xor k | NIST-V style / 256-bit | 2688 | 22 | 6 | 218 | 16 | 2 | 64 | 32 | 17984 | sk bytes derived from Rijndael-256 key length. |
| FAEST-EM-256f | Rijndael256_x(k) xor k | NIST-V style / 256-bit | 2688 | 32 | 8 | 234 | 16 | 2 | 64 | 32 | 23476 | sk bytes derived from Rijndael-256 key length. |

Teaching note: present FAEST as “prove knowledge of a block-cipher key mapping x to y,” using symmetric primitives plus zero-knowledge/VOLE-in-the-head machinery. Do not present it as a lattice or multivariate scheme.

## HAWK

Source: `HAWK_v1.1_specification.pdf`, Table 4.

| Parameter set | Targeted security | Bit security lambda | Degree n | Private key bytes | Public key bytes | Signature bytes | Transcript size limit qs | Sampling eta | sigma_sign | sigma_verify | sigma_krsec | Salt bits | Keygen seed bits | Hashed pubkey bits | Source note |
|---|---|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|---:|---|
| HAWK-256 | Challenge | 64 | 256 | 96 | 450 | 249 | 2^32 | 2 | 1.010 | 1.042 | 1.042 | 112 | 128 | 128 | Challenge/cryptanalytic target, not a NIST security level candidate. |
| HAWK-512 | NIST-I | 128 | 512 | 184 | 1024 | 555 | 2^64 | 4 | 1.278 | 1.425 | 1.425 | 192 | 192 | 256 | Main parameter set. |
| HAWK-1024 | NIST-V | 256 | 1024 | 360 | 2440 | 1221 | 2^64 | 8 | 1.299 | 1.571 | 1.974 | 320 | 320 | 512 | Main parameter set. |

Teaching note: HAWK is useful for showing that lattice signatures are not only ML-DSA/Falcon; however, it has different assumptions and implementation structure from ML-DSA.

## MAYO

Source: `MAYO_round2_specification_2025.pdf`, Table 2.1.

| Parameter set | Security level | q | n | m | o | k | salt bytes | digest bytes | pk seed bytes | f(z) | Compact secret key bytes | Compact public key bytes | Signature bytes | Expanded secret key size | Expanded public key size | Source note |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|---:|---|
| MAYO1 | 1 | 16 | 86 | 78 | 8 | 10 | 24 | 32 | 16 | f78(z) | 24 | 1420 | 454 | 141 KB | 142 KB | Smaller public keys, larger signatures at level 1. |
| MAYO2 | 1 | 16 | 81 | 64 | 17 | 4 | 24 | 32 | 16 | f64(z) | 24 | 4912 | 186 | 99 KB | 104 KB | Smaller signatures, larger public keys at level 1. |
| MAYO3 | 3 | 16 | 118 | 108 | 10 | 11 | 32 | 48 | 16 | f108(z) | 32 | 2986 | 681 | 367 KB | 370 KB | Main level-3 set. |
| MAYO5 | 5 | 16 | 154 | 142 | 12 | 12 | 40 | 64 | 16 | f142(z) | 40 | 5554 | 964 | 822 KB | 828 KB | Main level-5 set. |

Teaching note: MAYO is a compact-key multivariate signature family. A useful quickstart analogy is “Oil-and-Vinegar with a modified structure to shrink public keys.”

## MQOM

Source: `MQOM_round2_specification_2025.pdf`, Table 6 and Table 7.

Note: rows marked `3r/5r` share most parameters but have two signature sizes; the source states the signature-size difference comes from the proof-system parameter eta.

| Parameter set | NIST security category | Field size | m = n | tau | N | mu | eta 3r / 5r | w | Public key bytes | Secret key bytes | Signature bytes 3r | Signature bytes 5r | Source note |
|---|---|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|---:|---|
| MQOM2-L1-gf2-short-3r/5r | Cat. I | 2 | 160 | 12 | 2048 | 16 | 10 / 8 | 8 | 52 | 72 | 2868 | 2820 | Short level-1 GF(2) set. |
| MQOM2-L1-gf256-short-3r/5r | Cat. I | 256 | 48 | 12 | 2048 | 2 | 24 / 8 | 8 | 80 | 128 | 3540 | 3156 | Short level-1 GF(256) set. |
| MQOM2-L1-gf2-fast-3r/5r | Cat. I | 2 | 160 | 17 | 256 | 8 | 20 / 16 | 9 | 52 | 72 | 3212 | 3144 | Fast level-1 GF(2) set. |
| MQOM2-L1-gf256-fast-3r/5r | Cat. I | 256 | 48 | 17 | 256 | 1 | 48 / 16 | 9 | 80 | 128 | 4164 | 3620 | Fast level-1 GF(256) set. |
| MQOM2-L3-gf2-short-3r/5r | Cat. III | 2 | 240 | 18 | 2048 | 16 | 15 / 12 | 12 | 78 | 108 | 6388 | 6280 | Short level-3 GF(2) set. |
| MQOM2-L3-gf256-short-3r/5r | Cat. III | 256 | 72 | 18 | 2048 | 2 | 36 / 12 | 12 | 120 | 192 | 7900 | 7036 | Short level-3 GF(256) set. |
| MQOM2-L3-gf2-fast-3r/5r | Cat. III | 2 | 240 | 27 | 256 | 8 | 30 / 24 | 3 | 78 | 108 | 7576 | 7414 | Fast level-3 GF(2) set. |
| MQOM2-L3-gf256-fast-3r/5r | Cat. III | 256 | 72 | 27 | 256 | 1 | 72 / 24 | 3 | 120 | 192 | 9844 | 8548 | Fast level-3 GF(256) set. |
| MQOM2-L5-gf2-short-3r/5r | Cat. V | 2 | 320 | 25 | 2048 | 16 | 20 / 16 | 6 | 104 | 144 | 11764 | 11564 | Short level-5 GF(2) set. |
| MQOM2-L5-gf256-short-3r/5r | Cat. V | 256 | 96 | 25 | 2048 | 2 | 48 / 16 | 6 | 160 | 256 | 14564 | 12964 | Short level-5 GF(256) set. |
| MQOM2-L5-gf2-fast-3r/5r | Cat. V | 2 | 320 | 36 | 256 | 8 | 40 / 32 | 4 | 104 | 144 | 13412 | 13124 | Fast level-5 GF(2) set. |
| MQOM2-L5-gf256-fast-3r/5r | Cat. V | 256 | 96 | 36 | 256 | 1 | 96 / 32 | 4 | 160 | 256 | 17444 | 15140 | Fast level-5 GF(256) set. |

Teaching note: MQOM is a good example of “prove knowledge of a solution to an MQ instance” using in-the-head proof techniques. Do not group it with plain UOV just because both are multivariate.

## QR-UOV

Source: `QR-UOV_v2.0_specification_2025.pdf`, Table 1, Table 2, Table 3, and Table 5.

### QR-UOV main parameter sets

The specification states that the `(q=127, ell=3)` sets are recommended because of their balance of public-key size, signature size, and speed.

| Security level | q | v | m | ell | n | N | V | M | tau1 | tau2 | tau3 | Public key bytes | Private key bytes | Signature bytes | Source note |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| I | 127 | 156 | 54 | 3 | 210 | 70 | 52 | 18 | 4267 | 2916 | 82 | 24255 | 32 | 200 | Main recommended set. |
| III | 127 | 228 | 78 | 3 | 306 | 102 | 76 | 26 | 9020 | 6123 | 120 | 71891 | 48 | 292 | Main recommended set. |
| V | 127 | 306 | 105 | 3 | 411 | 137 | 102 | 35 | 16144 | 11018 | 162 | 173676 | 64 | 392 | Main recommended set. |

### QR-UOV additional parameter sets

| Security level | q | v | m | ell | n | N | V | M | tau1 | tau2 | tau3 | Public key bytes | Private key bytes | Signature bytes | Source note |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| I | 7 | 740 | 100 | 10 | 840 | 84 | 74 | 10 | 32629 | 8947 | 201 | 20641 | 32 | 331 | Additional trade-off set. |
| I | 31 | 165 | 60 | 3 | 225 | 75 | 55 | 20 | 4959 | 3571 | 104 | 23641 | 32 | 157 | Additional trade-off set. |
| I | 31 | 600 | 70 | 10 | 670 | 67 | 60 | 7 | 19242 | 4518 | 116 | 12266 | 32 | 435 | Additional trade-off set. |
| III | 7 | 1100 | 140 | 10 | 1240 | 124 | 110 | 14 | 71432 | 18461 | 289 | 55149 | 48 | 489 | Additional trade-off set. |
| III | 31 | 246 | 87 | 3 | 333 | 111 | 82 | 29 | 10878 | 7655 | 154 | 70983 | 48 | 232 | Additional trade-off set. |
| III | 31 | 890 | 100 | 10 | 990 | 99 | 89 | 10 | 41974 | 9507 | 169 | 34399 | 48 | 643 | Additional trade-off set. |
| V | 7 | 1490 | 190 | 10 | 1680 | 168 | 149 | 19 | 130305 | 33694 | 391 | 135407 | 64 | 662 | Additional trade-off set. |
| V | 31 | 324 | 114 | 3 | 438 | 146 | 108 | 38 | 18738 | 13145 | 203 | 158421 | 64 | 306 | Additional trade-off set. |
| V | 31 | 1120 | 120 | 10 | 1240 | 124 | 112 | 12 | 66236 | 14326 | 210 | 58532 | 64 | 807 | Additional trade-off set. |

Teaching note: QR-UOV is a good example for explaining public-key-size reduction in multivariate signatures by imposing quotient-ring structure, but the public keys are still much larger than lattice/hash-based standards in many parameter sets.

## SDitH

Source: `SDitH_round2_specification_2025.pdf`, Table 3, Table 4, Table 7, Table 8, and Table 9.

### SDitH main GF(2) instances

| Parameter set | NIST security category | Bits | q | n | n - k_rsd | k_rsd | w | Modeling mu | tau | kappa | wpow | Topen | B | Public key bytes | Secret key bytes | Signature avg bytes | Signature max bytes | Source note |
|---|---|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| SDitH2-L1-gf2-short | I | 143 | 2 | 10360 | 432 | 9928 | 56 | [4,4,4,3] | 11 | 11 | 9 | 107 | 16 | 70 | 163 | 3705 | 3705 | Main short level-1 set. |
| SDitH2-L1-gf2-fast | I | 143 | 2 | 10360 | 432 | 9928 | 56 | [4,4,4,3] | 16 | 8 | 2 | 101 | 16 | 70 | 163 | 4484 | 4484 | Main fast level-1 set. |
| SDitH2-L3-gf2-short | III | 207 | 2 | 18396 | 592 | 17804 | 73 | [4,4,4,4] | 16 | 12 | 2 | 157 | 16 | 98 | 232 | 7964 | 7964 | Main short level-3 set. |
| SDitH2-L3-gf2-fast | III | 207 | 2 | 18396 | 592 | 17804 | 73 | [4,4,4,4] | 24 | 8 | 2 | 153 | 16 | 98 | 232 | 9916 | 9916 | Main fast level-3 set. |
| SDitH2-L5-gf2-short | V | 272 | 2 | 19864 | 800 | 19064 | 104 | [4,4,4,3] | 21 | 12 | 6 | 216 | 16 | 132 | 307 | 14121 | 14121 | Main short level-5 set. |
| SDitH2-L5-gf2-fast | V | 272 | 2 | 19864 | 800 | 19064 | 104 | [4,4,4,3] | 32 | 8 | 2 | 207 | 16 | 132 | 307 | 17540 | 17540 | Main fast level-5 set. |

### SDitH GF(256) alternative instances

| Parameter set | NIST security category | Bits | q | n | n - k_rsd | k_rsd | w | Modeling mu | tau | kappa | wpow | Topen | B | Public key bytes | Secret key bytes | Signature bytes | Baseline GF(2) signature bytes | Source note |
|---|---|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| SDitH2-L1-gf256-short | I | 143 | 256 | 2176 | 64 | 2112 | 34 | [4,4,4] | 11 | 11 | 9 | 107 | 16 | 80 | 169 | 3661 | 3705 | Alternative GF(256) set. |
| SDitH2-L1-gf256-fast | I | 143 | 256 | 2176 | 64 | 2112 | 34 | [4,4,4] | 16 | 8 | 2 | 101 | 16 | 80 | 169 | 4420 | 4484 | Alternative GF(256) set. |
| SDitH2-L3-gf256-short | III | 207 | 256 | 3200 | 96 | 3104 | 50 | [4,4,4] | 16 | 12 | 2 | 157 | 16 | 120 | 251 | 7916 | 7964 | Alternative GF(256) set. |
| SDitH2-L3-gf256-fast | III | 207 | 256 | 3200 | 96 | 3104 | 50 | [4,4,4] | 24 | 8 | 2 | 153 | 16 | 120 | 251 | 9844 | 9916 | Alternative GF(256) set. |
| SDitH2-L5-gf256-short | V | 272 | 256 | 4224 | 120 | 4104 | 66 | [4,4,4] | 21 | 12 | 6 | 216 | 16 | 152 | 325 | 14079 | 14121 | Alternative GF(256) set. |
| SDitH2-L5-gf256-fast | V | 272 | 256 | 4224 | 120 | 4104 | 66 | [4,4,4] | 32 | 8 | 2 | 207 | 16 | 152 | 325 | 17476 | 17540 | Alternative GF(256) set. |

### SDitH TCitH variant signatures

Key sizes are stated by the source to be similar to the main VOLEitH-based instances.

| Parameter set | tau | kappa | wpow | Topen | Signature bytes | Baseline VOLEitH signature bytes | Source note |
|---|---:|---:|---:|---:|---:|---:|---|
| SDitH2-TCitH-L1-gf2-short | 14 | 11 | 2 | 125 | 4271 | 3705 | TCitH variant. |
| SDitH2-TCitH-L1-gf2-fast | 21 | 8 | 2 | 135 | 5509 | 4484 | TCitH variant. |
| SDitH2-TCitH-L3-gf2-short | 19 | 12 | 2 | 185 | 8426 | 7964 | TCitH variant. |
| SDitH2-TCitH-L3-gf2-fast | 31 | 8 | 6 | 212 | 11374 | 9916 | TCitH variant. |
| SDitH2-TCitH-L5-gf2-short | 25 | 12 | 6 | 265 | 15618 | 14121 | TCitH variant. |
| SDitH2-TCitH-L5-gf2-fast | 42 | 8 | 4 | 280 | 19968 | 17540 | TCitH variant. |

Teaching note: SDitH is useful for teaching code-based digital signatures separately from code-based KEMs such as HQC. Emphasize syndrome decoding and proof-system overhead.

## SNOVA

Source: `SNOVA_round2_specification_2025.pdf`, Table 6.

Note: the source table reports several public-key/signature sizes as half-byte values because of F16 element packing. Before using these values as API byte-string lengths, visually verify the API constants in the implementation/specification.

| Security level | v | o | q | l | Public key size bytes | Signature size bytes | Expanded secret key bytes | Seed-type secret key bytes | Source note |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| I | 37 | 17 | 16 | 2 | 9842 | 124 | 91440 | 48 | l=2 set. |
| I | 25 | 8 | 16 | 3 | 2320 | 164.5 | 39576 | 48 | l=3 set. |
| I | 24 | 5 | 16 | 4 | 1016 | 248 | 36848 | 48 | l=4 set; highlighted in introduction as compact public key at level I. |
| III | 56 | 25 | 16 | 2 | 31266 | 178 | 300848 | 48 | l=2 set. |
| III | 49 | 11 | 16 | 3 | 6005.5 | 286 | 177060 | 48 | l=3 set. |
| III | 37 | 8 | 16 | 4 | 4112 | 376 | 133040 | 48 | l=4 set. |
| III | 24 | 5 | 16 | 5 | 1578.5 | 378.5 | 60048 | 48 | l=5 set. |
| V | 75 | 33 | 16 | 2 | 71890 | 232 | 704532 | 48 | l=2 set. |
| V | 66 | 15 | 16 | 3 | 15203.5 | 380.5 | 435423 | 48 | l=3 set. |
| V | 60 | 10 | 16 | 4 | 8016 | 576 | 395248 | 48 | l=4 set. |
| V | 29 | 6 | 16 | 5 | 2716 | 453.5 | 100398 | 48 | l=5 set. |

Teaching note: SNOVA is useful for explaining how structured multivariate schemes try to reduce public-key size. Keep it distinct from plain UOV and QR-UOV.

## SQIsign

Source: `SQIsign_v2.0.1_specification_2025.pdf`, Table 4.

| Parameter set | Security level | Public key bytes | Secret key bytes | Signature bytes | Source note |
|---|---|---:|---:|---:|---|
| NIST-I | I | 65 | 353 | 148 | Key and signature sizes table. |
| NIST-III | III | 97 | 529 | 224 | Key and signature sizes table. |
| NIST-V | V | 129 | 701 | 292 | Key and signature sizes table. |

Teaching note: SQIsign is the main isogeny-based Round 3 candidate in this corpus. It has very compact public keys and signatures, but the implementation and mathematics are much more specialized than ML-DSA or UOV-style schemes.

## UOV

Source: `UOV_round2_specification_2025.pdf`, Table 4.

Note: `epk/esk` are expanded public/secret keys; `cpk/csk` are compact public/secret keys. The source states `salt_len = 128`, `pk_seed_len = 128`, and `sk_seed_len = 256` for all sets.

| Parameter set | NIST security level | n | m | q | Expanded public key bytes | Expanded secret key bytes | Compact public key bytes | Compact secret key bytes | Signature bytes | Source note |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| uov-Ip | 1 | 112 | 44 | 256 | 278432 | 237896 | 43576 | 32 | 128 | Level-1 set optimized for compressed public key size. |
| uov-Is | 1 | 160 | 64 | 16 | 412160 | 348704 | 66576 | 32 | 96 | Level-1 set optimized for shorter signatures. |
| uov-III | 3 | 184 | 72 | 256 | 1225440 | 1044320 | 189232 | 32 | 200 | Level-3 set. |
| uov-V | 5 | 244 | 96 | 256 | 2869440 | 2436704 | 446992 | 32 | 260 | Level-5 set. |

Teaching note: UOV is the baseline multivariate family to use when introducing Oil-and-Vinegar signatures. It has short signatures but large public keys, especially in expanded form.

## Agent usage rules for this file

1. Do not state that any Round 3 candidate has become a final standard unless a later final-standard source is added.
2. When answering exact key/signature-size questions, cite this file plus the original source PDF/table.
3. For teaching, group the candidates by family rather than listing all parameter rows first.
4. For performance comparisons, do not compare these key/signature sizes alone; include signing/verification cost and implementation assumptions if making deployment claims.
5. If a future updated Round 3 specification changes any numbers, mark this file as superseded rather than silently editing without an extraction note.
