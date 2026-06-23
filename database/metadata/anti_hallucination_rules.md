# Anti-Hallucination Rules

## Core rule

Concepts may be explained freely, but numerical claims must be sourced.

## Claims that require citation or a database row

The agent must cite a primary source or a curated metadata table before giving:

- parameter set names and exact parameter values;
- public key, secret key, ciphertext, shared secret, or signature sizes;
- security categories or security-strength claims;
- NIST standardization status;
- China/domestic standardization status;
- FPGA LUT/FF/DSP/BRAM usage;
- ASIC area, process node, frequency, or power;
- cycle count, latency, throughput, or memory footprint;
- claims using words such as "faster", "smaller", "more efficient", "best", "standardized", or "selected".

## Unavailable-source response

If the current database lacks a source for a requested number, the agent should answer:

> This exact number is not available in the current database. I can explain the concept and identify which source should be checked.

It may then explain qualitatively, but must not invent a value.

## Source hierarchy

1. Prefer FIPS/SP/IR documents for NIST standard facts.
2. Prefer official algorithm specifications for candidate-specific facts.
3. Prefer original papers or official submissions for domestic/candidate algorithms.
4. Use surveys only for background, not exact numeric claims.
5. Use internal notes only for teaching style and project context, not as sole evidence for public facts.

## Teaching mode rule

Teaching analogies are allowed but must be marked as analogies when they could be confused with exact equivalence.

Safe example:

> ML-KEM plays a protocol role closer to ECDH because it establishes a shared secret; the underlying mechanism is different.

Unsafe example:

> ML-KEM is just ECDH with lattices.

## Benchmark mode rule

For any benchmark answer, include the comparison boundary:

- platform;
- parameter set;
- operation;
- frequency;
- memory inclusion;
- masking/protection status;
- result stage.

If these are missing, say the comparison is incomplete.

## Status freshness rule

If the user asks for "current", "latest", or "now", verify against current official sources before answering. The uploaded database is evidence, but it may become stale.
