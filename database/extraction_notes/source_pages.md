# Extraction Notes and Source Pages

This file records where the v2 extracted tables came from. It is intended to make later manual review easier and to prevent the tutor agent from treating unchecked values as authoritative.

## Extraction method

- Primary method: PyMuPDF text extraction from the uploaded PDF corpus.
- Table reconstruction: manual reconstruction from extracted text around the relevant tables.
- OCR: not used.
- Visual verification: recommended before publication or before using exact values in a formal report.

## Source notes

### Falcon / FN-DSA-track

- Source file: `03_selected_future_standards/Falcon_specification_falcon-sign_2020.pdf`.
- Parameter data: Section 3.11.5 and Table 3.3.
- Important fields extracted:
  - Falcon-512 / Falcon-1024.
  - n, q, sigma, sigma_min, sigma_max.
  - max signature square norm.
  - public key and signature bytes.
  - private key bytes derived from fixed-width private-key encoding.
- Review note: final FIPS 206 / FN-DSA is not present in this corpus, so these values must not be labeled as final FIPS 206 values.

### HQC

- Source file: `03_selected_future_standards/HQC_specification_2025-08-22.pdf`.
- Parameter data: Table 5 and Table 6.
- Software benchmark data: Table 7 and Table 8.
- Important fields extracted:
  - HQC-1 / HQC-3 / HQC-5.
  - n1, n2, n, k, omega, omega_r, omega_e, DFR.
  - encapsulation key, decapsulation key, compressed decapsulation key, ciphertext, shared key bytes.
  - reference and AVX2 software-cycle tables.
- Review note: final NIST FIPS text for HQC is not present in this corpus.

### Aigis-enc

- Source file: `05_china_related/Aigis-enc算法设计文档.pdf`.
- Parameter data: Table 1.
- Software benchmark data: Table 2.
- Important fields extracted:
  - PARAMS I / PARAMS II / PARAMS III.
  - n, k, q, eta1, eta2, dt, du, dv.
  - public key, secret key, compact secret key, ciphertext, shared secret bytes.
  - DFR and security estimates.
  - AVX2 CPU-cycle benchmark values.
- Review note: keep as China-related design-document material. Do not present as NIST/FIPS standard.

### Aigis-sig

- Source file: `05_china_related/Aigis-sig算法设计文档.pdf`.
- Parameter data: Table 1.
- Software benchmark data: Table 2.
- Important fields extracted:
  - PARAMS I / PARAMS II / PARAMS II-b / PARAMS III.
  - n, k, l, q, d, omega, eta1, eta2, beta1, beta2, gamma1, gamma2.
  - public key, secret key, signature bytes.
  - expected signing-loop count.
  - AVX2 CPU-cycle benchmark values.
- Review note: compare structurally with ML-DSA only as a teaching analogy; do not state equivalence without source.

### Scloud+

- Source file: `05_china_related/Scloud+.pdf`.
- Parameter data: Table 2, Table 3, Table 4, and Table 6.
- Software benchmark data: Table 5.
- Important fields extracted:
  - Scloud+-128 / Scloud+-192 / Scloud+-256.
  - q, q1, q2, m, n, mbar, nbar, h1, h2, eta1, eta2.
  - key/ciphertext/shared-secret sizes.
  - classical/quantum security estimates and DFR.
  - MsgEnc/MsgDec parameters: mu, tau, coding lattice, shaping lattice.
  - software-cycle values in 10^3 cycles.
- Review note: keep paper-level Scloud+ parameters separate from any local RTL/demo parameterization.

### CTRU / CNTR research paper

- Source file: `05_china_related/CTRU.pdf`.
- Parameter data: Table I.
- Benchmark platform notes: benchmark section, but full cycle-value table not reconstructed in v2.
- Important fields extracted:
  - CTRU and CNTR comparison rows.
  - assumptions, ring, n, q, public key bytes, ciphertext bytes, bandwidth bytes, security estimates, DFR.
- Review note: do not silently merge this table with the Chinese draft CTRU parameter table; they use different named parameter sets and sometimes different n values.

### CTRU Chinese draft

- Source file: `05_china_related/基于NTRU的密钥封装机制-征求意见稿.pdf`.
- Parameter data: Table 1, Table 2, and Table 3.
- Important fields extracted:
  - CTRU-576 / CTRU-768 / CTRU-1024.
  - CTRU-Light.
  - CTRU-Prime.
  - ring family, n, n_prime, q, q2, Psi1, Psi2.
  - secret key, public key, ciphertext, shared key bytes.
  - classical/quantum security estimates.
- Review note: this is a draft in the corpus. Do not claim final GM/T or national-standard status unless a final issued standard source is added.

### NEV

- Source file: `05_china_related/NEV.pdf`.
- Parameter/comparison data: Table 1.
- Important fields extracted:
  - NEV-512 / NEV'-512 / NEV-1024 / NEV'-1024.
  - public key bytes, secret key bytes, ciphertext bytes.
  - DFR and LWE estimator bits.
- Review note: NEV performance values were not reconstructed in v2; only the comparison table is included.

### Additional-signature Round 3 candidates

- Source directory: `04_nist_additional_signatures_round3/`.
- Candidate files present:
  - `FAEST_v2_specification_2025.pdf`
  - `HAWK_v1.1_specification.pdf`
  - `MAYO_round2_specification_2025.pdf`
  - `MQOM_round2_specification_2025.pdf`
  - `QR-UOV_v2.0_specification_2025.pdf`
  - `SDitH_round2_specification_2025.pdf`
  - `SNOVA_round2_specification_2025.pdf`
  - `SQIsign_v2.0.1_specification_2025.pdf`
  - `UOV_round2_specification_2025.pdf`
