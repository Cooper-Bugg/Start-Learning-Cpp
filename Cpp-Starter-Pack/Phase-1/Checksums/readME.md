```markdown
# checksums

Implementations and tests for common checksum and CRC algorithms (CRC-16, CRC-32) with reference test vectors and simple benchmarks.

Features:
- Correct, documented CRC-16 and CRC-32 implementations.
- Test vectors with known-good outputs and small benchmarks to compare implementations.
- Optional streaming interface to compute CRCs over data streams.

Learning outcomes:
- Understand polynomial CRC computation, bit reflection, and common parameter conventions.
- Build test harnesses that validate against RFC or widely-cited vectors.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o checksums tests.cpp crc.cpp
./checksums --run-tests
```

Notes:
- Include comments or documentation explaining CRC parameters (polynomial, init, xorout, reflectIn/Out).
```
