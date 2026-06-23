# Standard Status

This file summarizes status using only the uploaded corpus. If newer status is needed, verify against current NIST pages before answering.

## Published NIST standards in this corpus

| Standard | Algorithm | Function | Corpus source | Agent rule |
|---|---|---|---|---|
| FIPS 203 | ML-KEM | Key encapsulation mechanism | `01_nist_standards/NIST_FIPS_203_ML-KEM_2024.pdf` | Authoritative for ML-KEM parameters, sizes, and algorithm flow. |
| FIPS 204 | ML-DSA | Digital signature | `01_nist_standards/NIST_FIPS_204_ML-DSA_2024.pdf` | Authoritative for ML-DSA parameters, sizes, and algorithm flow. |
| FIPS 205 | SLH-DSA | Stateless hash-based digital signature | `01_nist_standards/NIST_FIPS_205_SLH-DSA_2024.pdf` | Authoritative for SLH-DSA parameters, sizes, and algorithm flow. |
| SP 800-227 | KEM recommendations | KEM usage and deployment guidance | `01_nist_standards/NIST_SP_800-227_KEM_Recommendations_2025.pdf` | Use for KEM deployment/security guidance, not for hardware benchmarks. |

## Selected future standards / not final FIPS in this corpus

| Algorithm / standard track | Status represented by corpus | Corpus source | Agent rule |
|---|---|---|---|
| Falcon / FN-DSA / FIPS 206 | Future-standard/signature track material is present, including Falcon spec and FIPS 206 status presentation. A final FIPS 206 document is not present in this corpus. | `03_selected_future_standards/Falcon_specification_falcon-sign_2020.pdf`; `03_selected_future_standards/FIPS_206_FN-DSA_status_presentation_2025.pdf` | Do not say Falcon/FN-DSA is final FIPS-standardized unless a final FIPS 206 source is added. |
| HQC | Selected future KEM standard material is present through HQC specification and NIST fourth-round status report. A final HQC FIPS document is not present in this corpus. | `03_selected_future_standards/HQC_specification_2025-08-22.pdf`; `02_nist_reports_migration/NIST_IR_8545_Fourth_Round_Status_HQC_2025.pdf` | Do not say HQC is final FIPS-standardized unless a final FIPS source is added. |

## Additional digital signature candidates in this corpus

These are candidate specifications, not final standards. NIST IR 8610 and the NIST CSRC update dated May 14, 2026 state that these nine algorithms advanced to Round 3 of the Additional Digital Signatures process:

- FAEST
- HAWK
- MAYO
- MQOM
- QR-UOV
- SDitH
- SNOVA
- SQIsign
- UOV

Corpus sources:

- `02_nist_reports_migration/NIST_IR_8610_Additional_Signatures_Round2_Status_2026.pdf`
- `04_nist_additional_signatures_round3/*.pdf`

Detailed candidate parameter/key/signature tables:

- `database/metadata/additional_signatures_round3_tables.md`

Agent rule: explain these as Round 3 candidates unless a newer official source says otherwise. Do not rank them by security, speed, area, or deployment readiness without a cited comparison source.

## China-related / domestic-potential material in this corpus

The corpus contains Aigis, CTRU, NEV, Scloud+, LAC-related material, a NTRU-based KEM consultation draft, and China-focused PQC presentations.

Agent rule: use these for domestic PQC landscape and teaching context. Do not treat them as NIST FIPS standards. Do not claim a Chinese national/industry standard status unless a primary standardization document is added.