- Status in v2:
  - candidate list recorded;
  - exact parameter/key/signature-size tables not yet extracted.
- Review note: do not answer exact sizes for these candidates until the parameter tables are added.

## Suggested next extraction tasks

1. Reconstruct exact parameter and size tables for the nine additional-signature Round 3 candidates.
2. Visually verify all China-related tables where PDF text extraction may have disrupted table alignment.
3. Reconstruct software benchmark tables for CTRU/CNTR and NEV if needed.
4. Add hardware benchmark tables only from explicit FPGA/ASIC papers or synthesis reports; do not infer hardware numbers from software benchmarks.

## v3 update: Additional-signature Round 3 candidates

The v3 update reconstructed candidate parameter/key/signature-size tables for the nine NIST Additional Digital Signatures Round 3 candidates. The detailed extracted tables are stored in:

- `database/metadata/additional_signatures_round3_tables.md`

### FAEST

- Source file: `04_nist_additional_signatures_round3/FAEST_v2_specification_2025.pdf`.
- Extracted from: Section 3 main-parameter table around `FAEST and FAEST-EM Parameter Sets`.
- Important extracted fields:
  - FAEST and FAEST-EM 128/192/256, short/fast variants.
  - OWF description, ell, tau, wgrind, Topen, B, nleafcom.
  - Public key and signature bytes.
- Review note:
  - Secret-key bytes in the v3 table are derived from OWF key length, not directly listed in the source table.

### HAWK

- Source file: `04_nist_additional_signatures_round3/HAWK_v1.1_specification.pdf`.
- Extracted from: Table 4, `Parameter sets for HAWK`.
- Important extracted fields:
  - HAWK-256 challenge set, HAWK-512, HAWK-1024.
  - Key/signature sizes, degree, security target, sampling eta, sigma values, salt/keygen/hpub lengths.
- Review note:
  - HAWK-256 is a challenge/cryptanalytic target, not a recommended NIST security level set.

### MAYO

- Source file: `04_nist_additional_signatures_round3/MAYO_round2_specification_2025.pdf`.
- Extracted from: Table 2.1.
- Important extracted fields:
  - MAYO1, MAYO2, MAYO3, MAYO5.
  - q, n, m, o, k, salt/digest/pk seed bytes.
  - compact/expanded key sizes and signature sizes.
- Review note:
  - Table 2.2 contains additional trade-off parameter sets but v3 records only the main selected parameter sets.

### MQOM

- Source file: `04_nist_additional_signatures_round3/MQOM_round2_specification_2025.pdf`.
- Extracted from: Table 6 and Table 7.
- Important extracted fields:
  - NIST security category, field size, m=n, tau, N, mu, eta, w.
  - Public key, secret key, and 3-round/5-round signature sizes.
- Review note:
  - Rows share a `3r/5r` label; v3 splits signature size into `Signature bytes 3r` and `Signature bytes 5r`.

### QR-UOV

- Source file: `04_nist_additional_signatures_round3/QR-UOV_v2.0_specification_2025.pdf`.
- Extracted from: Table 1, Table 2, Table 3, and Table 5.
- Important extracted fields:
  - Main `(q=127, ell=3)` parameter sets for security levels I, III, and V.
  - Additional trade-off parameter sets.
  - Auxiliary n, N, V, M, tau1, tau2, tau3.
  - Public/private key and signature sizes.
- Review note:
  - Source text states `(q=127, ell=3)` is the recommended choice due to balance; other rows are retained as additional trade-off sets.

### SDitH

- Source file: `04_nist_additional_signatures_round3/SDitH_round2_specification_2025.pdf`.
- Extracted from: Table 3, Table 4, Table 7, Table 8, and Table 9.
- Important extracted fields:
  - Main GF(2) RSD parameters and proof-system/key/signature sizes.
  - GF(256) alternative instances.
  - TCitH variant signature sizes.
- Review note:
  - TCitH variant table states key sizes are similar to the main VOLEitH-based instances; v3 only records signature sizes for those variants.

### SNOVA

- Source file: `04_nist_additional_signatures_round3/SNOVA_round2_specification_2025.pdf`.
- Extracted from: Table 6.
- Important extracted fields:
  - `(v, o, q, l)` parameter sets for security levels I, III, and V.
  - Public-key size, signature size, expanded secret-key size, seed-type secret-key size.
- Review note:
  - Some sizes are reported as half-byte values in the source. v3 preserves the source values and warns that API constants should be visually verified before formal use.

### SQIsign

- Source file: `04_nist_additional_signatures_round3/SQIsign_v2.0.1_specification_2025.pdf`.
- Extracted from: Table 4.
- Important extracted fields:
  - NIST-I, NIST-III, NIST-V public key, secret key, and signature sizes.
- Review note:
  - v3 records only key/signature-size values, not full isogeny parameter internals.

### UOV

- Source file: `04_nist_additional_signatures_round3/UOV_round2_specification_2025.pdf`.
- Extracted from: Table 4.
- Important extracted fields:
  - uov-Ip, uov-Is, uov-III, uov-V.
  - n, m, q.
  - expanded/compact public-key and secret-key sizes.
  - signature bytes.
- Review note:
  - Source table states salt_len = 128, pk_seed_len = 128, and sk_seed_len = 256 for all sets.
