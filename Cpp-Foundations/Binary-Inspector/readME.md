```markdown
# Binary-Inspector

Compact C++ utility for exploring numeric representations at the bit and byte level. Useful for learning integer endianness, two's complement representation, and IEEE-754 floating-point layout.

Features:
- Print integer values in binary and hexadecimal with configurable width and grouping.
- Display raw bytes for built-in types to demonstrate endianness.
- Decompose floats and doubles into sign, exponent, and mantissa and show reconstructed values.

Learning outcomes:
- Visualize how numeric types are represented in memory.
- Practice bitwise operations, masking, and shifts in C++.
- Add unit tests that validate decomposition against known bit patterns.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o binary-inspector main.cpp
./binary-inspector --float 3.14
```

Usage examples:
- `./binary-inspector 255` — show `255` as hex, binary, and raw bytes.
- `./binary-inspector --float 3.14` — show IEEE-754 decomposition for a `double`.

Notes:
- Document assumed type sizes and provide compile-time guards or fallbacks.
- Include tests for both little-endian and big-endian sample patterns.
```
