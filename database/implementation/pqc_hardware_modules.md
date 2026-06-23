# PQC Hardware Modules

## Common modules

- Keccak/SHAKE or SHA2/SHAKE hash/XOF blocks
- NTT / INTT for lattice schemes using polynomial multiplication
- modular addition/subtraction/multiplication/reduction
- sampling / rejection sampling / CBD-like sampling depending on scheme
- pack / unpack / compression / decompression
- hint/decompose logic for ML-DSA-style schemes
- memory banking and data-movement control

## Hardware-data warning

This file is conceptual. Do not use it as a source for LUT, FF, DSP, BRAM, cycle count, frequency, area, or power. Put those numbers in `metadata/benchmark_tables.md` only after extracting from a cited paper or synthesis report.
