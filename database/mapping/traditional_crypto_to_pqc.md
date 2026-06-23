# Traditional Crypto to PQC Mapping

| Traditional crypto concept | PQC teaching bridge | Warning |
|---|---|---|
| ECDH / key agreement | ML-KEM and HQC play a similar protocol role: establish a shared secret. | KEM is not literally the same mechanism as ECDH. |
| RSA-OAEP public-key encryption | KEM + DEM construction is the modern way to explain public-key encryption with PQC. | ML-KEM should not be presented as bulk encryption. |
| ECDSA / RSA-PSS | ML-DSA, Falcon/FN-DSA, SLH-DSA are signature-side replacements. | Do not mix KEM and signature algorithms. |
| Big-integer modular exponentiation | PQC often uses polynomial/vector/matrix modular arithmetic. | Exact operations depend on algorithm family. |
| ECC scalar multiplication | Lattice schemes often optimize NTT and polynomial-vector arithmetic. | NTT is not a curve operation; it is a transform for polynomial multiplication. |
| SHA/AES | PQC still relies on symmetric primitives for hashing/XOF and bulk encryption. | PQC does not replace AES or SHA wholesale. |
