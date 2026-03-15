# mini-disasm

Educational disassembler for a tiny instruction subset. Focuses on binary parsing, opcode decoding, and human-friendly output formats.

## Features

- Parse binary instruction streams for a small custom or reduced ISA subset.
- Pretty-print mnemonics, operands, and addresses with annotation hints.
- Test cases that map known byte patterns to expected assembly output.

## Learning outcomes

- Understand opcode decoding and the relationship between binary encodings and assembly mnemonics.
- Build clear, testable parsing code and mapping tables.

## Build & run

g++ -std=c++17 -O2 -o mini-disasm main.cpp
./mini-disasm sample.bin

## Notes

- Keep the ISA small and documented. This is an educational tool, not a production disassembler.
