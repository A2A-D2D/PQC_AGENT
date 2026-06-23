# Falcon / FN-DSA Card

## Basic role

Falcon is a lattice/NTRU-based digital signature scheme on the selected future-standard track as represented in this corpus. FN-DSA / FIPS 206 material is present as status material, but a final FIPS 206 document is not present.

## Traditional-crypto analogy

Closest role: ECDSA/RSA-PSS replacement for digital signatures.

## Implementation warning

Falcon is often attractive because of compact signatures, but implementation is more complex than ML-DSA because it involves FFT-like arithmetic and Gaussian sampling.

## Sources in corpus

- `03_selected_future_standards/Falcon_specification_falcon-sign_2020.pdf`
- `03_selected_future_standards/FIPS_206_FN-DSA_status_presentation_2025.pdf`

## Agent rule

Do not claim final FIPS 206 standard status unless a final FIPS 206 document is added.
