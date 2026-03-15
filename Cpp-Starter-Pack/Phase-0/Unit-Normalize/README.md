# unit-normalize

Parser and normalizer for human-friendly unit strings such as 12.5kHz, 3.3V, 10ms, and 0xFF. Focuses on robust parsing, canonicalization, and unit conversion.

## Features

- Parse numeric values with SI prefixes and common electrical/temporal units.
- Convert to canonical base units (Hz, V, seconds, bytes) with floating-point accuracy control.
- Provide clear error messages for malformed inputs.

## Learning outcomes

- Practice tokenization and grammar for small DSLs.
- Handle edge cases: unit suffixes, optional whitespace, and mixed-case prefixes.
- Create unit tests with representative inputs and expected canonical outputs.

## Build & run

g++ -std=c++17 -O2 -o unit-normalize main.cpp
./unit-normalize "12.5kHz"

- ./unit-normalize "10ms" — 0.010 s
- ./unit-normalize "3.3V" — 3.3 V

## Notes

- Document supported units and prefixes so users know expected behavior.
