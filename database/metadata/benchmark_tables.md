# Benchmark Tables

Rule: benchmark data is the highest-risk hallucination zone. Do not provide exact area, latency, frequency, power, LUT/FF/DSP/BRAM, or ranking unless a row in this file or a cited paper table supports it.

## Hardware Benchmark Entry Template

| Paper / source | Algorithm | Operation | Platform | Device / process node | Frequency | LUT | FF | DSP | BRAM | Area | Power | Latency cycles | Latency time | Memory included | Masking / protection | Result stage | Source table/section | Notes |
|---|---|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---|---|---|---|
| TODO | TODO | KeyGen/Encaps/Decaps/Sign/Verify/NTT/etc. | FPGA/ASIC/software | TODO | TODO | TODO | TODO | TODO | TODO | TODO | TODO | TODO | TODO | yes/no/unclear | yes/no/unclear | pre-synth/post-synth/post-P&R/silicon/unclear | TODO | Do not compare directly without normalized conditions. |

## Comparison rules

When comparing hardware results, the agent must state at least:

- algorithm and parameter set;
- operation measured;
- FPGA device or ASIC process;
- frequency;
- whether the number is cycles or time;
- whether memory/SRAM/BRAM is included;
- whether masking, shuffling, or side-channel protection is included;
- whether the result is pre-synthesis, post-synthesis, post-place-and-route, silicon, or estimated.

## Unsafe claims unless sourced

The agent must not say:

- "implementation A is faster than B";
- "this architecture is smaller";
- "this is the best hardware architecture";
- "candidate X is more efficient than candidate Y";
- "domestic algorithm X has lower area";

unless the benchmark row gives enough conditions to support the comparison.

## Initial corpus status

The uploaded corpus is mainly standards, specifications, status reports, and surveys. It does not yet contain a curated hardware benchmark table. Add rows here only after extracting exact numbers from a paper/report.
