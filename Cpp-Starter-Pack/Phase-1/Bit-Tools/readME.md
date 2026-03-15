```markdown
# bit-tools

Collection of compact utilities demonstrating bit-packed structures and a tiny bloom-filter experiment. Focuses on memory-efficient representations and bitwise operations.

Features:
- Implement bit-field packing helpers with explicit size and alignment control.
- Small bloom-filter implementation with tunable parameters and test harness.
- Utilities for counting bits, scanning, and fast bit manipulations.

Learning outcomes:
- Explore memory-efficient representations and bit-level algorithms.
- Practice unit testing probabilistic data structures and measuring false-positive rates.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o bit-tools main.cpp
./bit-tools --test-bloom
```

Notes:
- Document assumptions about machine word size and behavior; provide fallback or tests for different architectures.
```
