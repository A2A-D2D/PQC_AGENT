# Software Benchmark Tables

Rule: values in this file are software/CPU benchmarks extracted from the current PDF corpus. They are **not** FPGA or ASIC hardware synthesis results. Do not compare rows across schemes unless platform, compiler, implementation style, and measurement method are explicitly aligned.

## Benchmark-use guardrails

When using this file, the tutor agent must state:

- whether the implementation is reference C, optimized C, AVX2, or another implementation;
- CPU model and clock setting if available;
- compiler and flags if available;
- whether the values are cycles, kilo-cycles, or time;
- whether the reported value is mean, median, or another statistic;
- that these numbers do not imply hardware area/latency.

## HQC reference implementation

Source: `03_selected_future_standards/HQC_specification_2025-08-22.pdf`, Table 7.

Platform notes from the specification:

- OS: Ubuntu 22.04.2 LTS 64-bit.
- CPU: Intel Core i7-11850H @ 2.50 GHz.
- Hyperthreading and Turbo Boost disabled.
- Memory: 32 GB.
- Compiler: gcc 11.4.0.
- Flags: `-O3 -std=c99 -funroll-all-loops -flto -pedantic -Wall -Wextra`.
- Values are in kilo-cycles.

| Instance | Implementation | KeyGen kcycles | Encaps kcycles | Decaps kcycles | Source |
|---|---|---:|---:|---:|---|
| HQC-1 | Reference implementation | 4557 | 9116 | 13918 | Table 7 |
| HQC-3 | Reference implementation | 13783 | 27571 | 41669 | Table 7 |
| HQC-5 | Reference implementation | 33123 | 66261 | 100213 | Table 7 |

## HQC AVX2 optimized implementation

Source: `03_selected_future_standards/HQC_specification_2025-08-22.pdf`, Table 8.

Platform notes from the specification:

- OS: Ubuntu 22.04.2 LTS 64-bit.
- CPU: Intel Core i7-11850H @ 2.50 GHz.
- Hyperthreading and Turbo Boost disabled.
- Memory: 32 GB.
- Compiler: gcc 8.2.1.
- Flags: `-O3 -std=c99 -funroll-all-loops -mavx -mavx2 -mpclmul -pedantic -Wall -Wextra`.
- Values are in kilo-cycles.

| Instance | Implementation | KeyGen kcycles | Encaps kcycles | Decaps kcycles | Source |
|---|---|---:|---:|---:|---|
| HQC-1 | AVX2 optimized | 76 | 150 | 353 | Table 8 |
| HQC-3 | AVX2 optimized | 181 | 355 | 732 | Table 8 |
| HQC-5 | AVX2 optimized | 363 | 720 | 1435 | Table 8 |

## Aigis-enc AVX2 implementation

Source: `05_china_related/Aigis-enc算法设计文档.pdf`, Table 2.

Platform notes from the document:

- OS: Windows 10 64-bit.
- CPU: Intel Core i7-6700 @ 3.4 GHz.
- Machine: ThinkCentre, 4 GB memory.
- Development environment: Microsoft Visual Studio 2017 or later.
- Values are CPU cycles, averaged over 10,000 runs.

| Parameter set | Implementation | KeyGen cycles | Encaps cycles | Decaps cycles | Source |
|---|---|---:|---:|---:|---|
| PARAMS I | AVX2 | 24686 | 35535 | 31540 | Table 2 |
| PARAMS II | AVX2 | 34456 | 49740 | 44745 | Table 2 |
| PARAMS III | AVX2 | 46291 | 62087 | 60153 | Table 2 |

## Aigis-sig AVX2 implementation

Source: `05_china_related/Aigis-sig算法设计文档.pdf`, Table 2.

Platform notes from the document:

- OS: Windows 10 64-bit.
- CPU: Intel Core i7-6700 @ 3.4 GHz.
- Machine: ThinkCentre, 4 GB memory.
- Development environment: Microsoft Visual Studio 2017 or later.
- Values are CPU cycles, averaged over 10,000 runs.

| Parameter set | Implementation | KeyGen cycles | Sign cycles | Verify cycles | Source |
|---|---|---:|---:|---:|---|
| PARAMS I | AVX2 | 75216 | 296716 | 78841 | Table 2 |
| PARAMS II | AVX2 | 112362 | 459903 | 104337 | Table 2 |
| PARAMS II-b | AVX2 | 102852 | 624031 | 104488 | Table 2 |
| PARAMS III | AVX2 | 140563 | 533880 | 136503 | Table 2 |

## Scloud+ software implementation

Source: `05_china_related/Scloud+.pdf`, Table 5.

Platform notes from the paper:

- OS: Fedora 33.
- CPU: Intel Core i9-10980XE @ 3.00 GHz.
- Hyperthreading and Turbo Boost disabled.
- Compiler: gcc 7.2.0.
- Command: `gcc -O3 -march=native -lm`.
- Values are in 10^3 cycles.
- Reported values are medians over 1,000 measurements.

| Instance | Implementation | KeyGen 10^3 cycles | Encaps 10^3 cycles | Decaps 10^3 cycles | Encaps + Decaps 10^3 cycles | Source |
|---|---|---:|---:|---:|---:|---|
| Scloud+.KEM-128 | Optimized software in paper | 1052 | 1115 | 1109 | 2224 | Table 5 |
| Scloud+.KEM-192 | Optimized software in paper | 2034 | 2226 | 2262 | 4488 | Table 5 |
| Scloud+.KEM-256 | Optimized software in paper | 3564 | 3738 | 3884 | 7622 | Table 5 |

## CTRU / CNTR software benchmarks

Source: `05_china_related/CTRU.pdf`.

Status: platform notes were found, but the cycle-value table has not yet been reconstructed in this v2 extraction.

Platform notes found in the paper:

- CPU: Intel Core i7-10510U @ 2.30 GHz.
- OS: Ubuntu 20.04.
- Compiler: gcc 9.4.0.
- Average over 10,000 test runs.

| Scheme | KeyGen cycles | Encaps cycles | Decaps cycles | Status |
|---|---:|---:|---:|---|
| CTRU/CNTR | TODO | TODO | TODO | Recheck source table visually before filling. |

## NEV software benchmarks

Source: `05_china_related/NEV.pdf`.

Status: performance table not yet reconstructed in this v2 extraction.

| Scheme | KeyGen cycles | Encaps cycles | Decaps cycles | Status |
|---|---:|---:|---:|---|
| NEV / NEV' | TODO | TODO | TODO | Recheck source table visually before filling. |
